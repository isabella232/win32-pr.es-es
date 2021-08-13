---
title: Creación de animaciones
description: Creación de animaciones
ms.assetid: 6d5c3c61-b3f2-4505-aa43-b6d001c444a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed5955e57af405451def3208902678d3d6a0ffb9857cc719bfe100dbbd2447f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118752362"
---
# <a name="creating-animations"></a>Creación de animaciones

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Para empezar a crear animaciones para el carácter, seleccione el **icono Animaciones** en el árbol. Se muestra la **página Propiedades** con la configuración predeterminada para todas las animaciones. Puede modificar el tamaño del marco, la duración predeterminada del fotograma y la configuración de la paleta de colores en la **página** Propiedades.

### <a name="setting-your-characters-frame-size"></a>Establecer el tamaño del marco del carácter

El alto y el ancho del fotograma de animación deben permanecer constantes en toda la definición de caracteres (es decir, para todas las animaciones de ese carácter). Aunque puede cambiar el tamaño del fotograma de su configuración predeterminada (128 x 128 píxeles), las imágenes que se muestran en el editor se escalarán para ajustarse al tamaño de pantalla predeterminado. Si cambia la configuración de marco predeterminada, puede mostrar el tamaño completo y no escalado del marco eligiendo **Abrir** ventana de marco en el **menú** Editar.

### <a name="setting-your-characters-palette"></a>Establecer la paleta de caracteres

De forma predeterminada, el Editor usa la primera imagen de mapa de bits que se carga para establecer la paleta<sup></sup> de colores predeterminada del carácter, los colores que determinan cómo aparece el carácter y establece el color en la posición de la 11ª paleta como color de transparencia. Sin embargo, puede establecer la paleta y la transparencia explícitamente en el grupo **Información de paleta.** Esto le permite especificar un archivo de imagen que se usará para la paleta. Puede especificar uno de los archivos de imagen de animación o cualquier archivo gráfico. El archivo de paleta que especifique debe ser un archivo de color de 8 bits (256). Una vez cargado, use el **botón Cambiar** configuración para cambiar el color de transparencia.

La paleta de colores del carácter no debe reasignar los colores estándar del sistema. El editor reservará automáticamente la paleta de colores del sistema al mostrar imágenes. Además, todas las imágenes de animación deben usar la misma paleta de colores y el mismo color de transparencia. Esto es muy importante. Si no es así, es posible que vea la remapping de colores de las imágenes al cargarlas en el editor.

Aunque puede establecer la paleta de colores para el carácter, en sistemas de Windows donde las propiedades mostrar están establecidas en una paleta de colores de 8 bits (256), el color del carácter estará sujeto a la paleta del sistema actual. Dado que las aplicaciones pueden cambiar la paleta del sistema, es posible que el carácter no aparezca con la configuración de color correcta. Aunque no hay ninguna manera de evitarlo, puede reducir el efecto limitando el número de colores que usa y estableciendo la paleta del carácter en función de la paleta usada por la aplicación que impulsa el carácter. Por ejemplo, si está desarrollando un carácter para usarlo con páginas web, puede establecer la paleta de caracteres mediante la paleta de semitonos de Microsoft Internet Explorer. Para capturar la paleta del explorador, haga clic con el botón  derecho en una imagen de  una página web y elija el comando Guardar imagen como y seleccione Mapa de bits en la opción Guardar como tipo y, a continuación, haga clic en **Guardar.**  Para optimizar los archivos de imagen de animación en un archivo de paleta específico, es posible que quiera usar un producto como Equilibrios DeBabelizer.

### <a name="creating-a-new-animation"></a>Crear una nueva animación

Una vez que haya determinado la configuración global de la animación, puede empezar a crear animaciones. Para crear una animación, elija **Nueva animación** en el **menú** Editar o en el botón **Nueva animación** de la barra de herramientas. Esto agrega un nuevo icono de animación en el árbol bajo el **icono Animaciones** y asigna al nuevo icono un nombre predeterminado. Puede cambiar el nombre de la animación escribiendo en el **campo Nombre de** animación. Tenga en cuenta que los nombres de animación dentro de una definición de caracteres deben ser únicos. Además, evite usar caracteres en el nombre que no sean caracteres válidos para los nombres de archivo.

### <a name="adding-frames"></a>Agregar fotogramas

Cada animación se compone de fotogramas. Para crear un nuevo marco para la animación, elija **Nuevo** marco en el **menú** Editar o en la barra de herramientas. Esto agrega un nuevo icono de marco al árbol bajo el icono de animación y muestra tres páginas con pestañas. La **página General** incluye controles que le permiten cargar y ajustar una imagen para el marco. También incluye un área de presentación para la apariencia del fotograma.

![Captura de pantalla que muestra el panel Imagen con el nombre de archivo, la ruta de acceso y la posición.](images/f2charflame.gif)

Un marco puede contener una o varias imágenes. Para definir una imagen para un marco, haga clic en **el botón Agregar** archivo de imagen situado justo encima del cuadro de **lista** Imágenes. Se **muestra el cuadro de diálogo** Seleccionar archivos de imagen, que permite seleccionar un archivo de imagen de mapa de bits.

![Captura de pantalla que muestra un archivo de imagen seleccionado en Explorador de archivos.](images/f3chardialbox.gif)

Seleccione el archivo que desea cargar, elija **Abrir** y la imagen aparecerá en la pantalla de marco de la **página General.** El editor acepta imágenes almacenadas como formato de mapa de bits de 1 bit (monocromo), de 4 bits o de 8 Windows mapa de bits, o como formato GIF.

Puede usar los cuatro botones de  flecha debajo de la imagen en el cuadro Posición para ajustar la apariencia de la imagen dentro del marco. Si la imagen es mayor que el tamaño del marco, solo se mostrará la parte de la imagen que aparece dentro del marco. Si aumenta el tamaño del marco, la imagen se puede escalar para ajustarse al área de presentación del editor.

También puede mostrar un marco si elige Abrir ventana **de marco** en el **menú** Editar. Esto muestra el marco actual en una ventana independiente sin escalar las imágenes cargadas en el marco. El tamaño inicial de esta ventana se basa en la configuración de alto y ancho del marco. Puede cambiar su tamaño más pequeño, pero no mayor. La ventana Marco refleja los cambios realizados mediante los controles del Editor y también le permite ver el marco mientras ve sus otras páginas de propiedades.

![Captura de pantalla que muestra el panel Posición.](images/f4charposctrl.gif)

Puede crear un marco a partir de varias imágenes. Cada vez que se selecciona **el botón Agregar** imagen y se elige otra imagen, la imagen se agrega a la lista y al área de presentación de la imagen. También puede agregar varias imágenes seleccionando más de un archivo. Presione MAYÚS o CTRL mientras hace clic en el **cuadro de** diálogo Seleccionar archivos de imagen y, a continuación, elija **Abrir.** Los **botones Subir** y  **Bajar** situados encima del cuadro de lista Imágenes mueven una imagen seleccionada en el orden de presentación (orden Z) del fotograma. También puede mover imágenes arrastrándolas dentro de la lista. Al seleccionar una imagen en la lista y hacer clic en **el botón** Eliminar se quita una imagen. Para cambiar una imagen que ha cargado en otro archivo de imagen, puede hacer clic en el  nombre de archivo para editarla directamente o usar **el botón ...** (puntos suspensivos) para abrir el cuadro de diálogo Seleccionar archivos de imagen y seleccionar otro archivo.

![Captura de pantalla que muestra el botón de puntos suspensivos.](images/f5charell.gif)

Puede usar el cuadro **de texto Duración** para establecer la duración del marco; es decir, cuánto tiempo se mostrará el marco. Si un fotograma no tiene ninguna imagen y duración cero, el fotograma no se mostrará cuando se reproduce la animación.

También puede especificar un archivo de efecto de sonido que se reproducirá cuando se muestre el fotograma. Si planea cargar el carácter desde un servidor web, puede comprimir el archivo de efecto de sonido para minimizar el tiempo de carga. A continuación, puede especificar el archivo de sonido comprimido en el Editor de caracteres del agente. Además, evite usar un efecto de sonido con una duración mayor que la duración de la animación y, especialmente, evite un efecto de sonido que se en bucle, ya que los servicios de animación de Microsoft Agent no envían un evento completo de animación hasta que se complete el sonido. Evite también especificar un efecto de sonido para  cualquier animación que asigne a los estados **De** escucha o Audiencia, ya que esto interfiere con la entrada de voz. Por último, aunque puede incluir más de un efecto de sonido en una animación, evite colocarlos para que se superpongan, ya que esto puede afectar al tiempo de la animación. Además, tenga en cuenta que los efectos de sonido pueden reproducirse a velocidades diferentes en función del hardware del usuario.

Para agregar fotogramas a la animación, vuelva a elegir **el comando Nuevo** marco y siga el mismo procedimiento. Como opción, también puede cargar varias imágenes y generar automáticamente nuevos fotogramas para ellas. Para usar esta característica, elija **Nuevos fotogramas a partir de imágenes** en el **menú** Editar. Los fotogramas se crearán en orden alfabético en función de los nombres de archivo de la imagen. Cuando haya terminado de definir todos los fotogramas de la animación, puede volver a elegir el comando Nueva animación para iniciar una nueva animación. 

Hay otras maneras de agregar fotogramas a animaciones y mover fotogramas dentro o entre animaciones. Puede seleccionar otro fotograma (de la misma  animación u otra animación) y elegir Cortar o **Copiar,** después seleccionar la animación o un marco de esa animación y elegir **Pegar.** También puede arrastrar un fotograma de una animación a otra. Si arrastra dentro de una animación, la acción mueve el marco. Si arrastra a otra animación, copia el marco. Al arrastrar a un marco anterior de la misma animación, se inserta el marco antes del fotograma al que se arrastra. Al arrastrar a un marco siguiente, se coloca después del fotograma al que se arrastra. Si arrastra un marco con el botón derecho del mouse, al soltar el botón se muestra un menú emergente con las opciones de transferencia.

También puede crear una animación copiando una animación existente (seleccione la  animación y elija **Copiar),** seleccione el icono Animaciones u otro icono de animación y elija **Pegar.** El Editor crea automáticamente un nuevo nombre para la animación, aunque puede cambiar el nombre.

### <a name="branching"></a>Bifurcación

Al crear un fotograma, también puede definir qué fotograma se reproduce a continuación. De forma predeterminada, el siguiente fotograma que se reproduce en la secuencia de animación es siempre el siguiente fotograma en el orden Z. Sin embargo, al elegir la **página** Bifurcación, puede establecer la probabilidad de hasta otros tres fotogramas que el servidor puede reproducir. Escriba el porcentaje de probabilidad y el número de fotograma de destino en los campos adecuados. Puede especificar la bifurcación incluso para los fotogramas que no tienen imágenes y tienen su duración establecida en cero. Esto le permite bifurcar sin mostrar primero una imagen determinada.

![Captura de pantalla que muestra la página "Bifurcación".](images/f6charbranch.gif)

Puede usar la característica de bifurcación para crear animaciones que se recorrerán en bucle indefinidamente. Sin embargo, tenga en cuenta que cuando se reproduce una animación en bucle, otras animaciones de la cola del carácter no se reproducirán hasta que un evento (por ejemplo, un usuario que presiona la tecla de inserción para hablar o la aplicación cliente que llama al método [**Stop)**](stop-method.md) detenga la animación de bucle. Por lo tanto, considere detenidamente el contexto en el que se usará la animación antes de crear una animación en bucle.

La página de bifurcación también permite crear ramas de salida. Una rama de salida es una rama a un marco que la animación tomará cuando se detenga la animación y antes de que se resalte la animación siguiente. La definición de ramas de salida le permitirá moverse sin problemas durante la transición de una animación a otra. La bifurcación de salida no debe crear un bucle circular, pero finalmente debe poder salir al último fotograma de la animación.

No es necesario proporcionar una rama de salida para cada fotograma; sin embargo, si no lo hace, la animación seguirá la bifurcación normal del marco. Si el marco no tiene ninguna rama explícita, la animación se bifurca automáticamente al marco que lo sigue. Por ejemplo, si bifurca del fotograma 3 al fotograma 1 y el fotograma 1 no tiene ninguna otra bifurcación (rama normal o de salida), el fotograma 1 se bifurcará al marco 2. Si el fotograma 2 no tiene ninguna bifurcación, la animación volverá a bifurcarse al fotograma 3 y tendrá un bucle circular. En su lugar, podría bifurcar del fotograma 3 al fotograma 1 y, a continuación, establecer la rama de salida del fotograma 1 en cualquier fotograma que esté después del fotograma 3 y normalmente continúe con el último fotograma de la animación.

A veces es posible que tenga que crear un fotograma final explícito de una animación que no se reproduce visiblemente, pero proporciona un final de la animación. Por ejemplo, debe salir de la animación, pero salir al último fotograma no sería adecuado. Para ello, cree un marco de duración cero en blanco como último fotograma de la animación. Esto permite que la animación se reprodgue normalmente a través del último fotograma de la animación y también le permite proporcionar un punto de salida final para la bifurcación de salida.

### <a name="previewing-an-animation"></a>Vista previa de una animación

Puede obtener una vista previa de la animación en  el Editor de caracteres del agente si elige el comando Vista **previa** en el menú Editar o el botón Vista previa de la barra de herramientas. Esto reproduce la animación, incluidas las ramas y los efectos de sonido, a partir del fotograma seleccionado actual. Se restablece al marco seleccionado actual cuando se completa la animación. Para reproducir toda la animación, vaya a la vista de árbol, seleccione el icono o el primer fotograma de la animación y elija el **comando Vista** previa. El editor anima los fotogramas en la **página General.** Para detener la vista previa antes de que finalice, elija el **comando Detener vista** previa. El **comando Vista** previa cambia automáticamente a Detener vista **previa** mientras se reproduce la versión preliminar.

También puede obtener una vista previa de la bifurcación de salida si elige el comando Vista previa **de** bifurcación de salida en el **menú** Editar o en la barra de herramientas. permite probar cómo aparecerá la bifurcación de salida desde cualquier fotograma específico.

### <a name="assigning-speaking-overlays"></a>Asignación de superposiciones de habla

Puede definir un carácter para que hable durante el último fotograma de su animación. En este marco, elija la **página Superposición.** Esta página le permite cargar y asignar archivos de imagen de cocina a las posiciones estándar de la cocina compatibles con Microsoft Agent. Haga clic **en el botón Agregar** imagen y seleccione la imagen en el cuadro de diálogo. También puede seleccionar varias imágenes y el editor cargará y asignará las imágenes a partir de la posición de la cocina que seleccionó. Haga clic **en los botones Subir** y **Bajar** o arrastre una entrada para cambiar una asignación de imagen en la lista. Haga clic **en el botón** Eliminar para quitar una imagen. También puede editar el nombre de ruta de acceso de un archivo asignado haciendo clic en su entrada en  la lista y reeptando su nombre de archivo, o eligiendo el botón **De** puntos suspensivos para mostrar el cuadro de diálogo Seleccionar archivos de imagen.

![Captura de pantalla que muestra la página "Superposiciones" con un archivo seleccionado.](images/f7charover.gif)

Las superposiciones de la máscara deben caber dentro del contorno del marco base sobre el que aparecerán. Si no lo hacen, se recortarán al marco base.

Si desea que el carácter hable con su propia voz fuera del marco base (por ejemplo, cuando el carácter diga hacia los lados), cree primero el marco base con la cabeza del carácter (o el área que se moverá a medida que el carácter hable) como su imagen superior. A continuación, defina las superposiciones de la máscara para reemplazar esa imagen y establezca **la opción Reemplazar imagen superior de marco** base. También puede usar el botón **Establecer** todo para establecer esta opción para todas las superposiciones de la máscara en el marco.

### <a name="assigning-a-return-animation"></a>Asignar una animación de devolución

Para crear una transición fluida de una animación a la siguiente, diseñe las secuencias de animación para que comiencen y terminen con una imagen neutra. Para obtener más información, [**vea Designing Characters for Microsoft Agent**](designing-characters-for-microsoft-agent.md). Sin embargo, esto no significa que cada animación deba terminar en la posición neutra. Puede animar un carácter a través de una secuencia de fotogramas, hacer que hable durante el último fotograma y crear una animación independiente y complementaria que devuelva el carácter a la posición neutra. Esta animación complementaria se denomina animación Return.

Puede definir una animación Return mediante la creación de una animación explícita para este propósito. También puede crear una animación Return mediante la bifurcación de salida que defina dentro de la animación. Para asignar una animación Return, seleccione la animación en el árbol y seleccione la animación Return que creó o Use Exit Branching (Usar bifurcación de salida) en la lista desplegable Animación de retorno de la página Propiedades.

La creación y asignación de una animación Return tiene una ventaja adicional: cuando el servidor recibe una solicitud para reproducir otra animación, intentará reproducir la animación Return para la última animación que ha reproducido, si se asigna una animación Return. Esto garantiza una transición sin problemas. Si una animación comienza y termina en la posición neutra, no es necesario definir una animación Devolución. Del mismo modo, si piensa controlar las transiciones de una animación a otra usted mismo, es posible que no tenga que asignar una animación Devolución.

### <a name="assigning-animations-to-states"></a>Asignación de animaciones a estados

Los servicios de animación de Microsoft Agent reproducen automáticamente animaciones cuando la aplicación cliente de hospedaje usa determinados métodos. Por ejemplo, cuando una aplicación llama a los métodos [**MoveTo**](moveto-method.md) y [**GestureAt,**](gestureat-method.md) el servidor determina automáticamente dónde se muestra el carácter y reproduce una animación adecuada. De forma similar, Microsoft Agent reproduce automáticamente animaciones inactivas cuando el usuario no ha interactuado con el carácter durante varios segundos. Estas condiciones, cuando el servidor reproduce automáticamente animaciones en nombre de una aplicación, se *denominan estados*. Sin embargo, para que el servidor sepa qué animación se va a reproducir, debe asignar animaciones a estos estados.

Para asignar una animación o animaciones a un estado, cree la animación adecuada, expanda la entrada Estados en la vista de árbol de la ventana Editor y seleccione el icono Estado. La lista de animaciones que ha creado aparece en un cuadro de lista en el lado derecho de la ventana. Compruebe la animación que desea asignar a este estado. Tenga en cuenta que puede asignar más de una animación al mismo estado. Esto permite al servidor seleccionar aleatoriamente distintas animaciones para el estado. Asignar una animación a un estado no impide que una animación resalte esa animación directamente.

También puede asignar una animación a un estado seleccionando la entrada de la animación en el árbol. En **el cuadro de lista** Asignar a estado de la página **Propiedades** se enumeran los estados. Active la casilla del estado al que va a asignar la animación.

El Editor no admite la creación de estados adicionales porque los estados solo se aplican a situaciones en las que el servidor debe reproducir automáticamente una animación en nombre de la aplicación cliente. Por lo tanto, no hay ninguna ventaja en la definición de su propio estado. Si es necesario, puede reproducir cualquier animación explícitamente mediante el [**método Play.**](play-method.md)

### <a name="saving-your-character-definition"></a>Guardar la definición de caracteres

Puede guardar el archivo de definición  del carácter  si elige el comando Guardar en el menú Archivo o el botón Guardar definición de **caracteres** de la barra de herramientas. Si desea guardar el archivo de definición de caracteres con un nombre nuevo, elija el comando **Guardar como** en el **menú** Archivo. El Editor guarda la definición modificable de un carácter como definición de carácter del agente (. Archivo ACD). También puede editar este formato de archivo de texto auto documentando con la mayoría de los editores de texto y las aplicaciones de procesamiento de texto.

### <a name="printing-your-character-definition"></a>Imprimir la definición de caracteres

Para imprimir la definición del carácter, elija el comando **Imprimir** en el menú **Archivo** o el botón Imprimir **de** la barra de herramientas. Para establecer las propiedades de la salida impresa, elija el comando **Configuración** de página y elija la configuración antes de seleccionar el **comando** Imprimir.

### <a name="building-a-character"></a>Generar un carácter

Cuando haya terminado de crear las animaciones, el carácter y las imágenes deben compilarse en un formato especial que Microsoft Agent usa para cargar estos datos. Para compilar un carácter, seleccione el comando Carácter de compilación en el **menú** Archivo o en la barra de herramientas. Si ha guardado ediciones en el archivo de definición de caracteres, el Editor guarda el archivo de definición antes de mostrar el cuadro **de** diálogo Carácter de compilación.

![Captura de pantalla que muestra la ventana "Carácter de compilación" con un archivo seleccionado.](images/f8charbldg.gif)

El Editor de caracteres del agente propondrá automáticamente un nombre de archivo basado en el nombre de archivo de la definición de caracteres. El cuadro de diálogo Carácter de compilación también incluye una lista desplegable para que pueda elegir entre compilar el carácter como un único archivo de almacenamiento (. ACS) o como varios archivos. Si elige este último, el Editor compila un . Archivo ACF que incluye los datos de caracteres y . Archivo ACA para cada animación que ha creado. Si planea instalar y acceder a un carácter almacenado en el mismo equipo que la aplicación cliente, normalmente elegiría el formato de archivo estructurado único. Este formato proporciona una instalación y acceso sencillos y eficaces al carácter. Sin embargo, si se accederá al carácter desde un servidor web mediante el protocolo HTTP, compile el carácter mediante . Formato de archivo ACF (individual). Esta última estructura de archivos permite que un script de página web cargue archivos de animación individuales, almacenando los datos en la caché de archivos del explorador del usuario. Proporciona un acceso más eficaz a través de la Web porque los datos de animación se pueden descargar según sea necesario en lugar de requerir al usuario que espere a que todo el conjunto de animaciones se descargue a la vez. Además, dado que los datos del carácter se almacenan en la caché del explorador, el espacio de archivo se puede reclamar automáticamente.

Aunque también puede descargar datos de caracteres (ya sea como un único archivo estructurado o varios archivos) desde un servidor web e instalarlos en otro lugar en la máquina de un usuario, este método requiere aprovisionamientos de seguridad para la descarga y la instalación. Como resultado, la API de Microsoft Agent no incluye compatibilidad con la instalación descargable de un carácter, excepto en la memoria caché del explorador. Sin embargo, puede seguir siendo compatible con este escenario mediante la creación de su propio control de instalación y distribuirlo siguiendo las convenciones de seguridad adecuadas. Para obtener más información, consulte El Kit de desarrollo de software cliente de Internet de Microsoft.

La opción Comprimir permite establecer si los datos de caracteres están comprimidos. Normalmente, querrá establecer esta opción para compactar los datos de caracteres, aunque la creación de un carácter con los datos compactados tarda más tiempo.

Una vez que compile un carácter, las compilaciones posteriores serán más rápidas si compila el carácter en la misma ubicación de directorio. El Editor de caracteres comprueba y copia automáticamente los archivos que no han cambiado y vuelve a compilar los datos que se han editado.

Si el Editor detecta errores en el archivo de caracteres al compilar el carácter, escribe la información en un archivo de registro y muestra un cuadro de mensaje. Puede elegir ver el archivo de registro o omitirlo y leerlo más adelante con un editor de texto. Sin embargo, tenga en cuenta que el Editor sobrescribirá el archivo de registro la próxima vez que compile un archivo de caracteres.

### <a name="editing-an-existing-character"></a>Edición de un carácter existente

Para editar un carácter existente, elija **Abrir en** el **menú** Archivo y seleccione el archivo de definición del carácter (. ACD) en el cuadro de diálogo resultante y elija Abrir. El archivo se cargará en el editor. Tenga en cuenta que no puede cargar archivos de caracteres compilados (. Acs. ACF o . ACA) con el Editor.

Porque el archivo de definición del carácter (. ACD) es un archivo de texto, también puede editar la definición de un carácter abriendo el archivo con un editor de texto o un programa de procesamiento de texto. Sin embargo, al completar los cambios, asegúrese de guardar el archivo en su formato original antes de cargarlo en el editor de caracteres para la compilación.

 

 




