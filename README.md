graph {

    "POV: You are about to sacrifice 5 treasures and activate Magda!" -- "Is the board safe? Staxed out, or opponents are tapped out."


    YesSafe [label="Yes!"]
    NoSafe [label="No :("]
    "Is the board safe? Staxed out, or opponents are tapped out." -- YesSafe
    "Is the board safe? Staxed out, or opponents are tapped out." -- NoSafe

    YesSafe -- "Do you have/can you make an artifact dwarf?"
    YesDwarf [label="Yes!"]
    NoDwarf [label="No :("]
    "Do you have/can you make an artifact dwarf?" -- YesDwarf
    "Do you have/can you make an artifact dwarf?" -- NoDwarf

    NoDwarf -- "Get another stax piece if someone can win soon"
    NoDwarf -- "Just wait for a better time."
    NoDwarf -- "Utvara Hellkite lol"

    YesDwarf -- "Well it's time win the game!"

    NoSafe -- "If noone is about to win, you can get GPS"
    NoSafe -- "Hold on for a last-minute interaction (Jar, Hellkite) or a better moment when you can win"


    "Well it's time win the game!" -- "Do you have access Maskwood and Xorn?"
    YesMX [label="Yes!"]
    NoMX [label="No :("]
    "Do you have access Maskwood and Xorn?" -- YesMX
    "Do you have access Maskwood and Xorn?" -- NoMX

    NoMX -- "Can you perform Rube Goldberg?"

    YesRube [label="Yes!"]
    NoRube [label="No :("]
    "Can you perform Rube Goldberg?" -- YesRube
    "Can you perform Rube Goldberg?" -- NoRube

    YesRube -- "Then you can make infinite untapped treasures!"
    YesMX -- "Then you can make infinite untapped treasures!"

    NoRube -- "You can win with Double Welder loop (no Elixir required)"


    "Then you can make infinite untapped treasures!" -- "Have you access to Elixir?"
    YesElixir [label="Yes!"]
    NoElixir [label="No :("]

    "Have you access to Elixir?" -- YesElixir
    "Have you access to Elixir?" -- NoElixir

    YesElixir -- "Win with Memory Jar loops!"
    YesElixir -- "Win with Facebreaker damage spells loops!"

    NoElixir -- "Win with Hellkite etb Welder loops!"
}
