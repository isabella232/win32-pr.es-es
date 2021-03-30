---
description: Un script complejo es un script para el que el miembro fComplex de \_ las propiedades de script está establecido en true. En este tema se detallan las propiedades que puede tener un script complejo.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Acerca de los scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104082935"
---
# <a name="about-complex-scripts"></a>Acerca de los scripts complejos

Un [script complejo](uniscribe-glossary.md) es un script para el que  el miembro fComplex [**de \_ las propiedades de script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) está establecido en **true**. En este tema se detallan las propiedades que puede tener un script complejo.

## <a name="bidirectional-rendering"></a>Representación bidireccional

La representación bidireccional es el tratamiento del texto que lee de izquierda a derecha y de derecha a izquierda. Por ejemplo, en la representación bidireccional de árabe, la dirección de lectura predeterminada del texto es de derecha a izquierda, pero es de izquierda a derecha para algunos números. El procesamiento de un script complejo debe tener en cuenta la diferencia entre el orden lógico de pulsación de teclas y el orden visual de los glifos. Además, el procesamiento debe tratar correctamente el movimiento del símbolo de intercalación y la prueba de posicionamiento. La asignación entre la posición de la pantalla y un índice de caracteres requiere la comprensión de los algoritmos de diseño de la pantalla determinada, por ejemplo, la selección de texto o la presentación del símbolo de intercalación.

## <a name="contextual-shaping"></a>Modelado contextual

En el modelado contextual, los caracteres de script cambian de forma en función de los caracteres que los rodean. Este tipo de modelado se produce en escritura cursiva en inglés cuando la forma "l" minúscula cambia según el carácter que lo precede, como una "a" (se conecta bajo a la "l") o una "o" (se conecta alto). Por ejemplo, el árabe es un script que exhibe el modelado contextual.

## <a name="combining-characters"></a>Combinar caracteres

La combinación de caracteres, también denominados "ligaduras", son caracteres que se unen en un carácter cuando se colocan juntos. Arabic es un script que tiene muchos caracteres combinables. Un ejemplo del uso de caracteres de combinación es la "a" seguida de "combinación de acento grave", para la que la representación representada es "à". La secuencia Unicode "U + 0061 U + 0300" requiere cierto procesamiento para asegurarse de que el "acento grave" está colocado correctamente encima de la "a".

## <a name="specialized-word-break-and-justification"></a>Separación y justificación de palabras especializadas

Algunos scripts, por ejemplo, tailandés, tienen reglas complejas para dividir palabras entre líneas o para justificar texto en una línea.

## <a name="filtering-for-illegal-character-combinations"></a>Filtrar por combinaciones de caracteres no válidas

Un script complejo, por ejemplo, tailandés, puede filtrar las combinaciones de caracteres no válidas cuando un lenguaje no permite determinadas combinaciones de caracteres.

## <a name="font-fallback"></a>Reserva de fuentes

La reserva de fuentes es la selección automatizada de una fuente distinta de la fuente seleccionada por el usuario. En Uniscribe, la función [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) aplica la reserva de fuentes cuando todo o parte del texto está en un script que no admite la fuente seleccionada por el usuario. Para obtener más información, vea [usar la reserva de fuentes](using-font-fallback.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



