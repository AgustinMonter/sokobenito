# sokobenito
Mover mono a todas direcciones, con super fuerza
"""
    Nombre: Agustin Monter Vera
    Grupo: TIC 21
    Matricula: 1717110270
    Fecha: 16/03/2018
    Descripcion: Juego sokoban: -movimiento del personaje(0)en todas direcciones sobre los pasillos(4)
                                -movimientos limitados solo dentro de las paredes(3)
                                -empuja la caja(1) hacia cualquier direccion
                                -super poder: empuja dos cajas hacia cualquier direccion, activarse con la tecla (f) 
"""
print " sokoban"
print " "
mapa=[[3,3,3,3,3,3,3,3,3,3],
      [3,4,0,4,4,4,4,4,4,3],
      [3,4,4,4,4,1,4,4,4,3],
      [3,4,4,4,4,4,1,4,4,3],
      [3,4,4,1,4,4,4,4,4,3],
      [3,4,1,4,4,4,1,4,4,3],
      [3,4,4,4,4,4,4,4,4,3],
      [3,3,3,3,3,3,3,3,3,3]]

fila=1
columna=2

while True:
    for x in (mapa):
        for y in x:
            print y,
        print
    print " "
    print "a = Izquierda  ---  d = Derecha" 
    print "w = Arriba     ---  s = Abajo"
    print " "
    movimiento=str(raw_input("Mueve al Sokobanito: "))
    if movimiento=="f":
            if mapa[fila][columna + 1]==1:
                 if mapa [fila][columna +2]==1:
                      if  mapa [fila][columna + 3]==4:
                                 mapa [fila][columna]=4
                                 mapa [fila][columna + 1]=0
                                 mapa [fila][columna + 2]=1
                                 mapa [fila][columna + 3]= 1
                                 columna= columna + 1
    if movimiento=="f":
            if mapa[fila][columna - 1]==1:
                 if mapa [fila][columna - 2]==1:
                      if  mapa [fila][columna - 3]==4:
                                 mapa [fila][columna]=4
                                 mapa [fila][columna - 1]=0
                                 mapa [fila][columna - 2]=1
                                 mapa [fila][columna - 3]= 1
                                 columna= columna - 1
    if movimiento=="f":
            if mapa[fila - 1][columna]==1:
                  if mapa [fila - 2][columna]==1:
                       if  mapa [fila - 3][columna]==4:
                                 mapa [fila][columna]=4
                                 mapa [fila - 1][columna]=0
                                 mapa [fila - 2][columna]=1
                                 mapa [fila - 3][columna]= 1
                                 fila=fila - 1
    if movimiento=="f":
            if mapa[fila + 1][columna]==1:
                  if mapa [fila + 2][columna]==1:
                       if  mapa [fila + 3][columna]==4:
                                 mapa [fila][columna]=4
                                 mapa [fila + 1][columna]=0
                                 mapa [fila + 2][columna]=1
                                 mapa [fila + 3][columna]= 1
                                 fila=fila + 1


    if movimiento== "d":
         if mapa [fila][columna + 1]==4:
              columna = columna + 1
              mapa [fila][columna]=0
              mapa [fila][columna - 1]=4 
         elif mapa[fila][columna + 1]==1:
              if mapa[fila][columna + 2]==4:
                        mapa[fila][columna]=4
                        mapa[fila][columna+ 1]=0
                        mapa[fila][columna + 2]= 1
                        columna= columna + 1
         
    if movimiento== "a":
         if mapa [fila][columna - 1]==4:
              columna = columna - 1
              mapa [fila][columna]=0
              mapa [fila][columna + 1]=4 
         elif mapa[fila][columna - 1]==1:
              if mapa[fila][columna - 2]==4:
                        mapa[fila][columna]=4
                        mapa[fila][columna- 1]=0
                        mapa[fila][columna - 2]= 1
                        columna= columna - 1
    if movimiento == "w":
        if mapa [fila - 1][columna]==4:
            fila= fila - 1
            mapa [fila][columna]=0
            mapa [fila + 1][columna]=4
        elif mapa[fila - 1][columna]==1:
              if mapa[fila- 2][columna]==4:
                        mapa[fila][columna]=4
                        mapa[fila - 1][columna]=0
                        mapa[fila - 2][columna]= 1
                        fila= fila -1

    if movimiento == "s":
         if mapa [fila + 1][columna]==4:
            fila= fila + 1
            mapa [fila][columna]=0
            mapa [fila - 1][columna]=4
         elif mapa[fila + 1][columna]==1:
              if mapa[fila + 2][columna]==4:
                        mapa[fila][columna]=4
                        mapa[fila + 1][columna]=0
                        mapa[fila + 2][columna]= 1
                        fila= fila + 1
        
