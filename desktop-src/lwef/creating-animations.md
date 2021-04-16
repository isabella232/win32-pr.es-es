---
title: Creación de animaciones
description: Creación de animaciones
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16c460908e7c782054a3f62ece87d01e7c9a817
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104563022"
---
# <a name="creating-animations"></a>Creación de animaciones

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Para empezar a crear animaciones para el carácter, seleccione el icono **animaciones** en el árbol. Esto muestra la página de **propiedades** con la configuración predeterminada para todas las animaciones. Puede modificar el tamaño de los fotogramas, la duración predeterminada de los fotogramas y la configuración de la paleta de colores en la página **propiedades** .

### <a name="setting-your-characters-frame-size"></a>Establecer el tamaño del fotograma del carácter

El alto y el ancho del marco de animación deben permanecer constantes a lo largo de toda la definición de caracteres (es decir, para todas las animaciones de ese carácter). Aunque puede cambiar el tamaño del marco de su configuración predeterminada (128 x 128 píxeles), las imágenes mostradas en el editor se escalarán para ajustarse al tamaño de presentación predeterminado. Si cambia la configuración de trama predeterminada, puede mostrar el tamaño completo y sin escala del marco seleccionando **Abrir ventana de marco** en el menú **edición** .

### <a name="setting-your-characters-palette"></a>Establecer la paleta del carácter

De forma predeterminada, el editor usa la primera imagen de mapa de bits que se carga para establecer la paleta de colores predeterminada del carácter, los colores que determinan cómo aparece el carácter y establece el color de la posición de la<sup>paleta 11 como</sup> color de transparencia. Sin embargo, puede establecer la paleta y la transparencia explícitamente en el grupo **información de paleta** . Esto le permite especificar un archivo de imagen para utilizarlo en la paleta. Puede especificar uno de los archivos de imagen de animación o cualquier archivo gráfico. El archivo de paleta que especifique debe ser un archivo de color de 8 bits (256). Una vez cargado, use el botón **Cambiar configuración** para cambiar el color de transparencia.

La paleta de colores del carácter no debe reasignar los colores estándar del sistema. El editor reservará automáticamente la paleta de colores del sistema cuando se muestren imágenes. Además, todas las imágenes de animación deben usar la misma paleta de colores y el mismo color de transparencia. Esto es muy importante. Si no es así, puede ver la reasignación de color de las imágenes al cargarlas en el editor.

Aunque puede establecer la paleta de colores para el carácter, en los sistemas Windows en los que las propiedades de presentación se establecen en una paleta de colores de 8 bits (256), el color del carácter estará sujeto a la paleta del sistema actual. Dado que las aplicaciones pueden cambiar la paleta del sistema, es posible que el carácter no aparezca con la configuración de color correcta. Aunque no hay ninguna manera de evitar esto, puede reducir el efecto limitando el número de colores que usa y estableciendo la paleta del carácter en función de la paleta utilizada por la aplicación que lo impulsa. Por ejemplo, si está desarrollando un carácter que se va a utilizar con páginas web, puede establecer la paleta del carácter mediante la paleta de medios tonos de Microsoft Internet Explorer. Para capturar la paleta del explorador, haga clic con el botón derecho en una imagen de una página web y elija el comando **guardar imagen como** y elija **mapa de bits** en la opción **Guardar como tipo** y, a continuación, haga clic en **Guardar**. Para optimizar los archivos de imagen de animación en un archivo de paleta específico, es posible que desee usar un producto como DeBabelizer de equilibrio.

### <a name="creating-a-new-animation"></a>Crear una nueva animación

Después de determinar la configuración de la animación global, puede empezar a crear animaciones. Para crear una animación nueva, elija **nueva animación** en el menú **edición** o en el botón **nueva animación** de la barra de herramientas. Esto agrega un nuevo icono de animación en el árbol en el icono **animaciones** y asigna el nuevo icono a un nombre predeterminado. Puede cambiar el nombre de la animación escribiendo en el campo Nombre de la **animación** . Tenga en cuenta que los nombres de animación dentro de una definición de caracteres deben ser únicos. Además, evite usar caracteres en el nombre que no sean caracteres válidos para los nombres de archivo.

### <a name="adding-frames"></a>Agregar marcos

Cada animación se compone de fotogramas. Para crear un nuevo fotograma para la animación, elija **nuevo fotograma** en el menú **edición** o en la barra de herramientas. Esto agrega un nuevo icono de marco al árbol bajo el icono de animación y muestra tres páginas con pestañas. La página **General** incluye controles que permiten cargar y ajustar una imagen para el marco. También incluye un área de presentación para la apariencia del marco.

![Captura de pantalla que muestra el panel imagen con el nombre de archivo, la ruta de acceso y la posición.](images/f2charflame.gif)

Un marco puede contener una o varias imágenes. Para definir una imagen para un marco, haga clic en el botón **Agregar archivo de imagen** justo encima del cuadro de lista **imágenes** . Aparece el cuadro de diálogo **seleccionar archivos de imagen** , que permite seleccionar un archivo de imagen de mapa de bits.

![Captura de pantalla que muestra un archivo de imagen seleccionado en el explorador de archivos.](images/f3chardialbox.gif)

Seleccione el archivo que desea cargar, elija **abrir** y la imagen aparecerá en la pantalla del marco en la página **General** . El editor acepta imágenes almacenadas como formato de mapa de bits de Windows de 1 bit (monocromo), de 4 bits o de 8 bits, o como formato GIF.

Puede usar los cuatro botones de flecha situados debajo de la imagen en el cuadro **posición** para ajustar el aspecto de la imagen dentro del marco. Si la imagen es mayor que el tamaño del fotograma, solo se mostrará la parte de la imagen que aparece dentro del marco. Si aumenta el tamaño de los fotogramas, es posible que la imagen se escale para ajustarse al área de visualización del editor.

También puede mostrar un marco seleccionando **Abrir ventana de marco** en el menú **edición** . Esto muestra el marco actual en una ventana independiente sin escalar las imágenes cargadas en el marco. El tamaño inicial de esta ventana se basa en la configuración de alto y ancho del fotograma. Puede cambiar su tamaño más pequeño, pero no mayor. La ventana marco refleja los cambios que se realizan mediante los controles del editor y también permite ver el marco mientras se visualizan las demás páginas de propiedades.

![Captura de pantalla que muestra el panel posición.](images/f4charposctrl.gif)

Puede crear un marco a partir de varias imágenes. Cada vez que seleccione el botón **Agregar imagen** y elija otra imagen, la imagen se agregará a la lista y al área de visualización de la imagen. También puede agregar varias imágenes seleccionando más de un archivo. Presione Mayús o CTRL mientras hace clic en el cuadro de diálogo **seleccionar archivos de imagen** y, a continuación, elija **abrir**. Los botones **subir** y **bajar** sobre el cuadro de lista **imágenes** mueven una imagen seleccionada en el orden de presentación (orden z) del marco. También puede mover las imágenes arrastrándolas dentro de la lista. Al seleccionar una imagen en la lista y hacer clic en el botón **eliminar** , se quita una imagen. Para cambiar una imagen que ha cargado en otro archivo de imagen, puede hacer clic en el nombre de archivo para editarlo directamente o usar el botón **...** (puntos suspensivos) para abrir el cuadro de diálogo **seleccionar archivos de imagen** y seleccionar un archivo diferente.

![Captura de pantalla que muestra el botón de puntos suspensivos.](images/f5charell.gif)

Puede usar el cuadro de texto **duración** para establecer la duración del marco; es decir, cuánto tiempo se mostrará el fotograma. Si un fotograma no tiene ninguna imagen y la duración de cero, el marco no se mostrará cuando se reproduzca la animación.

También puede especificar un archivo de efecto de sonido que se reproducirá cuando se muestre el fotograma. Si tiene previsto cargar el carácter desde un servidor Web, es posible que desee comprimir el archivo de efecto de sonido para minimizar el tiempo de carga. Después, puede especificar el archivo de sonido comprimido en el editor de caracteres del agente. Además, evite el uso de un efecto de sonido con una duración mayor que la duración de la animación y, en especial, evite un efecto sonoro en bucle, ya que los servicios de animación de agente de Microsoft no envían un evento de animación completa hasta que se completa el sonido. Evite también la especificación de un efecto sonoro para cualquier animación que asigne a los Estados de **escucha** o **audición** , ya que esto interfiere con la entrada de voz. Por último, aunque puede incluir más de un efecto de sonido en una animación, evite colocarlos para que se superpongan, ya que esto puede afectar al tiempo de la animación. Además, tenga en cuenta que los efectos sonoros pueden reproducirse a diferentes velocidades según el hardware del usuario.

Para agregar fotogramas a la animación, vuelva a elegir el comando **nuevo marco** y siga el mismo procedimiento. Como opción, también puede cargar varias imágenes y generar automáticamente nuevas tramas para ellas. Para usar esta característica, elija **nuevo fotogramas a partir de imágenes** en el menú **edición** . Los marcos se crearán en orden alfabético en función de los nombres de archivo de imagen. Cuando haya terminado de definir todos los fotogramas de la animación, puede volver a elegir el nuevo comando de **animación** para iniciar una nueva animación.

Hay otras maneras de agregar fotogramas a animaciones y de desplazar fotogramas dentro o entre animaciones. Puede seleccionar otro fotograma (de la misma animación u otra), elegir **cortar** o **copiar** y, a continuación, seleccionar la animación o un fotograma en esa animación y elegir **pegar**. También puede arrastrar un fotograma de una animación a otra. Si arrastra dentro de una animación, la acción mueve el marco. Si arrastra a otra animación, copia el marco. Al arrastrar a un fotograma anterior en la misma animación, se inserta el fotograma delante del fotograma al que se arrastra. Al arrastrar a un fotograma siguiente, se coloca después del fotograma en el que se arrastra. Si arrastra un fotograma con el botón secundario del mouse, al soltar el botón se muestra un menú emergente con las opciones de transferencia.

También puede crear una animación copiando una animación existente (seleccione la animación y elija **copiar**) y seleccione el icono **animaciones** u otro icono de animación y elija **pegar**. El editor crea automáticamente un nuevo nombre para la animación, aunque puede cambiar el nombre.

### <a name="branching"></a>Bifurcación

Al crear un fotograma, también puede definir qué fotograma se reproducirá a continuación. De forma predeterminada, el siguiente fotograma que se reproduce en la secuencia de animación siempre es el siguiente fotograma en el orden z. Sin embargo, al elegir la página de **bifurcación** , puede establecer la probabilidad de hasta tres fotogramas que el servidor pueda reproducir. Escriba el porcentaje de probabilidad y el número de marco de destino en los campos correspondientes. Puede especificar la bifurcación incluso para fotogramas que no tienen imágenes y cuya duración está establecida en cero. Esto le permite crear una bifurcación sin mostrar primero una imagen determinada.

![Captura de pantalla que muestra la página ' bifurcación '.](images/f6charbranch.gif)

Puede usar la característica de bifurcación para crear animaciones que se recorrerán indefinidamente. Sin embargo, tenga en cuenta que cuando se reproduce una animación de bucle, no se reproducirán otras animaciones de la cola del carácter hasta que un evento (por ejemplo, un usuario que presione la tecla de invalidación o la aplicación cliente que llama al método [**Stop**](stop-method.md) ) detenga la animación de bucle. Por lo tanto, considere cuidadosamente el contexto en el que se utilizará la animación antes de crear una animación de bucle.

La página de bifurcación también le permite crear una bifurcación de salida. Una rama de salida es una rama a un fotograma que la animación realizará cuando se detenga la animación y antes de que se reproduzca la animación siguiente. La definición de ramas de salida le permitirá moverse sin problemas durante la transición de una animación a otra. La bifurcación de salida no debe crear un bucle circular, pero debe poder salir hasta el último fotograma de la animación.

No es necesario proporcionar una rama de salida para cada fotograma; sin embargo, si no lo hace, la animación seguirá la rama normal del fotograma. Si el marco no tiene ninguna rama explícita, la animación se bifurca automáticamente en el marco que le sigue. Por ejemplo, si se ramifica desde el fotograma 3 al marco 1 y el marco 1 no tiene ninguna otra bifurcación (rama normal o de salida), el marco 1 se ramificará en el fotograma 2. Si el fotograma 2 no tiene ninguna bifurcación, la animación se ramificará en el fotograma 3 y tendrá un bucle circular. En su lugar, puede crear una bifurcación del fotograma 3 al marco 1 y, a continuación, establecer la rama de salida del marco 1 en cualquier fotograma que esté después del fotograma 3 y que normalmente continúe en el último fotograma de la animación.

En ocasiones, es posible que necesite crear un marco final explícito de una animación que no se reproduzca de forma visible, pero que proporcione un final de la animación. Por ejemplo, debe salir de la animación, pero salir hasta el último fotograma no sería adecuado. Para ello, puede crear un marco de duración en blanco y cero como último fotograma de la animación. Esto permite que la animación se reproduzca normalmente a través del último fotograma de la animación y también le permite proporcionar un punto de salida final para la bifurcación de salida.

### <a name="previewing-an-animation"></a>Obtener una vista previa de una animación

Puede obtener una vista previa de la animación en el editor de caracteres del agente eligiendo el comando **vista previa** en el menú **edición** o el botón vista previa de la barra de herramientas. Esto reproduce la animación, incluidas las ramas y los efectos sonoros, a partir del marco seleccionado actualmente. Se restablece en el marco seleccionado actual cuando se completa la animación. Para reproducir la animación completa, vaya a la vista de árbol, seleccione el icono de la animación o el primer fotograma de la animación y elija el comando **vista previa** . El editor anima los marcos en la página **General** . Para detener la vista previa antes de finalizar, elija el comando **detener vista previa** . El comando de **vista previa** cambia automáticamente a **detener vista previa** mientras se reproduce la vista previa.

También puede obtener una vista previa de la bifurcación de salida eligiendo el comando **vista previa salir de la bifurcación** en el menú **edición** o en la barra de herramientas. Permite probar el modo en que la bifurcación de salida aparecerá desde cualquier fotograma específico.

### <a name="assigning-speaking-overlays"></a>Asignar superposiciones de habla

Puede definir un carácter para que hable durante el último fotograma de la animación. En este marco, elija la página **superposición** . Esta página le permite cargar y asignar archivos de imagen de la boca a las posiciones estándar de la boca compatible con el agente de Microsoft. Haga clic en el botón **Agregar imagen** y seleccione la imagen en el cuadro de diálogo. También puede seleccionar varias imágenes y el editor cargará y asignará las imágenes a partir de la posición de la boca seleccionada. Haga clic en los botones **subir** y **bajar** o arrastre una entrada para cambiar una asignación de imagen en la lista. Haga clic en el botón **eliminar** para quitar una imagen. También puede editar el nombre de ruta de acceso de un archivo asignado si hace clic en su entrada en la lista y vuelve a escribir su nombre de archivo, o si elige el botón de **puntos suspensivos** para mostrar el cuadro de diálogo **seleccionar archivos de imagen** .

![Captura de pantalla que muestra la página "superposiciones" con un archivo seleccionado.](images/f7charover.gif)

Las superposiciones de la boca deben caber dentro del contorno del marco base en el que aparecerán. Si no es así, se recortarán en el fotograma Base.

Si desea que el carácter hable con su boca fuera del marco base, por ejemplo, cuando el carácter se hable hacia los lados, cree primero el fotograma Base con el encabezado del carácter (o el área que se moverá como el carácter habla) como su imagen superior. A continuación, defina las superposiciones de la boca para reemplazar la imagen y establezca la opción **reemplazar imagen superior de fotogramas base** . También puede usar el botón **establecer todo** para establecer esta opción para todas las superposiciones de la boca en el marco.

### <a name="assigning-a-return-animation"></a>Asignar una animación de devolución

Para crear una transición suave de una animación a la siguiente, diseñe las secuencias de animación para que comiencen y terminen con una imagen neutra. Para obtener más información, vea [**diseñar caracteres para el agente de Microsoft**](designing-characters-for-microsoft-agent.md). Sin embargo, esto no significa que todas las animaciones deben terminar en la posición neutra. Puede animar un carácter a través de una secuencia de fotogramas, hacer que hable en el último fotograma y crear una animación independiente y complementaria que devuelva el carácter a la posición neutra. Esta animación complementaria se denomina animación devuelta.

Puede definir una animación de devolución creando una animación explícita para este fin. También puede crear una animación de devolución mediante la bifurcación de salida que defina dentro de la animación. Para asignar una animación de devolución, seleccione la animación en el árbol y, a continuación, seleccione la animación de retorno que creó o use la bifurcación de salida en la lista desplegable devolver animación de la página de propiedades.

La creación y asignación de una animación de devolución tiene una ventaja adicional: cuando el servidor recibe una solicitud para reproducir otra animación, intentará reproducir la animación de retorno de la última animación que reproduzca, si se asigna una animación de devolución. Esto garantiza una transición sin problemas. Si una animación comienza y termina en la posición neutra, no es necesario definir una animación devuelta. Del mismo modo, si desea controlar las transiciones de una animación a otra, es posible que no necesite asignar una animación de devolución.

### <a name="assigning-animations-to-states"></a>Asignar animaciones a Estados

Los servicios de animación de agente de Microsoft reproducen animaciones automáticamente cuando la aplicación cliente de hospedaje usa ciertos métodos. Por ejemplo, cuando una aplicación llama a los métodos [**moveTo**](moveto-method.md) y [**GestureAt**](gestureat-method.md) , el servidor determina automáticamente dónde se muestra el carácter y reproduce una animación adecuada. Del mismo modo, el agente de Microsoft reproduce automáticamente animaciones inactivas cuando el usuario no ha interactuado con el carácter durante varios segundos. Estas condiciones, cuando el servidor reproduce automáticamente animaciones en el nombre de una aplicación, se denomina *Estados*. Sin embargo, para que el servidor sepa qué animación reproducir, debe asignar animaciones a estos Estados.

Para asignar una animación o animaciones a un estado, cree la animación adecuada, expanda la entrada Estados en la vista de árbol de la ventana del editor y seleccione el icono de estado. La lista de animaciones que ha creado aparece en un cuadro de lista en el lado derecho de la ventana. Compruebe la animación que desea asignar a este estado. Tenga en cuenta que puede asignar más de una animación al mismo estado. Esto permite al servidor seleccionar aleatoriamente diferentes animaciones para el estado. La asignación de una animación a un estado no impide que una animación reproduzca esa animación directamente.

También puede asignar una animación a un estado seleccionando la entrada de la animación en el árbol. En el cuadro de lista **asignar a estado** de la página **propiedades** se muestran los Estados. Active la casilla del estado al que va a asignar la animación.

El editor no admite la creación de Estados adicionales, ya que los Estados solo se aplican a situaciones en las que el servidor debe reproducir una animación automáticamente en nombre de la aplicación cliente. Por lo tanto, no hay ninguna ventaja en la definición de su propio estado. Si es necesario, puede reproducir cualquier animación explícitamente mediante el método [**Play**](play-method.md) .

### <a name="saving-your-character-definition"></a>Guardar la definición de caracteres

Para guardar el archivo de definición del carácter, seleccione el comando **Guardar** en el menú **archivo** o el botón **Guardar definición de caracteres** en la barra de herramientas. Si desea guardar el archivo de definición de caracteres con un nuevo nombre, elija el comando **Guardar como** en el menú **archivo** . El editor guarda la definición editable de un carácter como una definición de caracteres del agente (. ACD). También puede editar este formato de archivo de texto autodocumentado con la mayoría de editores de texto y aplicaciones de procesamiento de textos.

### <a name="printing-your-character-definition"></a>Impresión de la definición de caracteres

Para imprimir la definición del carácter, elija el comando **Imprimir** del menú **archivo** o el botón **Imprimir** de la barra de herramientas. Para establecer las propiedades de la salida impresa, elija el comando **Configurar página** y elija la configuración antes de seleccionar el comando **Imprimir** .

### <a name="building-a-character"></a>Compilar un carácter

Cuando haya terminado de crear las animaciones, el carácter y las imágenes se deben compilar en un formato especial que el agente de Microsoft use para cargar estos datos. Para generar un carácter, seleccione el comando compilar carácter en el menú **archivo** o en la barra de herramientas. Si tiene ediciones sin guardar en el archivo de definición de caracteres, el editor guarda el archivo de definición antes de mostrar el cuadro de diálogo **generar carácter** .

![Captura de pantalla que muestra la ventana ' carácter de compilación ' con un archivo seleccionado.](images/f8charbldg.gif)

El editor de caracteres del agente propondrá automáticamente un nombre de archivo basado en el nombre de archivo de la definición de caracteres. El cuadro de diálogo generar carácter también incluye una lista desplegable para que pueda elegir entre compilar el carácter como un solo archivo de almacenamiento (. ACS) o como varios archivos. Si elige el último, el editor crea un. Archivo ACF que incluye los datos del carácter y un. El archivo ACA para cada animación que creó. Si planea instalar y acceder a un carácter almacenado en el mismo equipo que la aplicación cliente, normalmente elegiría el formato de archivo estructurado único. Este formato proporciona una instalación y un acceso sencillos y eficientes al carácter. Sin embargo, si se va a tener acceso al carácter desde un servidor Web mediante el protocolo HTTP, cree el carácter con el. Formato de archivo ACF (individual). Esta última estructura de archivos permite que un script de página web Cargue archivos de animación individuales y almacene los datos en la memoria caché de archivos del explorador del usuario. Proporciona un acceso más eficaz a través de la web, ya que los datos de animación se pueden descargar según sea necesario, en lugar de requerir al usuario que espere a que se descargue todo el conjunto de animaciones al mismo tiempo. Además, dado que los datos del carácter se almacenan en la memoria caché del explorador, el espacio de archivo se puede reclamar automáticamente.

Aunque también puede descargar datos de caracteres (ya sea como un único archivo estructurado o varios archivos) desde un servidor web e instalar en cualquier otro lugar del equipo de un usuario, este método requiere las provisiones de seguridad para la descarga e instalación. Como resultado, la API del agente de Microsoft no incluye compatibilidad para la instalación descargable de un carácter excepto en la memoria caché del explorador. Sin embargo, todavía puede admitir este escenario si crea su propio control de instalación y lo distribuye según las convenciones de seguridad adecuadas. Para obtener más información, vea el kit de desarrollo de software cliente de Microsoft Internet.

La opción comprimir permite establecer si los datos de caracteres se comprimen. Normalmente, querrá establecer esta opción para compactar los datos de caracteres, aunque la creación de un carácter con los datos compactos tarda más tiempo.

Una vez que se crea un carácter, las compilaciones posteriores serán más rápidas si se compila el carácter en la misma ubicación del directorio. El editor de caracteres comprueba y copia automáticamente los archivos que no han cambiado y vuelve a compilar los datos que se han editado.

Si el editor detecta errores en el archivo de caracteres durante la generación del carácter, escribe la información en un archivo de registro y muestra un cuadro de mensaje. Puede elegir ver el archivo de registro u omitirlo y leerlo más adelante con un editor de texto. Sin embargo, tenga en cuenta que el editor sobrescribirá el archivo de registro la próxima vez que cree un archivo de caracteres.

### <a name="editing-an-existing-character"></a>Editar un carácter existente

Para editar un carácter existente, elija **abrir** en el menú **archivo** y seleccione el archivo de definición del carácter (. ACD) en el cuadro de diálogo resultante y elija Abrir. El archivo se cargará en el editor. Tenga en cuenta que no puede cargar archivos de caracteres compilados (. ACS,. ACF o. ACA) con el editor.

Dado que el archivo de definición del carácter (. ACD) es un archivo de texto. también puede editar la definición de un carácter abriendo el archivo con un editor de texto o un programa de procesamiento de textos. Sin embargo, al completar los cambios, asegúrese de guardar el archivo en su formato original antes de cargarlo en el editor de caracteres para la compilación.

 

 




