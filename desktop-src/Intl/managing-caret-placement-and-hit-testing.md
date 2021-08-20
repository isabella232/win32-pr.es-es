---
description: ScriptShape divide los lenguajes de script complejos en clústeres. La reordenación de caracteres siempre se produce dentro de los límites del clúster. Se garantiza que los propios clústeres avanzan en la dirección del orden de lectura.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Administración de la selección de ubicación del centro de inserción y las pruebas de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e1c6d3b9dbd54f3df2b458a3f7473d1021dceafd6772730b8482b06c4e1c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788405"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Administración de la selección de ubicación del centro de inserción y las pruebas de posicionamiento

ScriptShape divide los lenguajes de script [complejos](uniscribe-glossary.md) en [**clústeres.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) La reordenación de caracteres siempre se produce dentro de los límites del clúster. Se garantiza que los propios clústeres avanzan en la dirección del orden de lectura.

La información del clúster de la matriz de clústeres lógica se usa para compartir el ancho de un clúster de glifos por igual entre los caracteres lógicos que representan. Por ejemplo, el glifo lam alef se divide en cuatro áreas:

-   La mitad inicial del lam.
-   La mitad final del lam.
-   La mitad inicial del alef.
-   La mitad final del alef.

Las convenciones para la selección de ubicación del elemento de inserción en clústeres dependen del script. Para el script árabe, si la posición del signo de subrayado se establece entre un carácter base y su marca de combinación, el carácter de subrayado se muestra a la mitad del carácter base. Para el script tailandés, el cursor de subrayado no se puede colocar dentro de un clúster. Por lo tanto, cuando el usuario avanza el símbolo de sistema, la aplicación debe avanzar más allá de todos los glifos que lo conste.

Las [**funciones ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) y [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) se traducen entre las posiciones del cursor de inserción (en desplazamientos de punto de código) y las posiciones x (en píxeles). La **función ScriptXtoCP** tiene conocimiento de las convenciones de posición de los cursores de cursor de cada script:

-   En el caso de la india y el tailandés, las posiciones de los cursores se alinean con los límites del clúster.
-   En el caso del árabe, las posiciones de los caracteres de cursor se interpolan con clústeres.
-   En el caso del hebreo, en las versiones anteriores a Usp10.dll, versión 1.420, las posiciones del carácter de cursor se interpolan con clústeres. A partir Usp10.dll, versión 1.420, las posiciones del cursor de subrayado se alinean con los límites del clúster.

Tanto [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) como [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) solo funcionan dentro de las ejecuciones. Las funciones requieren que determinados parámetros proceden de llamadas anteriores de Uniscribe, como se muestra en la tabla siguiente.



| Parámetro                                        | Origen                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *Psa*                                            | Como devuelve [**ScriptItemize.**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize) |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Como devuelve [**ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)     |
| *piAdvance*                                      | Devuelto por [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).     |



 

La aplicación debe establecer la ejecución en la que una posición x o desplazamiento de cursor determinado es antes de pasar la información a [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) o [**ScriptXtoCP.**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) Si la aplicación no guarda la información de ancho, puede realizar pruebas de posicionamiento y colocar el elemento de inserción después de mostrar cada ejecución. Como alternativa, la aplicación puede almacenar en caché suficiente información para realizar pruebas de posicionamiento y colocar el elemento de inserción en la línea actual sin necesidad de volver a procesar el párrafo.

[**ScriptXtoCP devuelve**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) un valor perimetral final para que la aplicación conozca el lado del carácter o clúster en el que el usuario ha hecho clic. El valor es 0 o el ancho del carácter o clúster en puntos de código. La posición del carácter devuelto es la posición del carácter en el que el usuario hizo clic. Para obtener más información, [vea Mostrar el caret en cadenas bidireccionales.](displaying-the-caret-in-bidirectional-strings.md)

En el caso de lenguajes como tailandés, para los que el usuario convencionalmente no quiere colocar el signo de asociación en un clúster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) establece la marca del lado final en 0 o en el ancho del clúster. En el caso de idiomas como el árabe, para el que el usuario espera poder editar dentro de un clúster, **ScriptXtoCP** establece la marca del lado final en 0 o en 1.

Para ayudar a la aplicación a establecer ubicaciones válidas para el elemento de cursor al controlar las teclas de dirección, Uniscribe proporciona información sobre las posiciones válidas del elemento caret en el miembro **fCharStop** en los atributos lógicos devueltos por [**ScriptBreak.**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak) **True** se devuelve para la mayoría de los caracteres y **FALSE para** los caracteres interclústeres en scripts como tailandés. La aplicación debe comprobar el valor **fNeedsCaretInfo** en la estructura PROPIEDADES DE [**SCRIPT \_**](/windows/desktop/api/Usp10/ns-usp10-script_properties) de un elemento para ver si es necesario llamar a **ScriptBreak** para comprobar si hay posiciones de símbolo de sistema válidas. Si el **valor de fNeedsCaretInfo** es **FALSE,** todos los puntos de código son posiciones de símbolo de referencia válidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




