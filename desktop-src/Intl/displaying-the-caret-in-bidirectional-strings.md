---
description: En texto unidireccional, la posición del carácter de cursor no tiene ambigüedad porque el borde inicial de un carácter está en el mismo lugar que el borde final del carácter anterior.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Mostrar el caret en cadenas bidireccionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a2e4c9fa06a45b4c653b76395854ee37e0dfdb6f555926987ab4f1a4decb10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328805"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>Mostrar el caret en cadenas bidireccionales

En texto unidireccional, la posición del carácter de cursor no tiene ambigüedad porque el borde inicial de un carácter está en el mismo lugar que el borde final del carácter anterior. Sin embargo, en texto bidireccional, la posición del cursor de cursor entre las ejecuciones de dirección opuesta es ambigua. Por ejemplo, en el párrafo de izquierda a derecha "hellosalaam", la última letra de "hello" precede inmediatamente a la primera letra de "salaam". La mejor posición en la que se debe mostrar el caret depende de si se considera que sigue la "o" de "hello" o que precede a la "s" de "salaam".

Uniscribe usa las convenciones de posicionamiento de los cursores de cursor que se muestran en la tabla siguiente.



| Situación       | Colocación del elemento de inserción visual                       |
|-----------------|----------------------------------------------|
| Escritura          | Borde final del último carácter con tipo.       |
| Pegar         | Borde final del último carácter pegado.      |
| Avance del centro de atención | Borde final del último carácter pasado. |
| Retirada del caret  | Borde inicial del último carácter pasado.  |
| Página principal            | Borde inicial de la línea.                        |
| End             | Borde final de la línea.                       |



 

El cursor de subrayado se puede colocar como se muestra en el ejemplo siguiente:


```C++
if (fAdvancing) {
    ScriptCPtoX(
        iCharPos - 1, TRUE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
} else {
    ScriptCPtoX(
        iCharPos, FALSE, 
        cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
        );
}
```



El posicionamiento del cursor de referencia puede ser más sencillo, como se muestra a continuación, dado un valor *fAdvancing* restringido a **TRUE** o **FALSE:**


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**ScriptCPtoX controla**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) las posiciones fuera del intervalo lógicamente. Devuelve el borde inicial de la ejecución para *iCharPos* <0 y el borde final de la ejecución para *iCharPos* >= length. Para más información, consulte Managing Caret Placement and Hit Testing (Administración [de la selección de ubicación del caret y las pruebas de posicionamiento).](managing-caret-placement-and-hit-testing.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



