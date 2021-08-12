---
title: Acerca de las listas de imágenes
description: Una lista de imágenes es una colección de imágenes del mismo tamaño, a las que su índice puede hacer referencia a cada una de ellas.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbfbb55ecd972e7f7e257eebabdb94ee40846a4f1b70b2a725ae1b67c6e69e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118672215"
---
# <a name="about-image-lists"></a>Acerca de las listas de imágenes

Una lista de imágenes es una colección de imágenes del mismo tamaño, a las que su índice puede hacer referencia a cada una de ellas. Las listas de imágenes se usan para administrar eficazmente grandes conjuntos de iconos o mapas de bits. Todas las imágenes de una lista de imágenes están contenidas en un único mapa de bits ancho en formato de dispositivo de pantalla. Una lista de imágenes también puede incluir un mapa de bits monocromático que contiene máscaras que se usan para dibujar imágenes de forma transparente (estilo de icono).

La API de Microsoft Win32 proporciona macros y funciones de lista de imágenes que permiten crear y destruir listas de imágenes, agregar y quitar imágenes, reemplazar y combinar imágenes, dibujar imágenes y arrastrar imágenes. Para usar las funciones de lista de imágenes, incluya el archivo de encabezado de control común en los archivos de código fuente y vincule con la biblioteca de exportación de controles comunes. Además, antes de llamar a cualquier función de lista de imágenes, use las funciones [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para asegurarse de que se carga el archivo DLL de control común.

En esta sección se explican los temas siguientes:

-   [Tipos](#types)
-   [Crear y destruir listas de imágenes](#creating-and-destroying-image-lists)
-   [Agregar y quitar imágenes](#adding-and-removing-images)
-   [Reemplazo y combinación de imágenes](#replacing-and-merging-images)
-   [Dibujar imágenes](#drawing-images)
-   [Arrastrar imágenes](#dragging-images)
-   [Información de la imagen](#image-information)
-   [Superposiciones de imágenes](#image-overlays)
-   [Iconos suavizados de contorno de 32 bits](#32-bit-antialiased-icons)

## <a name="types"></a>Tipos

Hay dos tipos de listas de imágenes: no enmascaradas y enmascaradas. Una lista de imágenes sin máscara consta de un mapa de bits de color que contiene una o varias imágenes. Una lista de imágenes enmascaradas consta de dos mapas de bits del mismo tamaño. El primero es un mapa de bits de color que contiene las imágenes y el segundo es un mapa de bits monocromático que contiene una serie de máscaras, una para cada imagen del primer mapa de bits.

Cuando se dibuja una imagen sin máscara, simplemente se copia en el contexto del dispositivo de destino. Es decir, se dibuja sobre el color de fondo existente del contexto del dispositivo. Cuando se dibuja una imagen enmascarada, los bits de la imagen se combinan con los bits de la máscara, lo que normalmente genera áreas transparentes en el mapa de bits donde se muestra el color de fondo del contexto del dispositivo de destino. Hay varios estilos de dibujo que puede especificar al dibujar una imagen enmascarada. Por ejemplo, puede especificar que la imagen se dithered para indicar un objeto seleccionado.

## <a name="creating-and-destroying-image-lists"></a>Crear y destruir listas de imágenes

Para crear una lista de imágenes, llame a la [**función ImageList \_ Create.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) Los parámetros incluyen el tipo de lista de imágenes que se va a crear, las dimensiones de cada imagen y el número de imágenes que se va a agregar a la lista. Para una lista de imágenes sin máscara, la función crea un único mapa de bits lo suficientemente grande como para contener el número especificado de imágenes de las dimensiones especificadas. A continuación, crea un contexto de dispositivo compatible con la pantalla y selecciona el mapa de bits en él. Para una lista de imágenes enmascaradas, la función crea dos mapas de bits y dos contextos de dispositivo compatibles con la pantalla. Selecciona el mapa de bits de imagen en un contexto de dispositivo y el mapa de bits de máscara en el otro. El archivo DLL de control común contiene el código ejecutable para las funciones de lista de imágenes.

En [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create)(Crear imagelist), especifique el número inicial de imágenes que estarán en una lista de imágenes, así como el número de imágenes por las que la lista puede crecer. Por lo tanto, si intenta agregar más imágenes de las que especificó inicialmente, la lista de imágenes crece automáticamente para dar cabida a las nuevas imágenes.

Si [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) se realiza correctamente, devuelve un identificador al tipo HIMAGELIST. Este identificador se usa en otras funciones de lista de imágenes para acceder a la lista de imágenes y administrarlas. Puede agregar y quitar imágenes, copiar imágenes de una lista de imágenes a otra y combinar imágenes de dos listas de imágenes diferentes. Cuando ya no necesite una lista de imágenes, puede destruirla especificando su identificador en una llamada a la [**función ImageList \_ Destroy.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy)

## <a name="adding-and-removing-images"></a>Agregar y quitar imágenes

Puede agregar imágenes, iconos o cursores con mapa de bits a una lista de imágenes. Agregue imágenes de mapa de bits especificando los identificadores a dos mapas de bits en una llamada a la [**función ImageList \_ Add.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) El primer mapa de bits contiene una o varias imágenes para agregar al mapa de bits de imagen, y el segundo mapa de bits contiene las máscaras que se agregarán al mapa de bits de máscara. En el caso de las listas de imágenes sin máscara, se omite el segundo identificador de mapa de bits; se puede establecer en **NULL.**

La [**función ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) también agrega imágenes con mapa de bits a una lista de imágenes enmascaradas. Esta función es similar a [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), salvo que no se especifica un mapa de bits de máscara. En su lugar, especifique un color que el sistema combine con el mapa de bits de imagen para generar automáticamente las máscaras. Cada píxel del color especificado en el mapa de bits de la imagen se cambia a negro y el bit correspondiente de la máscara se establece en 1. Como resultado, cualquier píxel de la imagen que coincida con el color especificado es transparente cuando se dibuja la imagen.

La [**macro ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) agrega un icono o cursor a una lista de imágenes. Si la lista de imágenes está enmascarada, **ImageList \_ AddIcon** agrega la máscara que se proporciona con el icono o cursor al mapa de bits de máscara. Si la lista de imágenes no está enmascarada, la máscara del icono o cursor no se usa al dibujar la imagen.

Puede crear un icono basado en una imagen y máscara en una lista de imágenes mediante la [**función ImageList \_ GetIcon.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) La función devuelve el identificador al nuevo icono.

[**ImageList \_ Agregue**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked y**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) asigne un índice a cada imagen a medida que se agrega a una lista de imágenes. Los índices son de base cero; Es decir, la primera imagen de la lista tiene un índice de cero, la siguiente tiene un índice de uno, y así sucesivamente. Después de agregar una sola imagen, las funciones devuelven el índice de la imagen. Cuando se agrega más de una imagen a la vez, las funciones devuelven el índice de la primera imagen.

La [**función ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) quita una imagen de una lista de imágenes.

## <a name="replacing-and-merging-images"></a>Reemplazo y combinación de imágenes

Las [**funciones ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) e [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) reemplazan una imagen de una lista de imágenes por una nueva imagen. **ImageList \_ Reemplazar** reemplaza una imagen por una imagen y una máscara con mapa de bits, y **ImageList \_ ReplaceIcon** reemplaza una imagen por un icono o cursor.

La [**función ImageList \_ Merge**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) combina dos imágenes y almacena la nueva imagen en una nueva lista de imágenes. La nueva imagen se crea dibujando la segunda imagen de forma transparente sobre la primera. La máscara de la nueva imagen es el resultado de realizar una operación **LÓGICA OR** en los bits de las máscaras para las dos imágenes existentes.

## <a name="drawing-images"></a>Dibujar imágenes

Para dibujar una imagen, use la función [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) Especifique el identificador de una lista de imágenes, el índice de la imagen que se va a dibujar, el identificador del contexto del dispositivo de destino, una ubicación dentro del contexto del dispositivo y uno o varios estilos de dibujo.

Al especificar el estilo **ILD \_ TRANSPARENT,** [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) usa un proceso de dos pasos para dibujar una imagen enmascarada. En primer lugar, realiza una operación **AND** lógica en los bits de la imagen y los bits de la máscara. A continuación, realiza una operación **XOR lógica** en los resultados de la primera operación y los bits en segundo plano del contexto del dispositivo de destino. Este proceso crea áreas transparentes en la imagen resultante; Es decir, cada bit blanco de la máscara hace que el bit correspondiente de la imagen resultante sea transparente.

Antes de dibujar una imagen enmascarada en un fondo de color sólido, debe usar la función [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) para establecer el color de fondo de la lista de imágenes en el mismo color que el destino. Establecer el color elimina la necesidad de crear áreas transparentes en la imagen y permite que [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) simplemente copien la imagen en el contexto del dispositivo de destino, lo que da lugar a un aumento significativo del rendimiento. Para dibujar la imagen, especifique el estilo **\_ ILD NORMAL** en una llamada a **ImageList \_ Draw** o **ImageList \_ DrawEx.**

Puede establecer el color de fondo de una lista de imágenes enmascaradas en cualquier momento para que se dibuje correctamente en cualquier fondo sólido. Al establecer el color de fondo en CLR \_ NONE, las imágenes se dibujan de forma transparente de forma predeterminada. Para recuperar el color de fondo de una lista de imágenes, use la [**función ImageList \_ GetBkColor.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor)

Los **estilos ILD \_ BLEND25** **e ILD \_ BLEND50** difuminan la imagen con el color de resaltado del sistema. Estos estilos son útiles si usa una imagen enmascarada para representar un objeto que el usuario puede seleccionar. Por ejemplo, puede usar el estilo **\_ BLEND50** de ILD para dibujar la imagen cuando el usuario la seleccione.

Una imagen sin máscara se copia en el contexto del dispositivo de destino mediante la operación de trama SRCCOPY. Los colores de la imagen aparecen iguales independientemente del color de fondo del contexto del dispositivo. Los estilos de dibujo especificados en [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) tampoco tienen ningún efecto en la apariencia de una imagen sin máscara.

## <a name="dragging-images"></a>Arrastrar imágenes

La API win32 incluye funciones para arrastrar una imagen en la pantalla. Las funciones de arrastre mueven una imagen sin problemas, en color y sin parpadear el cursor. Se pueden arrastrar imágenes enmascaradas y sin máscara.

La [**función ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) comienza una operación de arrastre. Los parámetros incluyen el identificador de la lista de imágenes, el índice de la imagen que se arrastrará y la ubicación del punto de acceso en caliente dentro de la imagen. La zona activa es un solo píxel que las funciones de arrastre reconocen como la ubicación exacta de la pantalla de la imagen. Normalmente, una aplicación establece la zona de acceso directo para que coincida con la zona de acceso directo del cursor del mouse. La [**función ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) mueve la imagen a una nueva ubicación.

La [**función ImageList \_ DragEnter**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) establece la posición inicial de la imagen de arrastre dentro de una ventana y dibuja la imagen en la posición. Los parámetros incluyen el identificador de la ventana en la que se va a dibujar la imagen y las coordenadas de la posición inicial dentro de la ventana. Las coordenadas son relativas a la esquina superior izquierda de la ventana, no al área de cliente. Lo mismo sucede con todas las funciones de arrastre de imágenes que toman coordenadas como parámetros. Esto significa que debe compensar los anchos de los elementos de ventana, como el borde, la barra de título y la barra de menús al especificar las coordenadas. Si especifica un identificador de ventana **NULL** al llamar a **ImageList \_ DragEnter,** las funciones de arrastre dibujan la imagen en el contexto del dispositivo asociado a la ventana de escritorio y las coordenadas son relativas a la esquina superior izquierda de la pantalla.

La [**función ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) crea una nueva imagen de arrastre combinando la imagen especificada (normalmente una imagen de cursor del mouse) con la imagen de arrastre actual. Dado que las funciones de arrastre usan la nueva imagen durante una operación de arrastre, debe usar la función [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) para ocultar el cursor del mouse real después de llamar a **ImageList \_ SetDragCursorImage**. De lo contrario, puede parecer que el sistema tiene dos cursores del mouse mientras dure la operación de arrastre.

Cuando una aplicación llama a [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag), el sistema crea una lista de imágenes interna temporal y, a continuación, copia la imagen de arrastre especificada en la lista interna. Puede recuperar el identificador de la lista de imágenes de arrastre temporal mediante la [**función ImageList \_ GetDragImage.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) La función también recupera la posición de arrastre actual y el desplazamiento de la imagen de arrastre con respecto a la posición de arrastre.

## <a name="image-information"></a>Información de la imagen

Hay una serie de funciones que recuperan información de una lista de imágenes. La función [**ImageList \_ GetImageInfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) rellena una estructura [**IMAGEINFO**](/windows/desktop/api) con información sobre una sola imagen, incluidos los identificadores de los mapas de bits de imagen y máscara, el número de planos y bits de color por píxel y el rectángulo delimitador de la imagen dentro del mapa de bits de la imagen. Puede usar esta información para manipular directamente los mapas de bits de la imagen. La [**función ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) recupera el número de imágenes de una lista de imágenes.

## <a name="image-overlays"></a>Superposiciones de imágenes

Cada lista de imágenes incluye una lista de índices que se usarán como superposiciones. Una superposición es una imagen que se dibuja de forma transparente sobre otra imagen. Cualquier imagen que esté actualmente en la lista de imágenes se puede usar como superposición. Puede especificar hasta cuatro superposiciones por lista de imágenes. Este límite se ha ampliado a 15 en la versión 4.71.

El índice de una imagen se agrega a la lista de superposiciones mediante la función [**ImageList \_ SetOverlayImage,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) especificando el identificador de la lista de imágenes, el índice de la imagen existente y el índice de superposición deseado. Esto, en efecto, indica a la lista de imágenes que "la imagen en el índice *x* se puede usar como superposición y quiero hacer referencia a la superposición como índice de *superposición y*". Los índices de superposición se basan en uno en lugar de en cero porque un índice de superposición de cero significa que no se usará ninguna superposición.

Se especifica una superposición al dibujar una imagen con la [**función ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx.**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) La superposición se especifica realizando una operación **OR** lógica entre las marcas de dibujo deseadas y el resultado de la macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) La **macro INDEXTOOVERLAYMASK** toma el índice de superposición y le da formato para su inclusión con las marcas de estas funciones. Esto dibujará la imagen con la superposición especificada. En el ejemplo siguiente se muestra cómo se agrega una superposición y se especifica al dibujar la imagen.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Se dibujará la imagen 1 y, a continuación, se superponerá esa imagen con la imagen 0. Dado que 3 es el índice de superposición que especificó en la llamada [**a ImageList \_ SetOverlayImage,**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) 3 se coloca en la macro [**INDEXTOOVERLAYMASK.**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask)

## <a name="32-bit-antialiased-icons"></a>Iconos suavizados de contorno de 32 bits

El suavizado de contorno es una técnica para suavizar o desenfocar los bordes nítidos. Esto proporciona a las imágenes una apariencia más natural. Las listas de imágenes Windows Vista y Windows 7 admiten el uso de iconos y mapas de bits suavizados de 32 bits. Los valores de color usan 24 bits y 8 bits como canal alfa en los iconos. Para crear una lista de imágenes que pueda controlar una imagen de 32 bits por píxel (bpp), llame a la función [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) y pase una marca \_ ILC COLOR32.

Para crear correctamente iconos de 32 bits, debe crear varias imágenes para cada icono, como se muestra en la ilustración siguiente.

![ilustración que muestra tres tamaños de iconos para cada una de las tres profundidades de color](images/theme2.png)

-   Las tres primeras imágenes están en modo de 16 colores para su uso en modo seguro.
-   Los tres iconos siguientes se usan en modo de 256 colores.
-   Los tres últimos iconos tienen el canal alfa y solo se pueden usar en sistemas operativos que ejecutan un color de 24 bits o superior.
-   El orden de las imágenes en el formato de icono es importante. Si el orden es incorrecto, las versiones anteriores de Windows funcionan mal al extraer los iconos. Extraer los iconos incorrectamente puede provocar daños en la memoria y una representación incorrecta.
-   Las versiones anteriores de Windows tenían un límite de recursos de 10 iconos.

> [!Note]  
> Puede usar herramientas de terceros para generar archivos de icono y mapas de bits que contengan un canal alfa. Si usa [**LoadImage para**](/windows/desktop/api/winuser/nf-winuser-loadimagea) cargar un mapa de bits de 32 bpp que contiene alfa, debe especificar la marca LR \_ CREATEDIBSECTION.

 

 

 