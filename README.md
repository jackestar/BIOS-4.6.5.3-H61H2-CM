# BIOS-4.6.5.3-H61H2-CM
BIOS 4.6.5.3 H61H2-CM Descargar

# Flash OSless

## Requerido 

- Rufus [Github](https://github.com/pbatard/rufus) [Pagina Web](rufus.ie)

## Pasos a seguir

1. -Descargar los datos relacionados.
  * ![Image text](https://github.com/smltrs0/BIOS-4.6.5.3-H61H2-CM/blob/main/InfoTutorial/1.jpg)
3. -Formatear el pendrive utilizando rufus en el modo FreeDos. 
4. -Pasar toda la información del zip al pendrive.
5. -Cambiar de posición Jumper (Esto retira la protección anti escrituras de las BIOS) -NECESARIO
6. -Iniciar el pendria como el disco booteable.
7. -Seleccionar el metodo distribución que utiliza tu teclado, es irelevante para el proceso.
8. -Escribir el comando  "FPT -F BIOS.BIM" en la consola que se habilita despues de completar el paso 6.
9. -Esperar a que se complete la instalación.
10. -Apagar el equipo.
11. -Retirar la bateria y las fuentes de alimentacion de la placa por 1 MIN.
12. -Colocar el jumper de protección de las BIOS en su posicion original.

Al encender el equipo tendras la tarjeta madre con las BIOS actuaizada.

## Otras versiones

backup 4.6.4 (incluye BIOS/ME/FD es el dump completo del chip)
permite mas controls de la bios (overclocking etc...) (no Changelog disponible/encontrado)

# Flash con linux

## Pasos a seguir

1. Asegurese de tener el jumper WP_BIOS (generalmente no esta populado) y MS_DIS desactivado (en posicion 2-3 si se quiere hacer backup o si genera problemas)
2. pasar el parametro `iomem=relaxed` al kernel al inicio (de hacer falta) (esta es una medida de seguridad de linux)
3. tener instalado flashrom (vease la documentacion de su distro para la instalacion)
4. `sudo flashrom -p internal -c "MX25L3205D/MX25L3208D" -r backup.rom` (backup si se requiere)
5. `sudo flashrom -p internal -c "MX25L3205D/MX25L3208D" -w BIOS.BIN`
