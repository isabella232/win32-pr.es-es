---
description: Un script complejo es un script para el que el miembro fComplex de PROPIEDADES DE SCRIPT \_ se establece en TRUE. En este tema se detallan las propiedades que podría tener un script complejo.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Acerca de los scripts complejos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e865b7638419178e3339169e56e8ceb111bcc65b925d9c337b5b71d0341827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520655"
---
# <a name="about-complex-scripts"></a>Acerca de los scripts complejos

Un [script complejo](uniscribe-glossary.md) es un script para el que el miembro **fComplex** de SCRIPT [**\_ PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) se establece en **TRUE.** En este tema se detallan las propiedades que podría tener un script complejo.

## <a name="bidirectional-rendering"></a>Representación bidireccional

La representación bidireccional es el control de texto que lee de izquierda a derecha y de derecha a izquierda. Por ejemplo, en la representación bidireccional del árabe, la dirección de lectura predeterminada del texto es de derecha a izquierda, pero es de izquierda a derecha para algunos números. El procesamiento de un script complejo debe tener en cuenta la diferencia entre el orden lógico (pulsación de tecla) y el orden visual de los glifos. Además, el procesamiento debe tratar correctamente con el movimiento del centro de atención y las pruebas de impacto. La asignación entre la posición de la pantalla y un índice de caracteres requiere una comprensión de los algoritmos de diseño para la presentación determinada, por ejemplo, la selección de texto o la presentación de caracteres de diálogo.

## <a name="contextual-shaping"></a>Forma contextual

En el modelado contextual, los caracteres de script cambian de forma en función de los caracteres que los rodean. Este modelado se produce en la escritura cursiva en inglés cuando una "l" minúscula cambia de forma en función del carácter que la precede, como una "a" (se conecta bajo a la "l") o una "o" (se conecta alto). Por ejemplo, árabe es un script que muestra la forma contextual.

## <a name="combining-characters"></a>Combinar caracteres

Los caracteres combinados, también denominados "ligaduras", son caracteres que se unen en un carácter cuando se colocan juntos. Árabe es un script que tiene muchos caracteres combinados. Un ejemplo del uso de caracteres combinados es "a" seguido de "combining grave", para el que la representación representada es "miento". La secuencia Unicode "U+0061 U+0300" requiere algún procesamiento para asegurarse de que la "gravedad de combinación" se coloca correctamente encima de la "a".

## <a name="specialized-word-break-and-justification"></a>Interrupción y justificación de palabras especializadas

Algunos scripts, por ejemplo, tailandés, tienen reglas complejas para dividir palabras entre líneas o justificar texto en una línea.

## <a name="filtering-for-illegal-character-combinations"></a>Filtrado de combinaciones de caracteres no válidas

Un script complejo, por ejemplo, tailandés, puede filtrar combinaciones de caracteres no válidas cuando un lenguaje no permite determinadas combinaciones de caracteres.

## <a name="font-fallback"></a>Reserva de fuentes

La reserva de fuentes es la selección automatizada de una fuente que no sea la fuente seleccionada por el usuario. En Uniscribe, la función [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) aplica la reserva de fuentes cuando todo o parte del texto está en un script que la fuente seleccionada por el usuario no admite. Para obtener más información, vea [Using Font Fallback](using-font-fallback.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



