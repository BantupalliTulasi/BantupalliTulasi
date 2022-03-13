import pygame
pygame.init()
white=(255,255,255)
darkblue=(36,19,190)
lightblue=(90,176,240)
red=(255,0,0)

bricks1=[pygame.Rect(10 + i * 100,60,80,30) for i in range(6)]
bricks2=[pygame.Rect(10 + i * 100,100,80,30) for i in range(6)]
bricks2=[pygame.Rect(10 + i * 100,140,80,30) for i in range(6)]

def draw_brick(bricks):
for i in bricks:
pygame.draw.rect(screen,RED,i)

score=0
velocity=[1,1]
size=(600,600)
screen=pygame.display.set_mode(size)
pygame.display.set_caption("my bricks game")
paddl=pygame.rect(100,550,60,10)
ball=pygame.rect(50,250,10,10)
gamecontinue=true
while gamecontinue:
         for event in pygame.event.get():
         if event.type==pygame.QUIT:
         gamecontinue=false
         
 screen.fill(DARKBLUE)
 
 pygame.draw.rect(screen,LIGHTBLUE,paddle)
 
 font=pygame.font.font(None,34)
 text=font.render("SCORE" + str(score),1,WHITE)
 
 screen.blit(text,(20,10))
 if event.type==pygame.KEYDOWN:
    if event.key==pygame.K_RIGHT:
    if paddle.x <540:
    paddle.x=paddle.x +5
 
if event.key==pygame.K_LEFT:
    if paddle.x <0:
    paddle.x=paddle.x -5
    draw_brick(bricks1)

   draw_brick(bricks2)
    draw_brick(bricks3)
    ball.x=ball.x + velocity[0]

ball.y=ball.y + velocity[1]
if ball.x>590 or ball.x <0:


