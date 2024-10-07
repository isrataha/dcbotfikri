import discord
import random
from discord.ext import commands
intents = discord.Intents.default()
intents.message_content = True
bot = commands.Bot(command_prefix='$', intents=intents)

s1 = "Sizce En İyi Dürüm Hangisi?"
s2 = "Sizce En İyi Yemek Hangisi?"
s3 = "Sizce En Kötü Yemek Hangisi?"
c1 = "Bot Olmak Da Çok Zor"
c2 = "Canım Yağ Çekti"
c3 = "Nimete Kötü Denmez(Hatırlatma)"
soruliste = [s1, s2, s3]
cevapliste = [c1, c2, c3]

def soru():
    return random.choice(soruliste)

def cevapla():
    return random.choice(cevapliste)

@bot.event
async def on_ready():
    print(f'{bot.user} olarak giriş yaptık')

@bot.command()
async def soru(ctx):
    await ctx.send(durumcumleleri.soru())

@bot.command()
async def cevapla(ctx):
    await ctx.send(durumcumleleri.cevapla())


bot.run("MTI4NTI5OTg2MDgxMTAyNjQ4Mg.GfcQYC.sciUGVLN48248pJwzCB348O4diKx7Z0L8NQSkc")
