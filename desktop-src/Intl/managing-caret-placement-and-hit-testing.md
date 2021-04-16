---
description: Los lenguajes de script complejos se dividen en clústeres por ScriptShape. La reordenación de caracteres siempre se produce dentro de los límites del clúster. Se garantiza que los propios clústeres avanzan en la dirección del orden de lectura.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Administrar la ubicación del símbolo de intercalación y la prueba de posicionamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60396a668c89f7392b28adde0bb123060bf50348
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687091"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Administrar la ubicación del símbolo de intercalación y la prueba de posicionamiento

Los lenguajes de script complejos se dividen en [clústeres](uniscribe-glossary.md) por [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). La reordenación de caracteres siempre se produce dentro de los límites del clúster. Se garantiza que los propios clústeres avanzan en la dirección del orden de lectura.

La información del clúster en la matriz de clústeres lógicos se usa para compartir el ancho de un clúster de glifos equitativamente entre los caracteres lógicos que representan. Por ejemplo, el glifo de Lam Alef se divide en cuatro áreas:

-   La mitad inicial del Lam.
-   La mitad final del Lam.
-   La mitad inicial del Alef.
-   La mitad final del Alef.

Las convenciones de la ubicación del símbolo de intercalación dentro de los clústeres dependen del script. En el caso del script árabe, si la posición del símbolo de intercalación se establece entre un carácter base y su marca de combinación, el símbolo de intercalación se muestra a la mitad del carácter base. En el caso del script tailandés, el símbolo de intercalación no se puede colocar dentro de un clúster. Por lo tanto, cuando el usuario avanza el símbolo de intercalación, la aplicación debe avanzar más allá de todos los glifos que componen el clúster.

Las funciones [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) y [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) se convierten entre las posiciones del símbolo de intercalación (en desplazamientos de punto de código) y las posiciones x (en píxeles). La función **ScriptXtoCP** tiene conocimiento de las convenciones de posición del símbolo de intercalación de cada script:

-   En el caso de India y tailandés, las posiciones del símbolo de intercalación se ajustan a los límites del clúster.
-   En el caso del árabe, las posiciones del símbolo de intercalación se interpolan con clústeres.
-   En el caso del hebreo, en las versiones anteriores a Usp10.dll, la versión 1,420, las posiciones del símbolo de intercalación se interpolan con los clústeres. A partir de Usp10.dll, versión 1,420, las posiciones del símbolo de intercalación se ajustan a los límites del clúster.

Tanto [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) como [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) funcionan solo dentro de las ejecuciones. Las funciones requieren que determinados parámetros provienen de llamadas anteriores a la versión anterior, como se muestra en la tabla siguiente.



| Parámetro                                        | Source                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *PSA*                                            | Tal y como lo devuelve [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Tal y como lo devuelve [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).     |
| *piAdvance*                                      | Tal y como lo devuelve [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).     |



 

La aplicación debe establecer la ejecución en la que un determinado desplazamiento de símbolo de intercalación o posición x es antes de pasar la información a [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) o [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp). Si la aplicación no guarda la información de ancho, puede realizar la prueba de posicionamiento y la posición del símbolo de intercalación después de mostrar cada ejecución. Como alternativa, la aplicación puede almacenar en memoria caché suficiente información para realizar la prueba de posicionamiento y la posición del símbolo de intercalación en la línea actual sin necesidad de volver a procesar el párrafo.

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) devuelve un valor de borde final para que la aplicación conozca el lado del carácter o el clúster en el que el usuario ha haga clic. El valor es 0 o el ancho del carácter o clúster en los puntos de código. La posición del carácter devuelto es la posición del carácter en el que el usuario hizo clic. Para obtener más información, vea [Mostrar el símbolo de intercalación en cadenas bidireccionales](displaying-the-caret-in-bidirectional-strings.md).

En el caso de idiomas como el tailandés, para los que el usuario convencional no desea colocar el símbolo de intercalación en un clúster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) establece la marca lateral final en 0 o en el ancho del clúster. En el caso de idiomas como el árabe, para los que el usuario espera poder editar dentro de un clúster, **ScriptXtoCP** establece la marca lateral final en 0 o en 1.

Para ayudar a la aplicación a establecer ubicaciones válidas para el símbolo de intercalación al controlar las teclas de dirección, Uniscribe proporciona información sobre las posiciones de símbolo de intercalación válidas en el miembro **fCharStop** en los atributos lógicos devueltos por [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak). **True** se devuelve para la mayoría de los caracteres y **false** para los caracteres de interagrupación en scripts como tailandés. La aplicación debe comprobar el valor de **fNeedsCaretInfo** en la estructura de [**\_ propiedades de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) de un elemento para ver si es necesario llamar a **ScriptBreak** para comprobar si hay posiciones de símbolo de intercalación válidas. Si el valor de **fNeedsCaretInfo** es **false**, todos los puntos de código son posiciones de símbolo de intercalación válidas.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




