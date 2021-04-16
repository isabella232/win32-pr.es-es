---
description: 'Una aplicación puede usar seis funciones para establecer los atributos de formato de texto para un contexto de dispositivo: SetBkColor, SetBkMode, SetTextAlign, SetTextCharacterExtra, SetTextColor y SetTextJustification.'
ms.assetid: fd4d81ee-7f8f-41e8-88a5-d3ed89f4c7bd
title: Atributos de Text-Formatting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58d345bfcfe1693a7ff0b25bb323615dffe221ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104569509"
---
# <a name="text-formatting-attributes"></a>Atributos de Text-Formatting

Una aplicación puede usar seis funciones para establecer los atributos de formato de texto para un contexto de dispositivo: [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor), [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode), [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign), [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra), [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)y [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification). Estas funciones afectan a la alineación del texto, el espaciado entre caracteres, la justificación del texto y los colores de texto y de fondo. Además, se pueden usar seis otras funciones para recuperar los atributos de formato de texto actuales de cualquier contexto de dispositivo: [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor), [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode), [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign), [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra), [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)y [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a).

## <a name="text-alignment"></a>Alineación del texto

Las aplicaciones pueden usar la función [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para especificar cómo debe colocar el sistema los caracteres en una cadena de texto cuando llaman a una de las funciones de dibujo. Esta función se puede usar para colocar encabezados, números de página, llamadas, etc. El sistema coloca una cadena de texto alineando un punto de referencia en un rectángulo imaginario que rodea la cadena, con la posición actual del cursor o con un punto pasado como argumento a una de las funciones de dibujo de texto. La función [**SetTextAlign**](/windows/win32/api/wingdi/nf-wingdi-settextalign) permite a la aplicación especificar la ubicación de este punto de referencia. A continuación se muestra una lista de las ubicaciones de puntos de referencia posibles.



| Ubicación         | Descripción                                                                                                             |
|------------------|-------------------------------------------------------------------------------------------------------------------------|
| izquierda/abajo      | El punto de referencia se encuentra en la esquina inferior izquierda del rectángulo.                                               |
| línea izquierda/base   | El punto de referencia se encuentra en la intersección de la línea base de la celda de carácter y el borde izquierdo del rectángulo.  |
| izquierda/superior         | El punto de referencia se encuentra en la esquina superior izquierda del rectángulo.                                                 |
| Centro/abajo    | El punto de referencia se encuentra en el centro de la parte inferior del rectángulo.                                            |
| centrar/línea base | El punto de referencia se encuentra en la intersección de la línea base de la celda de carácter y el centro del rectángulo.     |
| Centro/superior       | El punto de referencia se encuentra en el centro de la parte superior del rectángulo.                                               |
| derecha/abajo     | El punto de referencia se encuentra en la esquina inferior derecha del rectángulo.                                              |
| línea de base derecha  | El punto de referencia se encuentra en la intersección de la línea base de la celda de carácter y el borde derecho del rectángulo. |
| derecha/arriba        | El punto de referencia se encuentra en la esquina superior derecha del rectángulo.                                                |



 

En la ilustración siguiente se muestra una cadena de texto dibujada llamando a la función [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Antes de dibujar el texto, se llamó a la función [SetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-settextalign) para reubicar el punto de referencia en cada una de las nueve ubicaciones posibles.

![Ilustración que muestra el mismo texto nueve veces, uno para cada ubicación de punto de referencia posible](images/csftx-04.png)

La alineación de texto predeterminada para un contexto de dispositivo es la esquina superior izquierda del rectángulo imaginario que rodea el texto. Una aplicación puede recuperar la configuración de alineación de texto actual para cualquier contexto de dispositivo mediante una llamada a la función [GetTextAlign](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign) .

## <a name="intercharacter-spacing"></a>Espaciado entre caracteres

Las aplicaciones pueden usar la función [SetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra) para modificar el espaciado entre caracteres para todas las operaciones de salida de texto en un contexto de dispositivo especificado. En la ilustración siguiente se muestra una cadena de texto dibujada dos veces llamando a la función [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) . Antes de dibujar el texto por segunda vez, se llamó a la función [**SetTextCharacterExtra**](/windows/win32/api/wingdi/nf-wingdi-settextcharacterextra) para incrementar el espaciado entre caracteres.

![la ilustración shoing dos veces el mismo texto: primero con espaciado entre caracteres normales, con un espaciado más ancho](images/csftx-06.png)

El valor de espaciado entre caracteres predeterminado de cualquier contexto de dispositivo es cero. Una aplicación puede recuperar el valor de espaciado entre caracteres actual para un contexto de dispositivo mediante una llamada a la función [GetTextCharacterExtra](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra) .

## <a name="text-justification"></a>Justificación del texto

Las aplicaciones pueden usar las funciones [GetTextExtentPoint32](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a) y [SetTextJustification](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification) para justificar una línea de texto. La justificación del texto es una operación común en cualquier publicación de escritorio y en la mayoría de las aplicaciones de procesamiento de texto. La función [**GetTextExtentPoint32**](/windows/win32/api/wingdi/nf-wingdi-gettextextentpoint32a) calcula el ancho y el alto de una cadena de texto. Una vez calculado el ancho, la aplicación puede llamar a la función [**SetTextJustification**](/windows/win32/api/wingdi/nf-wingdi-settextjustification) para distribuir el espaciado adicional entre cada una de las palabras de una línea de texto. En la ilustración siguiente se muestra un párrafo de texto impreso dos veces: en el primer párrafo, el texto no estaba justificado. en el segundo párrafo, el texto se justifica llamando a las funciones **GetTextExtentPoint32** y **SetTextJustification** .

![Ilustración en la que se muestra un párrafo que solo se alinea a la izquierda y, a continuación, el mismo párrafo alineado a la izquierda y a la derecha](images/csftx-05.png)

## <a name="text-and-background-color"></a>Color de texto y de fondo

Las aplicaciones pueden usar la función [SetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor) para establecer el color del texto dibujado en el área cliente de las ventanas, así como el color del texto dibujado en una impresora de color. Una aplicación puede usar la función [SetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-setbkcolor) para establecer el color que aparece detrás de cada carácter y la función [SetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-setbkmode) para especificar el modo en que el sistema debe mezclar el color de fondo seleccionado con el color o los colores actuales de la pantalla de vídeo.

El color de texto predeterminado para un contexto de dispositivo de pantalla es negro; el color de fondo predeterminado es blanco; y el modo de fondo predeterminado es opaco. Una aplicación puede recuperar el color de texto actual para un contexto de dispositivo mediante una llamada a la función [GetTextColor](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor) . Una aplicación puede recuperar el color de fondo actual para un contexto de dispositivo mediante una llamada a la función [GetBkColor](/windows/desktop/api/Wingdi/nf-wingdi-getbkcolor) y al modo de fondo actual llamando a la función [GetBkMode](/windows/desktop/api/Wingdi/nf-wingdi-getbkmode) .

 

 
