import turtle

# Set up the screen
turtle.bgcolor("black")

# Create the turtle
pen = turtle.Turtle()
pen.color("red")
pen.pensize(3)
pen.speed(5)

# Draw the heart
pen.begin_fill()
pen.fillcolor("red")

pen.left(140)
pen.forward(180)
pen.circle(-90, 200)
pen.left(120)
pen.circle(-90, 200)
pen.forward(180)

pen.end_fill()

# Hide the turtle
pen.hideturtle()

# Keep the window open
turtle.done()
