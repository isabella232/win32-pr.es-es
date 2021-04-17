---
description: En texto unidireccional, la posición del símbolo de intercalación no tiene ambigüedad porque el borde inicial de un carácter está en el mismo lugar que el borde final del carácter anterior.
ms.assetid: 3bebb329-3dd7-4b2e-8ff3-878aaf337a2c
title: Mostrar el símbolo de intercalación en cadenas bidireccionales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c76cce95362aa69564fd245ccad1da4a967dddc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105653007"
---
# <a name="displaying-the-caret-in-bidirectional-strings"></a>Mostrar el símbolo de intercalación en cadenas bidireccionales

En texto unidireccional, la posición del símbolo de intercalación no tiene ambigüedad porque el borde inicial de un carácter está en el mismo lugar que el borde final del carácter anterior. Sin embargo, en texto bidireccional, la posición del símbolo de intercalación entre ejecuciones de dirección opuesta es ambigua. Por ejemplo, en el párrafo de izquierda a derecha "hellosalaam", la última letra de "Hello" precede inmediatamente a la primera letra de "Salaam". La mejor posición en la que se muestra el símbolo de intercalación depende de si se considera que sigue la "o" de "Hola" o antes de "s" de "Salaam".

Uniscribe utiliza las convenciones de posición del símbolo de intercalación que se muestran en la tabla siguiente.



| Situación       | Selección de ubicación del símbolo de intercalación                       |
|-----------------|----------------------------------------------|
| Escritura          | Borde final del último carácter escrito.       |
| Pegar         | Borde final del último carácter pegado.      |
| Avance del símbolo de intercalación | Borde final del último carácter pasado. |
| Retirado del símbolo de intercalación  | Borde inicial del último carácter pasado.  |
| Página principal            | Borde inicial de la línea.                        |
| End             | Borde final de la línea.                       |



 

El símbolo de intercalación se puede colocar tal y como se muestra en el ejemplo siguiente:


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



La posición del símbolo de intercalación puede ser más sencilla, como se muestra a continuación, dado un valor *fAdvancing* restringido a **true** o **false**:


```C++
ScriptCPtoX(
    iCharPos - fAdvancing, fAdvancing, 
    cChars, cGlyphs, &wLogClust, &sva, &iAdvance, &sa, &iCaretX
    );
```



[**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) controla las posiciones fuera del intervalo de forma lógica. Devuelve el borde inicial de la ejecución de *iCharPos* <0, y el borde final de la ejecución de *iCharPos* >= length. Para obtener más información, vea [administrar la colocación del símbolo de intercalación y la prueba de posicionamiento](managing-caret-placement-and-hit-testing.md) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



