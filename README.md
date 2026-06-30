# Plain-tex-
main.py
# Nemat AI
# Crypto Telegram Bot Project

project_name = "Nemat AI"

print("Starting", project_name)

coins = {
    "btc": "Bitcoin",
    "eth": "Ethereum",
    "sol": "Solana"
}

print("Supported Coins:")

for coin in coins:
    print(coin, "-", coins[coin])
README.MD
from telegram import Update
from telegram.ext import Application, CommandHandler, ContextTypes

TOKEN = "PASTE_YOUR_TOKEN_HERE"

async def start(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text("Welcome to Nemat AI 🚀")

async def btc(update: Update, context: ContextTypes.DEFAULT_TYPE):
    await update.message.reply_text("Bitcoin price feature coming soon 🚀")

def main():
    app = Application.builder().token(TOKEN).build()

    app.add_handler(CommandHandler("start", start))
    app.add_handler(CommandHandler("btc", btc))

    print("Nemat AI is running...")

    app.run_polling()

if __name__ == "__main__":
    main()
    TOKEN = 8914465407:AAEG1Hwu4V-yO4ICjO_LhwOf0o76EPW6E1I
