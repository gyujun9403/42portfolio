# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: gyeon <gyeon@student.42.fr>                +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/04/05 11:59:54 by naykim            #+#    #+#              #
#    Updated: 2022/04/07 18:33:49 by gyeon            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

GCC = gcc
FLAGS = -Wall -Wextra -Werror
TARGET = bonus.a

DIR_SRCS = ./srcs/
DIR_HEADER = ./incs/
SRCS = main_bonus.c \
	light_bonus.c\
	mlx_hook_bonus.c\
	parsing_bonus.c \
	parsing_cone_bonus.c \
	parsing_viewer_bonus.c\
	three_value_2_bonus.c\
	viewer_bonus.c\
	main_bonus.c\
	mlx_img_bonus.c\
	parsing_object_bonus.c\
	ray_bonus.c\
	three_value_vector_bonus.c\
	matrix_bonus.c\
	object_bonus.c\
	object2_bonus.c\
	parsing_utils_bonus.c\
	three_value_1_bonus.c\
	utils_bonus.c
OBJS = $(SRCS:.c=.o)

all : $(TARGET)
$(TARGET) : $(addprefix $(DIR_SRCS), $(OBJS))
	ar rcs $@ $^
%.o : %.c
	$(GCC) $(FLAGS) -c -o $@ $^ -I $(DIR_HEADER)

fclean : clean
	@rm -rf $(TARGET);

clean : 
	@rm -rf $(addprefix $(DIR_SRCS), $(OBJS));

re : clean fclean all
PHONY : all fclean clean re