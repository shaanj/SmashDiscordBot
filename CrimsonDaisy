import discord
from discord.ext import commands
import requests

client = commands.Bot(command_prefix='!', help_command=None)

@client.event
async def on_ready():
    print('Bot is ready.')
    general_channel = client.get_channel(818338932319846414)
    await general_channel.send('Hello Shaan.')
    await client.change_presence(status = discord.Status.online, activity = discord.Game('Super Smash Bros. Ultimate'))


@client.event
async def on_message(message):
    if message.author == client.user: return

    if message.content.startswith("hello"):
        await message.channel.send("Hello! " + message.author.mention)

    if "smash" in message.content and "!" not in message.content:
        await message.channel.send("I'll smash your dad")

    await client.process_commands(message)


@client.command(name = 'help')
async def help(context):
    file = discord.File("Images/DaisyIcon.png", filename="image.png")
    CrimsonDaisy = discord.Embed(title = "Help", type = "rich", description = "I am Crimson mf Daisy", color = 0x00ff00)
    CrimsonDaisy.set_thumbnail(url="attachment://image.png")
    CrimsonDaisy.set_author(name = "Crimson Daisy", icon_url = "https://ssb.wiki.gallery/images/2/2d/DaisyHeadSSBUWebsite.png")
    CrimsonDaisy.add_field(name = "!smash <OPTIONAL @USER>", value = "Smash that mf", inline=False)
    CrimsonDaisy.set_footer(text = "Degen Daisy Main")
    await context.message.channel.send(file=file, embed=CrimsonDaisy)


@client.command(name = 'smash')
async def smash(context, user : discord.User = None):
    if not user:
        await context.send("Fire Emblem exists")
    else:
        await context.send("I'm gonna smash " + user.mention)

@client.command(name = 'Daisy')
async def Daisy(context):
    file = discord.File("Images/DaisyImage.png", filename="image.png")
    CrimsonDaisy = discord.Embed(title = "Daisy", type = "rich", description = "My Main, float cancels OP", color = 0xfca103)
    CrimsonDaisy.set_thumbnail(url="attachment://image.png")
    CrimsonDaisy.set_author(name = "#13: Daisy", url = "https://open.spotify.com/album/0Sft679qCdCzuedMr6Obue", icon_url = "https://ssb.wiki.gallery/images/2/2d/DaisyHeadSSBUWebsite.png")
    CrimsonDaisy.add_field(name = "Run Speed", value = "1.595", inline=True)
    CrimsonDaisy.add_field(name = "Air Speed", value = "1.029", inline=True)
    CrimsonDaisy.add_field(name = "Fall/Fast Fall Speed", value = "1.19/1.904", inline=False)
    CrimsonDaisy.set_footer(text = "Absolute scale: Sonic = highest run speed, Robin = very low run speed")
    await context.message.channel.send(file=file, embed=CrimsonDaisy)
       
client.run('TOKEN')
