---
description: 'Una aplicación puede usar seis funciones para establecer los atributos de formato de texto para un contexto de dispositivo: SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor y SetTextJustification.'
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Text-Formatting atributos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e74cb8d30a0eb9b44f05be611da963b413e8798b81da2a334dc083bd3cc1651
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015285"
---
# <a name="text-formatting-attributes"></a>Text-Formatting atributos

Una aplicación puede usar seis funciones para establecer los atributos de formato de texto para un contexto de dispositivo: [SetBkColor,](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) [SetBkMode,](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) [SetTextAlign,](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) [SetTextCharacterExtra,](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)y [SetTextJustification.](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) Estas funciones afectan a la alineación del texto, el espaciado entre caracteres, la justificación del texto y los colores de texto y fondo. Además, se pueden usar otras seis funciones para recuperar los atributos de formato de texto actuales para cualquier contexto de dispositivo: [GetBkColor,](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) [GetBkMode,](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) [GetTextAlign,](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) [GetTextCharacterExtra,](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)y [GetTextExtentPoint32.](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)

## <a name="text-alignment"></a>Alineación del texto

Las aplicaciones pueden usar [la función SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para especificar cómo el sistema debe colocar los caracteres en una cadena de texto cuando llaman a una de las funciones de dibujo. Esta función se puede usar para colocar encabezados, números de página, llamadas, y así sucesivamente. El sistema coloca una cadena de texto alineando un punto de referencia en un rectángulo imaginario que rodea la cadena, con la posición actual del cursor o con un punto pasado como argumento a una de las funciones de dibujo de texto. La [**función SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) permite a la aplicación especificar la ubicación de este punto de referencia. A continuación se muestra una lista de las posibles ubicaciones de punto de referencia.



| Ubicación         | Descripción                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| left/bottom      | El punto de referencia se encuentra en la esquina inferior izquierda del rectángulo.                                               |
| línea izquierda/base   | El punto de referencia se encuentra en la intersección de la línea base de la celda de caracteres y el borde izquierdo del rectángulo.  |
| left/top         | El punto de referencia se encuentra en la esquina superior izquierda del rectángulo.                                                 |
| centro/inferior    | El punto de referencia se encuentra en el centro de la parte inferior del rectángulo.                                            |
| centro/línea base | El punto de referencia se encuentra en la intersección de la línea base de la celda de caracteres y el centro del rectángulo.     |
| center/top       | El punto de referencia se encuentra en el centro de la parte superior del rectángulo.                                               |
| right/bottom     | El punto de referencia se encuentra en la esquina inferior derecha del rectángulo.                                              |
| right/base line  | El punto de referencia se encuentra en la intersección de la línea base de la celda de caracteres y el borde derecho del rectángulo. |
| right/top        | El punto de referencia se encuentra en la esquina superior derecha del rectángulo.                                                |



 

En la ilustración siguiente se muestra una cadena de texto dibujada mediante una llamada a la [función TextOut.](/windows/desktop/api/Wingdi/nf-wingdi-textouta) Antes de dibujar el texto, se llamó a la función [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para reubicar el punto de referencia en cada una de las nueve ubicaciones posibles.

![ilustración que muestra el mismo texto nueve veces, una para cada ubicación de punto de referencia posible](images/csftx-04.png)

La alineación de texto predeterminada para un contexto de dispositivo es la esquina superior izquierda del rectángulo imaginario que rodea el texto. Una aplicación puede recuperar la configuración de alineación de texto actual para cualquier contexto de dispositivo llamando a la [función GetTextAlign.](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)

## <a name="intercharacter-spacing"></a>Intercharacter Spacing

Las aplicaciones pueden usar [la función SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) para modificar el espaciado entre caracteres para todas las operaciones de salida de texto en un contexto de dispositivo especificado. En la ilustración siguiente se muestra una cadena de texto dibujada dos veces llamando a la [función TextOut.](/windows/desktop/api/Wingdi/nf-wingdi-textouta) Antes de dibujar el texto la segunda vez, se llamó a la función [**SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) para incrementar el espaciado entre caracteres.

![ilustración que muestra el mismo texto dos veces: primero con espaciado entre caracteres normal y luego con espaciado más ancho](images/csftx-06.png)

El valor de espaciado entre caracteres predeterminado para cualquier contexto de dispositivo es cero. Una aplicación puede recuperar el valor de espaciado entre caracteres actual de un contexto de dispositivo mediante una llamada a la [función GetTextCharacterExtra.](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)

## <a name="text-justification"></a>Justificación de texto

Las aplicaciones pueden usar [las funciones GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) y [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) para justificar una línea de texto. La justificación de texto es una operación común en cualquier publicación de escritorio y en la mayoría de las aplicaciones de procesamiento de texto. La [**función GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) calcula el ancho y alto de una cadena de texto. Una vez calculado el ancho, la aplicación puede llamar a la función [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir el espaciado adicional entre cada una de las palabras de una línea de texto. En la ilustración siguiente se muestra un párrafo de texto impreso dos veces: en el primer párrafo, el texto no se justifica; en el segundo párrafo, el texto se justificaba mediante una llamada a las funciones **GetTextExtentPoint32** **y SetTextJustification.**

![ilustración que muestra un párrafo que se alinea solo a la izquierda y, a continuación, el mismo párrafo alineado a la izquierda y a la derecha](images/csftx-05.png)

## <a name="text-and-background-color"></a>Texto y color de fondo

Las aplicaciones pueden usar la función [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) para establecer el color del texto dibujado en el área cliente de sus ventanas, así como el color del texto dibujado en una impresora de color. Una aplicación puede usar la función [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) para establecer el color que aparece detrás de cada carácter y la función [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) para especificar cómo debe combinar el sistema el color de fondo seleccionado con el color o los colores actuales en la pantalla del vídeo.

El color de texto predeterminado para un contexto de dispositivo de presentación es negro; el color de fondo predeterminado es blanco; y el modo de fondo predeterminado es OPAQUE. Una aplicación puede recuperar el color de texto actual de un contexto de dispositivo llamando a la [función GetTextColor.](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) Una aplicación puede recuperar el color de fondo actual de un contexto de dispositivo llamando a la función [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) y al modo de fondo actual llamando a [la función GetBkMode.](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode)

 

 
