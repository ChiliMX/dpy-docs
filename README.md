# Dpy-Docs
A simple, lightweight tool used for documemting your discord.py commands


### Usage:

```py
import discord
from discord.ext import commands

from dpy_docs import DocGen

bot = commands.Bot(command_prefix="!", intents=discord.Intents.all())
docs = DocGen(bot)


@docs.generate_docs()
@bot.command()
async def foo(ctx: commands.Context) -> None:
    """This is an example command"""
    return 


bot.run(TOKEN)
```
Note: You *must* add `@docs.generate_docs()` before `@bot.command()`. This is due to the current code logic, and might be changed in the future.