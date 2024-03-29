# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: flbartol <flbartol@42.student.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/12/27 11:37:55 by ftrujill          #+#    #+#              #
#    Updated: 2019/05/14 15:13:24 by flbartol         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = libftprintf.a
CC = clang
FLAGS = -Wall -Wextra -Werror -Ofast
LIBFT = ft_atoi \
		ft_atoi_base \
		ft_itoa_base \
		ft_bzero \
		ft_min \
		ft_min_int \
		ft_countwords \
		ft_isalpha \
		ft_isdigit \
		ft_isprint \
		ft_itoa \
		ft_lstnew \
		ft_lstdelone \
		ft_lstdel \
		ft_lstadd \
		ft_lstiter \
		ft_lstmap \
		ft_memset \
		ft_memcpy \
		ft_memccpy \
		ft_memmove \
		ft_memchr \
		ft_memcmp \
		ft_memalloc \
		ft_memdel \
		ft_putchar \
		ft_putchar_fd \
		ft_putendl \
		ft_putendl_fd \
		ft_putnbr_fd \
		ft_putnbr \
		ft_putstr \
		ft_putstr_fd \
		ft_strlen \
		ft_strdup \
		ft_strcpy \
		ft_strncpy \
		ft_strcat \
		ft_strncat \
		ft_strlcat \
		ft_strchr \
		ft_strrchr \
		ft_strstr \
		ft_strnstr \
		ft_strcmp \
		ft_strncmp \
		ft_toupper \
		ft_tolower \
		ft_strnew \
		ft_strdel \
		ft_strclr \
		ft_striter \
		ft_striteri \
		ft_strmap \
		ft_strmapi \
		ft_strequ \
		ft_strnequ \
		ft_strsub \
		ft_strjoin \
		ft_strtrim \
		ft_strsplit \
		ft_printf \
		get_next_line \
		ft_atoi_base \
		rgb_to_int \
		rgb_smooth \
		print_c \
		print_d \
		print_else \
		print_lo \
		print_ls \
		print_lx \
		print_o \
		print_p \
		print_percent \
		print_s \
		print_u \
		print_x \
		printf_cast \
		printf_countlength \
		printf_isflags \
		printf_itoa_u \
		printf_parse \
		printf_unicode \


OBJ = $(addprefix obj/, $(addsuffix .o, $(LIBFT)))
OBJ_LIST = $(addsuffix .o, $(LIBFT))
HEADERS = -I./includes

all: $(NAME)

.PHONY: all clean

$(NAME): $(OBJ)
	@echo "\033[36mLinking...\033[34m"
	@ar rcs $(NAME) $(OBJ)
	@ranlib $(NAME)
	@echo  "\033[32m[ ✔ ] Library\033[1;32m $(NAME) \033[1;0m\033[32mis done! \033[0m"
obj/%.o: %.c
	@$(CC) -o $@ $(FLAGS) $(HEADERS) -c $^
	@echo  "\033[37mCompilation of \033[97m$(notdir $<) \033[0m\033[37mdone. \033[0m"
clean:
	@rm -rf $(OBJ)
	@echo  "\033[31m[ ✔ ] Objects files \033[91m$(OBJ_LIST) \033[0m\033[31m removed. \033[0m"
fclean: clean
	@rm -f $(NAME)
	@echo "\033[31m[ ✔ ] Lib \033[1;31m$(NAME) \033[1;0m\033[31mremoved.\033[0m"
re: fclean all