python
import pygame
import sys

# Inicializa o Pygame
pygame.init()

# Configurações da tela
screen_width, screen_height = 800, 600
screen = pygame.display.set_mode((screen_width, screen_height))
pygame.display.set_caption("Ver Através da Parede")

# Cores
WHITE = (255, 255, 255)
BLACK = (0, 0, 0)
GREEN = (0, 255, 0)

# Função para desenhar a parede
def draw_wall():
    pygame.draw.rect(screen, BLACK, (300, 100, 200, 400))

# Função principal
def main():
    while True:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                pygame.quit()
                sys.exit()

        screen.fill(WHITE)
        draw_wall()

        # Aqui você pode adicionar lógica para "ver" através da parede
        # Por exemplo, desenhar um objeto ou personagem que pode ver através da parede
        pygame.draw.circle(screen, GREEN, (400, 300), 50)  # Representa o que está "atrás" da parede

        pygame.display.flip()

if __name__ == "__main__":
    main()
