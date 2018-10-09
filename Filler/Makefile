# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: mmtana	  <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/07/30 03:23:24 by mmtana            #+#    #+#              #
#    Updated: 2018/08/08 16:31:32 by mmtana           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = resources/players/mmtana.filler

SRCS := srcs/main.c 
SRCS +=	srcs/tools.c 
SRCS +=	srcs/tools2.c 
SRCS +=	srcs/ft_parcing.c 
SRCS +=	srcs/play.c 
SRCS +=	srcs/play2.c 

FLAGS = -Wall -Werror -Wextra -I./includes

OBJ = $(SRCS:.c=.o)

all: $(NAME)

$(NAME): $(OBJ)
	make -C libft
	make -C visualization
	gcc -o $(NAME) $(FLAGS) $(OBJ) libft/libft.a
	echo "Filler done"

clean:
	make clean -C libft
	make clean -C visualization
	rm -f $(OBJ)

fclean: clean
	make fclean -C libft
	make fclean -C visualization
	rm -f $(NAME)

re: fclean all
