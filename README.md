# Preámbulo
Lo que pretendo con este proyecto es poder detallar como monté mi impresora 3D Voron 0.2. No es una guía concisa sino más bien una colección de fotos y descripción del proceso, poniendo énfasis en las partes que me generaron dudas o errores, por si puede ser de ayuda de alguien, igual que a mí me ha servido el trabajo de otros.
Hace años que escuché sobre el proyecto RepRap y quería montar una impresora 3D de principio a fin, pero por circunstancias de la vida no lo hice hasta ahora. Mi experiencia con impresión 3D real, es de alrededor de 3 años y de forma intermitente. Tuve una Creality Ender V3 KE, que nunca llegó a funcionar bien, y luego la cambié por una Bambu Lab A1 la cual fue mi salvación. Si que tengo algo de experiencia en electrónica y programación, pero esta será la primera vez que me meto en las tripas de una impresora 3D.
El kit que monté es el de Formbot (Voron 0.2 r1) ya que me pareció el más adecuado por relación calidad precio. Las piezas 3D necesarias, las pedí imprimir a un compañero ya que yo no tenía capacidad de impresión con ABS o ASA.
Los capítulos intentan seguir el mismo orden que el de la guía de montaje de Voron, aunque he añadido un capítulo 0 para la descripción de las piezas impresas y los capítulos finales dedicados a firmware y software.

# Capítulo 0 – Preparación e impresión de piezas y perfiles aluminio
Como he dicho antes, el kit que compré es el de Formbot (Voron 0.2 r1), añadiendo el Phaetus Standard Dragon-Flow como hotend. El paquete llegó bien, estaba bien protegido y el envío tardó poco tiempo en llegar.
Por lo que conozco, para montarte tu propia Voron Zero, puedes conseguir las piezas impresas a través del mismo vendedor del kit (suelen ofrecer un suplemento y te añaden todas las piezas impresas necesarias), a través del servicio PIF de Voron (te las imprime una persona que cumple unos mínimos de calidad reconocidos por Voron) o imprimirlas tú mismo o alguien que tenga impresora 3D.
La opción de comprarla junto al kit creo que es la más económica pero no hay opciones de color (negro y las partes de acento en rojo) y en algunos videos hay gente que ha reportado piezas no impresas del todo bien. Pero ya que me pongo con el proyecto, quería poder elegir el color de las piezas impresas y que no fuera otra Voron más, así que exploré las otras opciones. Yo mismo tengo impresora, pero es abierta y no podría imprimir ABS o ASA de forma fiable, así que contacté con un amigo que sí que contaba con impresoras preparadas y experiencia en impresión 3D y resultaba más económico que el PIF. Pero tenía que preparar yo mismo el fichero con todos los stls necesarios, así que aquí os describo qué stls necesité.
Estos stls se pueden encontrar en la propia página de Voron Design y en la propia página de Formbot. Yo usé los stls que proporciona Voron, ya que no sabía que Formbot también tenían los stls necesarios para el kit. Lo bueno de los que proporciona Formbot es que ya están todas las piezas necesarias para el kit específico, mientras que en la página de Voron hay multitud de piezas que no serán necesarias para tu kit e incluso algunas no las encontrarás directamente en el paquete de stls (por ejemplo, las piezas para la cama Kirigami), lo cual me hizo pedir más de una vez imprimir piezas que me faltaban. Pero si quieres usar dos colores a la vez en una misma pieza (como en mi caso), lo tienes en los documentos de Voron. Además de esto, en la página de Voron mods también puedes encontrar algunas piezas interesantes, como por ejemplo las asas laterales que van realmente bien.
Ahora os explicaré que piezas tuve que imprimir partiendo de lo que podéis encontrar en la página de Voron Design sobre el modelo 0.2. En la carpeta que te descargas con los stls, hay un documento Readme.md que podéis abrir con el bloc de notas y ahí explica claramente la nomenclatura de los archivos, para mi queda muy clara, así que os explicaré las cosas con las que dudé más o directamente me equivoqué.
En la carpeta de Electronics, yo imprimí el fichero de RPi_or_BTT-Pico_Mount que servirá para la SKR pico pero no para la Pi de mi kit.
En la carpeta de Skirts me equivoqué e imprimí el Foot_Rear_Right_Plain, pero en realidad para el kit de formbot, y para seguir las instrucciones del manual, la pieza a imprimir es Foot_Rear_Right_FRS_x1.
Dentro de las Toolheads, para el kit de formbot, el tipo de cabezal es el Mini_Stealthburner, así que imprimí todos los archivos de esa carpeta.
Y por otro lado, hay que descargarse los stls de la cama Kirigami por separado. Yo los descargué del github de christophmuellerorg (link), que es el oficial que aparece en el manual, pero también aparece en los stls de formbot, que son los que describo en la tabla de más abajo. 
En las siguientes tablas pongo todas las piezas que imprimí.
| Nombre pieza                     | Cantidad | Carpeta                         | Comentario |
|----------------------------------|----------|----------------------------------|------------|
| [a]_Idler_Cam_Lock_x2            | 2        | Raiz                             |            |
| [a]_Z_Endstop_Mount_x1           | 1        | Raiz                             |            |
| [a]_Z_Motor_Mount_x1             | 1        | Raiz                             |            |
| A_Idler_Lower_x1                 | 1        | Raiz                             |            |
| A_Idler_Upper_x1                 | 1        | Raiz                             |            |
| Drag_Chain_Spacer_x1             | 1        | Raiz                             |            |
| T8_Nut_Block_x1                  | 1        | Raiz                             |            |
| X_Carriage_x1                    | 1        | Raiz                             |            |
| [a]_9mm_Spacer_x6                | 6        | Raiz                             |            |
| [a]_A_Drive_Tensioner_x1         | 1        | Raiz                             |            |
| [a]_B_Drive_Tensioner_x1         | 1        | Raiz                             |            |
| [a]_Railstops_x5                 | 5        | Raiz                             |            |
| [a]_Tensioner_Knob_x2            | 2        | Raiz                             |            |
| A_Drive_Frame_Lower_x1           | 1        | Raiz                             |            |
| A_Drive_Frame_Upper_x1           | 1        | Raiz                             |            |
| B_Drive_Frame_Lower_x1           | 1        | Raiz                             |            |
| B_Drive_Frame_Upper_x1           | 1        | Raiz                             |            |
| B_Idler_Lower_x1                 | 1        | Raiz                             |            |
| B_Idler_Upper_x1                 | 1        | Raiz                             |            |
| M2_Nut_Adapter_Rotated_x5        | 5        | Raiz                             |            |
| Spool_Holder_x1                  | 1        | Raiz                             |            |
| XY_Joint_Left_Lower_x1           | 1        | Raiz                             |            |
| XY_Joint_Left_Upper_x1           | 1        | Raiz                             |            |
| XY_Joint_Right_Lower_x1          | 1        | Raiz                             |            |
| XY_Joint_Right_Upper_x1          | 1        | Raiz                             |            |
| [a]_Guidler_x1                   | 1        | Toolheads/Mini_Stealthburner     |            |
| [a]_Latch_x1                     | 1        | Toolheads/Mini_Stealthburner     |            |
| [a]_MiniSB_MidBody_x1            | 1        | Toolheads/Mini_Stealthburner     |            |
| [a]_MiniSB_Motor_Plate_x1        | 1        | Toolheads/Mini_Stealthburner     |            |
| [a]_Shuttle_x1                   | 1        | Toolheads/Mini_Stealthburner     |            |
| Strain_Relief_Spacer_x2          | 2        | Toolheads/Mini_Stealthburner     |            |
| Door_Handle_x1                   | 1        | Panel_Mounting                   |            |
| Door_Latch_x2                    | 2        | Panel_Mounting                   |            |
| Front_Bottom_Left_Clip_x1        | 1        | Panel_Mounting                   |            |
| Front_Bottom_Right_Hinge_x1      | 1        | Panel_Mounting                   |            |
| Front_Top_Left_Clip_x1           | 1        | Panel_Mounting                   |            |
| Front_Top_Right_Hinge_x1         | 1        | Panel_Mounting                   |            |
| Left_Bottom_Rear_Panel_Clip_x1   | 1        | Panel_Mounting                   |            |
| Left_Top_Rear_Panel_Clip_x1      | 1        | Panel_Mounting                   |            |
| Middle_Clip_x9                   | 7        | Panel_Mounting                   | Al usar los Stealth Handles especificados en la tabla de mods, te ahorras dos, por eso solo hace falta imprimir 7 |
| Rear_Bottom_Left_Clip_x1         | 1        | Panel_Mounting                   |            |
| Rear_Bottom_Right_Clip_x1        | 1        | Panel_Mounting                   |            |
| Right_Bottom_Front_Hinge_x1      | 1        | Panel_Mounting                   |            |
| Right_Bottom_Rear_Panel_Clip_x1  | 1        | Panel_Mounting                   |            |
| Right_Top_Left_Hinge_x1          | 1        | Panel_Mounting                   |            |
| Right_Top_Rear_Panel_Clip_x1     | 1        | Panel_Mounting                   |            |
| Left_Bottom_Front_Panel_Clip_x1  | 1        | Panel_Mounting                   |            |
| Left_Top_Front_Panel_Clip_x1     | 1        | Panel_Mounting                   |            |
| [a]_Foot_Accent_A_x2             | 2        | Skirts                           |            |
| [a]_Foot_Accent_B_x2             | 2        | Skirts                           |            |
| [a]_Logo_Insert_x2               | 1        | Skirts                           |            |
| Foot_Front_Left_x1               | 1        | Skirts                           |            |
| Foot_Front_Right_x1              | 1        | Skirts                           |            |
| Foot_Rear_Left_Inlet_x1          | 1        | Skirts                           |            |
| Foot_Rear_Right_FRS_x1           | 1        | Skirts                           |            |
| MGN7_Rail_Guide_x2               | 2        | Tools                            | Se pueden imprimir en cualquier material |
| Swiss_Army_Jig_x1                | 1        | Tools                            | Se pueden imprimir en cualquier material |
| [c]_Display_Diffuser_x1          | 1        | Display                          |            |
| Display_Knob_x1                  | 1        | Display                          |            |
| Display_Mount_Left_x1            | 1        | Display                          |            |
| Display_Mount_Right_x1           | 1        | Display                          |            |
| Fan_Mount_Bottom_x1              | 1        | Electronics                      |            |
| Fan_Mount_Top_x1                 | 1        | Electronics                      |            |
| PCB_DIN_Clip_x2                  | 2        | Electronics                      |            |
| PSU_Cover_x1                     | 1        | Electronics                      |            |
| RPi_or_BTT-Pico_Mount            | 1        | Electronics                      |            |
| TH_Hinge_A_Bottom_x1             | 1        | Tophat                           |            |
| TH_Hinge_A_Top_x1                | 1        | Tophat                           |            |
| TH_Hinge_B_Bottom_x1             | 1        | Tophat                           |            |
| TH_Hinge_B_Top_x1                | 1        | Tophat                           |            |
| TH_Lower_Clip_Mirror_x3          | 3        | Tophat                           |            |
| TH_Lower_Clip_x3                 | 3        | Tophat                           |            |
| TH_Side_Clip_Mirror_x4           | 4        | Tophat                           |            |
| TH_Side_Clip_x4                  | 4        | Tophat                           |            |
| TH_Top_Clip_x4                   | 4        | Tophat                           |            |
| Display_Faceplate_Multibody_x1   | 1        | Mult

Estos son stls específicos para el kit de formbot y que descargué de su página, a excepción de las partes de la cama kirigami, que las descargué del github comentado anteriormente, pero son las mismas piezas.
| Nombre pieza | Cantidad | Carpeta | Comentario |
|---|---:|---|---|
| BTT PI_Bracket.stl | 1 | 黑色 | Para la raspberry pi que tiene el kit |
| VHB_DIN_Moun_x2.stl | 2 | 黑色/Electronics | Para colocar las placas electrónicas con cinta de doble cara |
| V0.2_Toolhead_PCB_Mount.STL | 1 | 红色 | Para colocar la placa que va en el toolhead |
| [a]_FS_Hotend_Mount_Dragon.stl | 1 | 红色/Toolheads/Hotend_Mounts/Fan_Saver | Este incluye un protector lateral para que no se mezcle el flujo de aire de los ventiladores |
| VORON_v0.2_stealth_chain_mount_v2.STL | 1 | 红色/三角支架 | Para la cama Kirigami |
| VORON_v0.2_stealth_chain_mount_5mm_spacer_v2.STL | 1 | 红色/三角支架 | Para la cama Kirigami |
| VORON_v0.2_stealth_wire_guide.stl_v2.STL | 1 | 红色/三角支架 | Para la cama Kirigami |

Y esto son mods que también imprimí, son opcionales, excepto el Kirigami Bed V3 Offset Nut que a mi parecer es casi obligatorio.
| Nombre | Link | Descripción |
|---|---|---|
| Cable Management Duct | [Cable Management Duct by ryandam](https://mods.vorondesign.com/details/YTmSPTcWpctfTKQj3bOPg) | Es meramente estético, solo para ordenar los cables, pero con la longitud de los cables que incluye el kit de formbot, casi que resulta molesto |
| No-Drop Nuts | [V0 No-Drop Nuts by zruncho](https://mods.vorondesign.com/details/XGjXJC3VQU76EBYB7Yg) | Sirve para que las tuercas queden más o menos fijas, lo cual ayuda en el montaje. Yo imprimí unas cuantas, pero no las he usado, la verdad, pero lo hubiese agradecido en ciertas partes, como en el montaje de los paneles laterales y demás |
| Stealth Handles | [Stealth Handles by MapleLeafMakers](https://mods.vorondesign.com/details/GHaVestXfFM0svkcJRpk2A) | Lo veo muy útil y queda bien estéticamente |
| Modesty Mesh | [Modesty Mesh by MapleLeafMakers](https://mods.vorondesign.com/details/zQkxgPQUJw3HY5IHALTYA) | Es solo estético, pero si no, se ve el cableado por el lado y me parece feo |
| Long Thumb Nut V0 | [V0 Long Thumb Nut by ardichoke](https://mods.vorondesign.com/details/JUp9cjJO3rcJWWEyhS3ag) | Si no, los normales son los [a]_Thumb_Nut_x3 en la Raiz |
| Voron V0 (V0.1) Kirigami Bed V3 Offset Nut | [Voron V0 (V0.1) Kirigami Bed V3 Offset Nut por DG \| Descargar modelo STL gratuito \| Printables.com](https://www.printables.com/model/151079-voron-v0-v01-kirigami-bed-v3-offset-nut) | Si no lo tienes, puede ser que la cama se te desplace en el eje Y y que los muelles no hagan fuerza y no puedas nivelarla correctamente. |

# Capítulo 1 – Frame

Antes de empezar, quería dar un apunte sobre los perfiles de aluminio: para el kit de Formbot los perfiles A y B son intercambiables (en el kit, todos vienen roscados), y lo mismo para C y H.

## 1.1. Limpieza de las guías lineales

Para saber cómo hacer este proceso, seguí los consejos tanto de Canuck creator (https://www.youtube.com/watch?v=UYvhYjkBFTY)  como de Mapple Leaf Makers (How to clean and lube your rails).
Lo primero es quitar el aceite con el que vienen las guías. Para ello, puse todas las guías en una bolsa zip y lo sumergí en alcohol isopropílico. Aunque luego me di cuenta de que la bolsa empezó a desteñir, así que las deje en un recipiente sumergidas en alcohol. Moví de vez en cuando las guías arriba y abajo para que penetrase bien el alcohol.

<img src="./imagenes/C1/imagen 1_1.jpg" width="50%"><img src="./imagenes/C1/imagen 1_2.jpg" width="50%">

Luego las sequé una a una con papel absorbente. Y para acabar de asegurarme que se evaporaba todo el líquido, lo puse en un secador de filamentos que tengo, una hora a 40ºC, aunque dejarlo a la intemperie un rato, también hubiese funcionado.

<img src="./imagenes/C1/imagen 1_3.jpg" width="50%"><img src="./imagenes/C1/imagen 1_4.jpg" width="50%">

Una vez bien secos, toca lubricar. Yo usé uno de los lubricantes recomendados por la guía de Voron, el Mobil EP 2. Intenté buscar alternativas, pero no había mucha diferencia de precio, así que preferí invertir en un buen lubricante. Para introducirlo, usé una jeringuilla de las típicas que puedes comprar en una farmacia. Si lo volviese hacer, usaría aguja fina para poder introducir directamente en los rodamientos, ya que lo que hice fue meter el lubricante a presión tal y como se ve en las imágenes, y al comprobar que salían por los rodamientos, entendí que estaban correctamente lubricados. Luego se mueve un poco a lo largo del carril para que se reparta bien el lubricante, y con papel absorbente limpiamos el excedente.

<img src="./imagenes/C1/imagen 1_5.jpg" width="50%"><img src="./imagenes/C1/imagen 1_6.jpg" width="50%">

Lo que me sorprendió es que después de lubricarlos, se movían más lentamente que cuando solo tenían el aceite, pero con los días, han ido yendo más finos.

## 1.2. Montaje del frame

Ahora aquí, ya sí que seguimos las instrucciones de la guía Voron. Solo iré comentando las partes con las que tuve dudas o problemas.
En el caso de poner las guías en los carriles, dentro de la carpeta tools de los stls, hay unas piezas para centrar las guías, la cual ayudan mucho para esa operación. En la guía especifican que no hace falta añadir tornillos y tuercas en todos los agujeros de la guía lineal, pero con la cantidad que vienen el kit, se podría hacer (yo no lo hice).

<img src="./imagenes/C1/imagen 1_7.jpg" width="80%">

En todo el montaje, solo partí un tornillo, que fue justamente en estos primeros pasos. Por suerte fue fácil de remplazar y no perdí ninguna pieza. En este caso diría que fue un tornillo defectuoso, ya que no apliqué fuerza excesiva y aún quedaba tramo para roscar. Pero nada, una anécdota.

<img src="./imagenes/C1/imagen 1_8.jpg" width="80%">

Luego seguí las instrucciones para el montaje del frame. Aunque en las fotos lo veáis encima de una plancha de goma, a la hora de montarlo y cuadrarlo todo lo hice en la encimera de la cocina para garantizar una superficie plana (podéis ver esta recomendación en el siguiente video: https://www.youtube.com/watch?v=GSg7RDLgYV0). Me compré unas llaves hexagonales Wera, para evitar gastar las cabezas de los tornillos, y la verdad es que han ido muy bien, pero la parte más larga no pasaban por los agujeros que atraviesan las extrusiones de aluminio, ya que tienen un recubrimiento de goma, así que tuve que usar la parte corta, siendo difícil para cuadrar el frame, teniéndolo apoyado en la encimera.
Aquí ya está parte del frame montado con los raíles a 58 mm del borde.

<img src="./imagenes/C1/imagen 1_9.jpg" width="80%">

Luego viene la parte de poner los insertos metálicos en las piezas impresas. Yo utilicé el soldador que tengo en casa y le puse una temperatura de 255ºC. La verdad es que encajaban perfectamente en las piezas impresas, no tuve que retocar nada.

<img src="./imagenes/C1/imagen 1_10.jpg" width="80%">

Ahora toca montar la parte de la cama kirigami. En esta parte me detendré un poco más, porque para mí, la documentación es algo escasa o fragmentada, aunque la verdad es que es bastante más simple que la que aparece en el manual oficial.

## 1.3. Kirigami bed

En el manual de Voron, no hay una explicación detallada de cómo se monta la cama Kirigami, pero sí que recomienda ir a ver el github de
christophmuellerorg (GitHub - christophmuellerorg/voron_0_kirigami_bed · GitHub). Personalmente también creo que el video de Tommy Houghton ([I Wish I Built a Voron Sooner](https://www.youtube.com/watch?v=V_P36ezmop4)) puede resolver muchas dudas, ya que monta el mismo kit de Formbot.
Como ya he dicho, es bastante simple. Se pone los insertos en las piezas que muestro abajo.

<img src="./imagenes/C1/imagen 1_11.jpg" width="80%">

Y luego se colocan en lo que es la cama Kirigami:

<img src="./imagenes/C1/imagen 1_12.jpg" width="80%">

Junto con el “cable chain” para los cables.

<img src="./imagenes/C1/imagen 1_13.jpg" width="80%">

A la hora de juntar la cama con las guías lineales (pg. 44 de la guía) acordaros de usar el nutlocker para que no se aflojen los tornillos.
Y acabando este capítulo, la impresora nos queda como la imagen de abajo:

<img src="./imagenes/C1/imagen 1_14.jpg" width="80%">

Para mi gusto, la cama ha quedado muy dura, ya que para que baje, tengo que hacer cierta fuerza, cuando esperaría que casi cayera por su propio peso. [SrgntBallistic](https://github.com/SrgntBallistic) ya puso en su github este problema, pero en el momento de montarlo, me pareció que no era muy importante. Por el momento, no he notado defectos en las impresiones.
