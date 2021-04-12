---
title: Acerca de las listas de imágenes
description: Una lista de imágenes es una colección de imágenes del mismo tamaño, a las que se puede hacer referencia a través de su índice.
ms.assetid: vs|controls|~\controls\imagelist\imagelist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f059e89b04d16088fff1d937bd29cb23a427d4c2
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359439"
---
# <a name="about-image-lists"></a>Acerca de las listas de imágenes

Una lista de imágenes es una colección de imágenes del mismo tamaño, a las que se puede hacer referencia a través de su índice. Las listas de imágenes se utilizan para administrar de forma eficaz grandes conjuntos de iconos o mapas de bits. Todas las imágenes de una lista de imágenes están contenidas en un único mapa de bits ancho en formato de dispositivo de pantalla. Una lista de imágenes también puede incluir un mapa de bits monocromo que contenga máscaras que se utilizan para dibujar imágenes de forma transparente (estilo de icono).

La API de Microsoft Win32 proporciona funciones y macros de lista de imágenes que permiten crear y destruir listas de imágenes, agregar y quitar imágenes, reemplazar y combinar imágenes, dibujar imágenes y arrastrar imágenes. Para usar las funciones de lista de imágenes, incluya el archivo de encabezado de control común en los archivos de código fuente y vincule con la biblioteca de exportación de control común. Además, antes de llamar a cualquier función de lista de imágenes, use la función [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols) o [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) para asegurarse de que se carga el archivo dll de control común.

En esta sección se explican los temas siguientes:

-   [Tipos](#types)
-   [Crear y destruir listas de imágenes](#creating-and-destroying-image-lists)
-   [Adición y eliminación de imágenes](#adding-and-removing-images)
-   [Reemplazar y combinar imágenes](#replacing-and-merging-images)
-   [Dibujar imágenes](#drawing-images)
-   [Arrastrar imágenes](#dragging-images)
-   [Información de imagen](#image-information)
-   [Superposiciones de imágenes](#image-overlays)
-   [Iconos sin alias de 32 bits](#32-bit-antialiased-icons)

## <a name="types"></a>Tipos

Hay dos tipos de listas de imágenes: no enmascaradas ni enmascaradas. Una lista de imágenes no enmascaradas consta de un mapa de bits de color que contiene una o varias imágenes. Una lista de imágenes enmascaradas consta de dos mapas de bits de igual tamaño. El primero es un mapa de bits de color que contiene las imágenes y el segundo es un mapa de bits monocromo que contiene una serie de máscaras, una para cada imagen del primer mapa de bits.

Cuando se dibuja una imagen no enmascarada, simplemente se copia en el contexto del dispositivo de destino. es decir, se dibuja sobre el color de fondo existente del contexto del dispositivo. Cuando se dibuja una imagen enmascarada, los bits de la imagen se combinan con los bits de la máscara, normalmente produciendo áreas transparentes en el mapa de bits en el que se muestra el color de fondo del contexto del dispositivo de destino. Hay varios estilos de dibujo que puede especificar al dibujar una imagen enmascarada. Por ejemplo, puede especificar que la imagen se haya desactivado para indicar un objeto seleccionado.

## <a name="creating-and-destroying-image-lists"></a>Crear y destruir listas de imágenes

Para crear una lista de imágenes, llame a la función [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) . Los parámetros incluyen el tipo de lista de imágenes que se va a crear, las dimensiones de cada imagen y el número de imágenes que se van a agregar a la lista. En el caso de una lista de imágenes sin máscara, la función crea un mapa de bits único lo suficientemente grande como para contener el número especificado de imágenes de las dimensiones especificadas. Después, crea un contexto de dispositivo compatible con la pantalla y selecciona el mapa de bits en él. En el caso de una lista de imágenes enmascaradas, la función crea dos mapas de bits y dos contextos de dispositivo compatibles con la pantalla. Selecciona el mapa de bits de la imagen en un contexto de dispositivo y el mapa de bits de la máscara en el otro. El archivo DLL de control común contiene el código ejecutable para las funciones de lista de imágenes.

En [**ImageList \_ crear**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create), se especifica el número inicial de imágenes que se incluirán en una lista de imágenes, así como el número de imágenes que puede alcanzar la lista. Por lo tanto, si intenta agregar más imágenes de las especificadas inicialmente, la lista de imágenes crece automáticamente para alojar las nuevas imágenes.

Si [**ImageList \_ crea**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) correctamente, devuelve un identificador al tipo HIMAGELIST. Este identificador se usa en otras funciones de lista de imágenes para tener acceso a la lista de imágenes y administrar las imágenes. Puede Agregar y quitar imágenes, copiar imágenes de una lista de imágenes a otra y combinar imágenes de dos listas de imágenes diferentes. Cuando ya no necesite una lista de imágenes, puede destruirla especificando su identificador en una llamada a la función [**ImageList \_ Destroy**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_destroy) .

## <a name="adding-and-removing-images"></a>Adición y eliminación de imágenes

Puede Agregar imágenes de mapa de imagen, iconos o cursores a una lista de imágenes. Agregue imágenes de mapa de bits especificando los identificadores de dos mapas de bits en una llamada a la función de [**\_ adición ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add) . El primer mapa de bits contiene una o más imágenes para agregar al mapa de bits de la imagen, y el segundo mapa de bits contiene las máscaras que se van a agregar al mapa de bits de la máscara. En el caso de las listas de imágenes no enmascaradas, se omite el segundo identificador de mapa de bits; se puede establecer en **null**.

La función [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked) también agrega imágenes de mapa Dete a una lista de imágenes enmascaradas. Esta función es similar a [**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), salvo que no se especifica un mapa de bits de máscara. En su lugar, se especifica un color que el sistema combina con el mapa de bits de la imagen para generar automáticamente las máscaras. Cada píxel del color especificado en el mapa de bits de la imagen se cambia a negro y el bit correspondiente de la máscara se establece en 1. Como resultado, cualquier píxel de la imagen que coincida con el color especificado es transparente cuando se dibuja la imagen.

La macro [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) agrega un icono o un cursor a una lista de imágenes. Si la lista de imágenes está enmascarada, **ImageList \_ AddIcon** agrega la máscara que se proporciona con el icono o el cursor al mapa de bits de la máscara. Si la lista de imágenes no está enmascarada, la máscara del icono o del cursor no se utiliza al dibujar la imagen.

Puede crear un icono basado en una imagen y una máscara en una lista de imágenes mediante la función [**ImageList \_ GetIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_geticon) . La función devuelve el identificador del nuevo icono.

[**ImageList \_ Add**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_add), [**ImageList \_ AddMasked**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addmasked)y [**ImageList \_ AddIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_addicon) asignan un índice a cada imagen a medida que se agrega a una lista de imágenes. Los índices son de base cero; es decir, la primera imagen de la lista tiene un índice de cero, el siguiente tiene un índice de uno, y así sucesivamente. Después de agregar una sola imagen, las funciones devuelven el índice de la imagen. Cuando se agrega más de una imagen a la vez, las funciones devuelven el índice de la primera imagen.

La función [**ImageList \_ Remove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_remove) quita una imagen de una lista de imágenes.

## <a name="replacing-and-merging-images"></a>Reemplazar y combinar imágenes

Las funciones [**ImageList \_ Replace**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replace) y [**ImageList \_ ReplaceIcon**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_replaceicon) reemplazan una imagen de una lista de imágenes con una nueva imagen. **ImageList \_ Replace** reemplaza una imagen por una imagen de mapa de imágenes y una máscara, y **ImageList \_ ReplaceIcon** reemplaza una imagen por un icono o un cursor.

La función de [**\_ combinación ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_merge) combina dos imágenes, almacenando la nueva imagen en una nueva lista de imágenes. La nueva imagen se crea dibujando la segunda imagen de forma transparente sobre la primera. La máscara de la nueva imagen es el resultado de realizar una operación **or** lógica en los bits de las máscaras de las dos imágenes existentes.

## <a name="drawing-images"></a>Dibujar imágenes

Para dibujar una imagen, use la función [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) . Especifique el identificador de una lista de imágenes, el índice de la imagen que se va a dibujar, el identificador del contexto de dispositivo de destino, una ubicación en el contexto del dispositivo y uno o varios estilos de dibujo.

Al especificar el estilo **\_ transparente rar** , [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o ImageList [**\_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) usa un proceso de dos pasos para dibujar una imagen enmascarada. En primer lugar, realiza una operación **and** lógica en los bits de la imagen y los bits de la máscara. A continuación, realiza una operación **XOR** lógica en los resultados de la primera operación y los bits de fondo del contexto del dispositivo de destino. Este proceso crea áreas transparentes en la imagen resultante; es decir, cada bit en blanco de la máscara hace que el bit correspondiente de la imagen resultante sea transparente.

Antes de dibujar una imagen enmascarada en un fondo de color sólido, debe usar la función [**ImageList \_ SetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setbkcolor) para establecer el color de fondo de la lista de imágenes en el mismo color que el destino. Al establecer el color, se elimina la necesidad de crear áreas transparentes en la imagen y se habilita [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) para copiar simplemente la imagen en el contexto del dispositivo de destino, lo que da lugar a un aumento significativo del rendimiento. Para dibujar la imagen, especifique el **estilo \_ normal rar** en una llamada a **ImageList \_ Draw** o **ImageList \_ DrawEx**.

Puede establecer el color de fondo de una lista de imágenes enmascaradas en cualquier momento para que se dibuje correctamente en cualquier fondo sólido. Al establecer el color de fondo en CLR \_ None, las imágenes se dibujan de manera transparente de forma predeterminada. Para recuperar el color de fondo de una lista de imágenes, use la función [**ImageList \_ GetBkColor**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getbkcolor) .

Los estilos **rar \_ BLEND25** y **rar \_ BLEND50** interpolan la imagen con el color de resaltado del sistema. Estos estilos son útiles si usa una imagen enmascarada para representar un objeto que el usuario puede seleccionar. Por ejemplo, puede usar el estilo **rar \_ BLEND50** para dibujar la imagen cuando el usuario la selecciona.

Una imagen no enmascarada se copia en el contexto de dispositivo de destino mediante la operación de trama SRCCOPY. Los colores de la imagen aparecen igual independientemente del color de fondo del contexto del dispositivo. Los estilos de dibujo especificados en [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o [**ImageList \_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) también no tienen ningún efecto en la apariencia de una imagen no enmascarada.

## <a name="dragging-images"></a>Arrastrar imágenes

La API de Win32 incluye funciones para arrastrar una imagen en la pantalla. Las funciones de arrastre mueven una imagen sin problemas, en color y sin intermitencia del cursor. Se pueden arrastrar imágenes enmascaradas y sin máscara.

La función [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag) inicia una operación de arrastre. Los parámetros incluyen el identificador de la lista de imágenes, el índice de la imagen que se va a arrastrar y la ubicación de la zona activa dentro de la imagen. La zona activa es un solo píxel que las funciones de arrastre reconocen como la ubicación de pantalla exacta de la imagen. Normalmente, una aplicación establece la zona activa para que coincida con la zona activa del cursor del mouse. La función [**ImageList \_ DragMove**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragmove) mueve la imagen a una nueva ubicación.

La función [**\_ DragEnter de ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_dragenter) establece la posición inicial de la imagen de arrastre dentro de una ventana y dibuja la imagen en la posición. Los parámetros incluyen el identificador de la ventana en la que se va a dibujar la imagen y las coordenadas de la posición inicial dentro de la ventana. Las coordenadas son relativas a la esquina superior izquierda de la ventana, no al área cliente. Lo mismo se aplica a todas las funciones de arrastre de imagen que toman las coordenadas como parámetros. Esto significa que debe compensar el ancho de los elementos de ventana como el borde, la barra de título y la barra de menús al especificar las coordenadas. Si especifica un identificador de ventana **nulo** al llamar a la función **ImageList \_**, las funciones de arrastre dibujan la imagen en el contexto del dispositivo que está asociado a la ventana del escritorio y las coordenadas son relativas a la esquina superior izquierda de la pantalla.

La función [**ImageList \_ SetDragCursorImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setdragcursorimage) crea una nueva imagen de arrastre combinando la imagen especificada (normalmente una imagen de cursor del mouse) con la imagen de arrastre actual. Dado que las funciones de arrastre usan la nueva imagen durante una operación de arrastre, debe usar la función [**ShowCursor**](/windows/desktop/api/winuser/nf-winuser-showcursor) para ocultar el cursor del mouse real después de llamar a **ImageList \_ SetDragCursorImage**. De lo contrario, puede parecer que el sistema tiene dos cursores del mouse mientras dure la operación de arrastre.

Cuando una aplicación llama a [**ImageList \_ BeginDrag**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_begindrag), el sistema crea una lista de imágenes temporal e internas y, a continuación, copia la imagen de arrastre especificada en la lista interna. Puede recuperar el identificador de la lista de imágenes de arrastre temporal mediante la función [**ImageList \_ GetDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getdragimage) . La función también recupera la posición de arrastre actual y el desplazamiento de la imagen de arrastre con respecto a la posición de arrastre.

## <a name="image-information"></a>Información de imagen

Hay una serie de funciones que recuperan información de una lista de imágenes. La función [**ImageList \_ GetImageInfo**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimageinfo) rellena una estructura [**IMAGEINFO**](/windows/desktop/api) con información sobre una sola imagen, incluidos los identificadores de los mapas de bits de la imagen y de la máscara, el número de planos de color y los bits por píxel, y el rectángulo delimitador de la imagen dentro del mapa de bits de la imagen. Puede usar esta información para manipular directamente los mapas de bits de la imagen. La función [**ImageList \_ GetImageCount**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_getimagecount) recupera el número de imágenes de una lista de imágenes.

## <a name="image-overlays"></a>Superposiciones de imágenes

Cada lista de imágenes incluye una lista de los índices que se van a usar como superposiciones. Una superposición es una imagen que se dibuja de forma transparente sobre otra imagen. Cualquier imagen que se encuentre actualmente en la lista de imágenes se puede usar como una superposición. Puede especificar hasta cuatro superposiciones por lista de imágenes. Este límite se ha ampliado a 15 en la versión 4,71.

Agregue el índice de una imagen a la lista de superposiciones mediante la función [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , especificando el identificador de la lista de imágenes, el índice de la imagen existente y el índice de superposición deseado. Esto, en efecto, indica a la lista de imágenes que "la imagen en el índice *x* se puede usar como superposición y quiero hacer referencia a la superposición como índice de superposición *y*". Los índices de superposición están basados en uno en lugar de basarse en cero porque un índice de superposición de cero significa que no se usará ninguna superposición.

Se especifica una superposición al dibujar una imagen con la función [**\_ DrawEx**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_drawex) de [**ImageList \_ Draw**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_draw) o ImageList. La superposición se especifica mediante la realización de una operación **or** lógica entre las marcas de dibujo deseadas y el resultado de la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) . La macro **INDEXTOOVERLAYMASK** toma el índice de superposición y lo formatea para su inclusión con las marcas de estas funciones. Esto dibujará la imagen con la superposición especificada. En el ejemplo siguiente se muestra cómo se agrega una superposición y se especifica al dibujar la imagen.


```
ImageList_SetOverlayImage(himl, 0, 3);
ImageList_Draw(himl, 1, hdc, 0, 0, ILD_MASK | INDEXTOOVERLAYMASK(3));
```



Esto dibujará la imagen 1 y, a continuación, superpondrá la imagen con la imagen 0. Dado que 3 es el índice de superposición que especificó en la llamada [**ImageList \_ SetOverlayImage**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_setoverlayimage) , 3 se coloca en la macro [**INDEXTOOVERLAYMASK**](/windows/desktop/api/Commctrl/nf-commctrl-indextooverlaymask) .

## <a name="32-bit-antialiased-icons"></a>Iconos sin alias de 32 bits

El suavizado de contorno es una técnica para suavizar o desenfocar bordes nítidos. Esto proporciona a las imágenes una apariencia más natural. Las listas de imágenes en Windows Vista y Windows 7 admiten el uso de los iconos y mapas de bits con suavizado de 32 bits. Los valores de color usan 24 bits y se usan 8 bits como canal alfa en los iconos. Para crear una lista de imágenes que pueda controlar una imagen de 32 bits por píxel (BPP), llame a la función de [**\_ creación ImageList**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) , pasando una \_ marca COLOR32 de ILC.

Para crear iconos de 32 bits correctamente, debe crear varias imágenes para cada icono, tal como se muestra en la siguiente ilustración.

![Ilustración que muestra tres tamaños de iconos para cada una de las tres profundidades de color](images/theme2.png)

-   Las tres primeras imágenes están en modo de 16 colores para su uso en modo seguro.
-   Los tres iconos siguientes se usan en el modo de 256 colores.
-   Los tres últimos iconos tienen el canal alfa y solo se pueden usar en sistemas operativos que ejecutan un color de 24 bits o superior.
-   El orden de las imágenes en el formato de icono es importante. Si el orden es incorrecto, las versiones anteriores de Windows funcionarán mal al extraer los iconos. La extracción incorrecta de los iconos puede producir daños en la memoria y una representación incorrecta.
-   Las versiones anteriores de Windows tenían un límite de recursos de 10 iconos.

> [!Note]  
> Puede usar herramientas de terceros para generar archivos de icono y mapas de bits que contengan un canal alfa. Si usa [**LoadImage**](/windows/desktop/api/winuser/nf-winuser-loadimagea) para cargar un mapa de bits 32 bpp que contiene Alpha, debe especificar la marca LR \_ CREATEDIBSECTION.

 

 

 