---
title: Justificación, kerning y espaciado
description: A partir de Windows 8, DirectWrite proporciona una serie de características que le permiten controlar las características tipográficas, de diseño y espaciado básicas, como el espaciado de caracteres, el emparejamiento de pares y la justificación.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdd82e201429adb62e687021f003d7d5d6bedcd228c3102f448b04d1f079f71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632651"
---
# <a name="justification-kerning-and-spacing"></a>Justificación, kerning y espaciado

A partir de Windows 8, [DirectWrite](direct-write-portal.md) proporciona una serie de características que permiten controlar las características tipográficas, de diseño y espaciado básicas, como el espaciado de caracteres, el kerning de pares y la justificación.

## <a name="character-spacing"></a>espaciado entre caracteres

El espaciado de caracteres, también conocido como "seguimiento", es el espaciado entre los caracteres de una ejecución de texto.

Este es un ejemplo de seguimiento. La primera línea no aplica ningún seguimiento al texto. La segunda línea aumenta el espaciado de caracteres y la tercera línea reduce el espaciado de caracteres.

![tres ejemplos del mismo texto sin seguimiento, más espaciado y menos espaciado.](images/spacing.png)

A partir Windows 8, [DirectWrite](direct-write-portal.md) estos métodos aquí para controlar el espaciado de caracteres en el texto.

Si usa el diseño [DirectWrite,](direct-write-portal.md) puede usar los métodos [**IDWriteTextLayout1::GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) e [**IDWriteTextLayout1::SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) para este propósito.

Use el [**método GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) para determinar el espaciado de caracteres actual y devuelve el carácter actual, el espaciado antes y después del carácter, el ancho de avance mínimo y una estructura [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que contiene información sobre la posición inicial y la longitud del texto restante.

Use [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) en una interfaz [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) para aplicar su propio espaciado de caracteres al texto del diseño. El **método SetCharacterSpacing** toma la cantidad de espacio que desea antes y después del carácter, el avance mínimo permitido y un INTERVALO DE TEXTO [**DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que define el intervalo para aplicar el espaciado.

Si usa un diseño [personalizado,](direct-write-portal.md) DirectWrite para establecer el espaciado de caracteres con [**IDWriteTextAnalyzer1::ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Use este método si necesita un diseño de texto personalizado para tener un control avanzado sobre el diseño. Este método permite proporcionar **a ApplyCharacterSpacing** el espaciado inicial y final, el ancho de avance mínimo, la longitud del mapa del clúster, el número de glifos, la asignación de intervalos de caracteres a glifos y el ancho de avance de cada glifo si se usa un diseño personalizado. El método devuelve los avances del glifo modificado y una enumeración [**DWRITE \_ GLYPH \_ OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) con los nuevos desplazamientos al origen de cada glifo.

## <a name="kerning"></a>Kerning

El kerning es el ajuste de espaciado contextual entre pares o tripletes de letras. El espaciado específico entre conjuntos de caracteres puede aumentar la legibilidad y mejorar el aspecto del texto. La diferencia importante entre el kerning y el espaciado de caracteres es el hecho de que el espaciado de letras es independiente del texto que espacios, mientras que el kerning se usa en determinadas situaciones entre determinados pares de caracteres, tal como se define en la fuente.

La imagen de ella es un ejemplo de kerning. La palabra AVATAR en la línea superior se kerned para que la palabra parezca más natural. Como puede ver en los cuadros rojos alrededor de los caracteres, se aplica más espaciado entre las cuatro primeras letras, mientras que la R del final tiene más espacio delante. El texto original sin kerning está en la segunda línea. El kerning de este ejemplo hace que la palabra sea más legible y natural.

![un ejemplo de la misma palabra con y sin kerning aplicado.](images/kerning.png)

El carácter avanza entre pares de caracteres que los kerns de fuente se almacenan en la tabla kern y [DirectWrite](direct-write-portal.md) analiza esa tabla y devuelve la información a través de las API de kerning.

Si desea saber si una fuente admite o no el kerning de pares, puede usar el [**método IDWriteFontFace1::HasKerningPairs.**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) Este método devuelve un valor bool de 1 si la fuente admite pares de kerning.

[**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) también tiene un método que le permite obtener acceso a los ajustes del par de kerning para los índices de glifo. [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) permite introducir una matriz de índices de glifo y [DirectWrite](direct-write-portal.md) devuelve una matriz de ajustes de avance de glifo. Si una fuente no admite la tabla kern, el método devuelve ceros para los ajustes de avance del glifo.

Si usa el diseño [DirectWrite,](direct-write-portal.md) hay dos métodos en la interfaz [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) que le permiten establecer el kerning de pares y obtener más información sobre el emparejamiento de kerning en el diseño. El [**método SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) toma una representación booleana de si desea habilitar o no el kerning de pares y un INTERVALO DE TEXTO [**DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que define el intervalo de texto al que se va a aplicar. Si desea saber si está habilitado o no el emparejamiento de kerning en un intervalo de texto, puede usar el método [**GetPairKerning,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) que toma la posición actual y devuelve un valor bool que corresponde a si está habilitado o no el kerning de pares, y el intervalo de texto al que se aplica la configuración de kerning.

## <a name="justification"></a>Justificación

La justificación es el proceso de alinear texto para que rellene todo el espacio de una columna aumentando los avances entre caracteres o clústeres de glifos o agregando caracteres de justificación para lograr el mismo efecto. En general, esto se logra determinando dónde se debe agregar espacio a una línea de texto e insertando caracteres de espaciado en esas oportunidades de separación. Estos elementos de espaciado también pueden diferir; en los scripts latinos, el texto se justifica aumentando los anchos de avance entre los elementos, mientras que en árabe, el texto se justifica con un kashida. Este es un ejemplo de script árabe y latino tanto justificado como no justificado.

![un ejemplo de script árabe y latino tanto justificado como no justificado.](images/justification.png)

A partir Windows 8, [DirectWrite](direct-write-portal.md) tiene una serie de métodos que permiten justificar el texto en las aplicaciones.

Hay un valor adicional en la [**enumeración DWRITE \_ TEXT \_ ALIGNMENT.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) Puede usar el [**método SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) y pasar la constante **DWRITE \_ TEXT ALIGNMENT \_ \_ JUSTIFIED** y [DirectWrite](direct-write-portal.md) justifica el texto e inserta el carácter de justificación adecuado para el script.

Si usa un diseño personalizado, tiene una serie de métodos disponibles para que pueda aprovechar las ventajas de la justificación. [DirectWrite](direct-write-portal.md) tiene tres métodos en la interfaz [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) que puede usar para agregar una justificación a un diseño personalizado.

El primer método es [**GetJustificationOpportunities,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities)que toma el texto que desea justificar y devuelve una estructura [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que describe dónde se pueden agregar caracteres de justificación para justificar el texto.

La segunda función es [**JustifyGlyphAdvances,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances)que justifica una matriz de avances de glifo para que se ajusten al ancho de línea. Este método toma la estructura [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que [**genera GetJustificationOpportunities,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) los avances del glifo y los desplazamientos del glifo. A continuación, genera los avances de glifos justificados y una enumeración [**DWRITE \_ GLYPH \_ OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) que contiene los desplazamientos de glifos justificados.

La tercera función es [**GetJustifiedGlyphs,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs)que rellena los nuevos glifos para scripts complejos donde la justificación ha aumentado los avances de los glifos. Solo es necesario llamar a **GetJustifiedGlyphs** si el script tiene un carácter de justificación específico devuelto por [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties). Este método toma información sobre la fuente, la longitud del texto, el tamaño em de los glifos, el script del texto, el número de glifos, el mapa del clúster, los desplazamientos o avances de glifo originales, los desplazamientos o avances de glifos justificados y las propiedades del glifo. El método devuelve el recuento real de glifos, el mapa de clúster actualizado, los índices de glifo actualizados con glifos de justificación insertados, los desplazamientos de glifo actualizados y los avances de glifo actualizados.

 

 