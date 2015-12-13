
from meet import *
import random
cells=[]
colors=["pink","blue","purple","green","red"]
cells_num= 0
for i in range(40):
	ball1={"radius":random.randint(5,100), "x":random.randint(10,200),"y":random.randint(10,200) ,  "dy":random.uniform(-0.70,-0.90),"dx":random.uniform(-0.40,0.50),"color":random.choice(colors)}
	circle1 = create_cell(ball1)
	cells.append(circle1)
	cells_num=cells_num+1

user_cell={"radius":random.randint(5,100), "x":random.randint(10,200),"y":random.randint(10,200) ,  "dy":random.uniform(-0.70,-0.90),"dx":random.uniform(-0.40,0.50),"color":random.choice(colors)}
t=create_cell(user_cell)
cells.append(t)

	


def limits(cells):
	for cell in cells:
		width=get_screen_width()
		height=get_screen_height()
		x=cell.xcor()
		y=cell.ycor()


		if (cell.xcor() > width):
			cell.set_dx(-cell.get_dx())
		if (cell.ycor() > height):
			cell.set_dy(-cell.get_dy())
		if (cell.xcor() < -width):
			cell.set_dx(-cell.get_dx())
		if (cell.ycor() < -height):
			cell.set_dy(-cell.get_dy())






while(True):
	move_cells(cells)
	limits(cells)
	dx,dy = get_user_direction(t)
	t.set_dx(dx)
	t.set_dy(dy)


	
meet.mainloop()
