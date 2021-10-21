# Transformaciones con Blender

A continuación, se aplican las transformaciones de traslación, rotación y escalamiento a un cubo que se agrega en el programa Blender.

Blender es la suite de creación 3D gratuita y de código abierto. Es compatible con la totalidad de la canalización 3D: modelado, montaje, animación, simulación, renderizado, composición y seguimiento de movimiento, incluso edición de video y creación de juegos.

El primer paso es crear un objeto predeterminado que ofrece el programa para agregarlo en el espacio de trabajo como se muestra en la siguiente captura.

Figura 1
Cubo predeterminado agregado al espacio de trabajo de Blender.

![image](https://user-images.githubusercontent.com/71055467/138249298-b0d66b2c-66b3-4edd-b473-68e3dee112d6.png)

Para poder abrir una consola en donde podemos observar toda la información que se va realizando en tiempo real en el objeto duplicamos el espacio de trabajo pero elegimos el tipo de editor "Info", así como se muestra en la siguiente figura.

Figura 2
En la ventana izquierda se muestra la información del Layout del lado derecho, en el lado derecho se muestra el objeto.

![image](https://user-images.githubusercontent.com/71055467/138250169-3d770fcd-dac4-408a-a26b-73d0a5c9cfe8.png)

En el siguiente paso, vamos a trasladar el objeto a donde deseamos, para ello seleccionamos el cubo y utilizamos el atajo del teclado, presionamos la tecla "g" y si movemos el mouse también el cubo se mueve y sólo presionamos clic izquierdo para dejar la imagen estática. En la siguiente captura se muestran las posiciones en los ejes tanto en x, y y z, asimismo en la ventana izquierda se muestra lo que se hizo, y también se muestra la nueva posición del objeto.

Figura 3
Nueva posición del objeto aplicando la traslación.

![image](https://user-images.githubusercontent.com/71055467/138252980-7743bd09-0185-43a9-8b2e-99fbad577fc2.png)

Ahora aplicamos la rotación al cubo, de la misma forma que en la anterior transformación, seleccionamos el objeto y presionamos la tecla g y después de eso, aplicamos la tecla r, y rotamos el cubo los grados que queramos. A continuación, se muestra lo que se ha descrito.

Figura 3
Rotación aplicada al cubo.

![image](https://user-images.githubusercontent.com/71055467/138253998-f5134801-0f44-47de-94ba-0cbd48fc28c1.png)

La última transformación se trata del escalamiento, en este caso aplicamos la tecla g y después la tecla s, y si movemos el mouse se hará grande el cubo o bien se hace más pequeño. El resultado de las posiciones se muestra a continuación. 

Figura 4
Escalamiento aplicado al cubo.

![image](https://user-images.githubusercontent.com/71055467/138254855-7c462ffe-d618-4dba-911b-9b903c46b6f0.png)

Ahora si necesitamos aplicar esta misma transformación pero utilizando la terminal de Blender, agregamos una nueva ventana pero elegimos el tipo de edición "Text Editor" e importamos la librería bpy que es usada en este programa. Ahora sí lo que hacemos es copiar las últimas tres acciones que se refieren a las transformaciones que están en la ventana del lado izquierdo y lo pegamos en la terminal, de la siguiente forma.

Figura 5
Transformaciones hechas desde el terminal.

![image](https://user-images.githubusercontent.com/71055467/138256576-e7e46ce9-b924-4af9-a2fb-8096b82eb321.png)

Como las sentencias no se muestran completa, a continuación se muestra el código completo que se pegó en la terminal.

-------------------------------------------------------------------------------------------------------------------------------------------
import bpy

bpy.ops.transform.translate(value=(1.24275, 3.76519, 0.771751), orient_type='GLOBAL', orient_matrix=((1, 0, 0), (0, 1, 0), (0, 0, 1)), orient_matrix_type='GLOBAL', mirror=True, use_proportional_edit=False, proportional_edit_falloff='SMOOTH', proportional_size=1, use_proportional_connected=False, use_proportional_projected=False)

bpy.ops.transform.rotate(value=-1.00459, orient_axis='Z', orient_type='VIEW', orient_matrix=((0.410029, 0.911976, -0.0132648), (-0.401743, 0.193644, 0.895045), (0.818828, -0.361665, 0.445779)), orient_matrix_type='VIEW', mirror=True, use_proportional_edit=False, proportional_edit_falloff='SMOOTH', proportional_size=1, use_proportional_connected=False, use_proportional_projected=False)

bpy.ops.transform.resize(value=(1.869, 1.869, 1.869), orient_type='GLOBAL', orient_matrix=((1, 0, 0), (0, 1, 0), (0, 0, 1)), orient_matrix_type='GLOBAL', mirror=True, use_proportional_edit=False, proportional_edit_falloff='SMOOTH', proportional_size=1, use_proportional_connected=False, use_proportional_projected=False)

-------------------------------------------------------------------------------------------------------------------------------------------

Ahora si corremos el script anterior desde la terminal, se muestra el resultado en la siguiente figura.

Figura 6
Correr el script.

![image](https://user-images.githubusercontent.com/71055467/138257458-5928ce28-1c07-4804-ad19-8ead13cb1d8b.png)

Figura 7
Resultado aplicando la misma transformación pero en la terminal de Blender.

![image](https://user-images.githubusercontent.com/71055467/138258160-8c93230a-a7e6-4e00-a8a8-e01fd48c0b04.png)


