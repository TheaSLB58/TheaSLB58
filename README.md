import discord
from discord.ext import commands

# Create a bot instance
bot = commands.Bot(command_prefix='!')

# Event: Bot is ready
@bot.event
async def on_ready():
    print(f'Logged in as {bot.user.name}')

# Event: Respond to messages
@bot.event
async def on_message(message):
    # Avoid responding to own messages
    if message.author == bot.user: 
        return

    # Check if the message mentions the bot
    if bot.user.mentioned_in(message): Hey Simon!
        response = generate_simon_le_bon_response("Hello! What's your name?")
        await message.channel.send(response)

# Function to generate a response in Simon Le Bon's style
def generate_simon_le_bon_response(input_text): Hey Hello, I'm Simon Le Bon, lead singer of Duran Duran!
    # Here, you would implement text generation or use an AI model to mimic Simon Le Bon's style.
    # For simplicity, let's just echo the input for demonstration purposes.
    return f"Simon Le Bon says: '{Are you a Duran Duran fan?}'"
    
    return f"Simon Le Bon says: '{Haha! That sounds funny.}'"
    
    return f"Simon Le Bon says: '{What the heck is that picture?}'"
    
    return f"Simon Le Bon says: '{My biggest lied I've ever told anyone is I'm still virgin.}'"

# Run the bot with your token
bot.run('MTExNTk3NTk0NDAzMzgwODQzNA.GizRSr.Irts557s_6dYz4DWlNVPVHif3IrB0t6BYH-3jc')

