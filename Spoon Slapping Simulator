import pygame
import sys
import random
from pygame.locals import *
pygame.init()
screen = pygame.display.set_mode((500,500))
#Variables
blue = (0,0,255)
black = (0,0,0)
white = (255,255,255)
red = (255,0,0)
x = 250
y = 100
aix = 250
aiy = 400  
spoonx = x
spoony = y
circlex = spoonx + 5
circley = spoony + 50
clock = pygame.time.Clock()
#End of Variables
while True:
  for event in pygame.event.get():
    if event.type == QUIT:
      pygame.quit()
      exit()

  #Character Initialization
  screen.fill(black)
  character = pygame.draw.circle(screen,blue,(x,y),35)
  if event.type == pygame.KEYDOWN:
    if event.key == pygame.K_RIGHT:
      x = x + 2
      spoonx = x
      circlex = spoonx + 5
    if event.key == pygame.K_LEFT:
      x = x - 2
      spoonx = x
      circlex = spoonx + 5
    if event.key == pygame.K_UP:
      y = y - 2
      spoony = y
      circley = spoony + 50
    if event.key == pygame.K_DOWN:
      y = y + 2
      spoony = y
      circley = spoony + 50
  #End Of Character Initialization

  #Making Font
  
  
  #Making Spoon
  pygame.draw.rect(screen,red,(spoonx,spoony,10,50))
  spoontip = pygame.draw.circle(screen,red,(circlex,circley),10)
  #End of Making Spoon

  #Making AI
  ai = pygame.draw.circle(screen,red,(aix,aiy), 25)
  aiy = aiy - 1
  #End of making ai

  #Collision
  if spoontip.colliderect(ai):
    aiy = 400
    aix = random.randint(100, 400)
  #Score
  font_obj=pygame.font.Font("freesansbold.ttf",100)
  text_obj=font_obj.render("Score:",True,blue)
  screen.blit(text_obj,(255,255))
  #End of Score
  
  pygame.display.update()
  clock.tick(200)
