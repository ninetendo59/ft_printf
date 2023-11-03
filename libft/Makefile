# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: hetan <hetan@student.42kl.edu.my>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/04/29 20:28:13 by hetan             #+#    #+#              #
#    Updated: 2023/10/16 23:07:40 by hetan            ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libft.a
HEADER = ../header

SOURCE = ft_isascii.c	\
			ft_putchar_fd.c	\
			ft_strdup.c		\
			ft_strmapi.c	\
			ft_tolower.c	\
			ft_atoi.c		\
			ft_isdigit.c	\
			ft_memchr.c		\
			ft_putendl_fd.c	\
			ft_striteri.c	\
			ft_strncmp.c	\
			ft_toupper.c	\
			ft_bzero.c		\
			ft_isprint.c	\
			ft_memcmp.c		\
			ft_putnbr_fd.c	\
			ft_strjoin.c	\
			ft_strnstr.c	\
			ft_calloc.c		\
			ft_itoa.c		\
			ft_memcpy.c		\
			ft_putstr_fd.c	\
			ft_strlcat.c	\
			ft_strrchr.c	\
			ft_isalnum.c	\
			ft_memmove.c	\
			ft_split.c		\
			ft_strlcpy.c	\
			ft_strtrim.c	\
			ft_isalpha.c	\
			ft_memset.c		\
			ft_strchr.c		\
			ft_strlen.c		\
			ft_substr.c
SOURCEB = ft_lstadd_back.c			\
				ft_lstadd_front.c	\
				ft_lstdelone.c		\
				ft_lstiter.c		\
				ft_lstlast.c		\
				ft_lstmap.c			\
				ft_lstnew.c			\
				ft_lstsize.c		\
				ft_lstclear.c

OBJ_S = obj/
OBJ = $(SOURCE:.c=.o)
OBJ_PREFIX = $(addprefix $(OBJ_S),$(OBJ))
OBJB=$(SOURCEB:.c=.o)
OBJB_PREFIX = $(addprefix $(OBJ_S),$(OBJB))
OBJF		= .cache_exists

CC = cc

CC_FLAGS = -Wall -Wextra -Werror

all: $(NAME)

$(NAME): $(OBJ_PREFIX)
	ar r $(NAME) $(OBJ_PREFIX)
	echo "Libft compiled!"

$(OBJ_S)%.o : %.c | $(OBJF)
	echo "Compiling: $<"
	$(CC) $(CC_FLAGS) -I $(HEADER) -c $< -o $@

$(OBJF):
	@mkdir -p $(OBJ_S)

all : $(NAME) $(OBJ_PREFIX)

clean:
	@rm -rf $(OBJ_S)

fclean: clean
	@rm -f $(NAME)

re: fclean all

bonus: $(OBJB_PREFIX)
	ar r $(NAME) $(OBJB_PREFIX)
	echo "Bonus Libft compiled!"

.PHONY : all clean fclean re bonus
