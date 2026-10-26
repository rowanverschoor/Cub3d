# cub3D

A small raycasting game in C, inspired by Wolfenstein 3D. Made as part of the 42 curriculum at Codam.

It reads a `.cub` map file and renders a first-person 3D view using DDA raycasting. Graphics are handled with [MLX42](https://github.com/codam-coding-college/MLX42).

## Build

You need `cc`, `make`, `cmake` and `glfw`.

```sh
git clone --recursive https://github.com/rowanverschoor/Cub3d.git
cd Cub3d
make          # builds ./cub3D
make bonus    # builds ./cub3D_bonus
```

## Run

```sh
./cub3D maps/subject.cub
./cub3D_bonus maps/42_bonus.cub
```

## Controls

| Key | Action |
| --- | --- |
| W A S D | Move |
| ← → | Turn |
| Esc | Quit |

Bonus only:

| Input | Action |
| --- | --- |
| Mouse | Look around |
| Left click / Space | Shoot. Shooting a door up close opens or closes it. |

## Map format

```
NO ./img/wallred.png
SO ./img/wallgrey.png
WE ./img/walldark.png
EA ./img/wallblue.png

F 220,100,0
C 225,30,0

111111
100001
10N001
111111
```

- `NO` `SO` `WE` `EA`: wall textures (PNG)
- `F` `C`: floor and ceiling colour in RGB
- `1` wall, `0` floor, `N` `S` `E` `W` player start and facing
- `D` door (bonus only)

The map must be closed off by walls. This is checked with a flood fill.

## Bonus

- Wall collisions
- Minimap
- Doors that open and close
- Animated gun
- Mouse look

## Authors

- [roversch](https://github.com/rowanverschoor)
- [nhendrik](https://github.com/Nissey05)
