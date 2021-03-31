---
title: Justificación, interletraje y espaciado
description: A partir de Windows 8, DirectWrite proporciona una serie de características que le permiten controlar características tipográficas, de diseño y de espaciado básicas, como el espaciado de caracteres, el kerning de pares y la justificación.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cc915922d0dbadb45bf47f223df83a25414daf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793522"
---
# <a name="justification-kerning-and-spacing"></a>Justificación, interletraje y espaciado

A partir de Windows 8, [DirectWrite](direct-write-portal.md) proporciona una serie de características que le permiten controlar características tipográficas, de diseño y de espaciado básicas, como el espaciado de caracteres, el kerning de pares y la justificación.

## <a name="character-spacing"></a>espaciado entre caracteres

El espaciado de caracteres, también conocido como "seguimiento", es el espaciado entre los caracteres de una ejecución de texto.

Este es un ejemplo de seguimiento. La primera línea no aplica ningún seguimiento al texto. La segunda línea aumenta el espaciado entre caracteres y la tercera línea reduce el espaciado de los caracteres.

![tres ejemplos del mismo texto sin seguimiento, más espaciado y menos espaciado.](images/spacing.png)

A partir de Windows 8, [DirectWrite](direct-write-portal.md) agrega aquí estos métodos para controlar el espaciado de los caracteres en el texto.

Si usa el diseño de [DirectWrite](direct-write-portal.md) , puede usar los métodos [**IDWriteTextLayout1:: GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) y [**IDWriteTextLayout1:: SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) para este propósito.

Use el método [**GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) para determinar el espaciado de caracteres actual y devuelve el carácter actual, el espaciado antes y después del carácter, el ancho de avance mínimo y una estructura de [**\_ \_ intervalo de texto DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que contiene información sobre la posición inicial y la longitud del texto restante.

Use [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) en una interfaz [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) para aplicar su propio espaciado de caracteres al texto en el diseño. El método **SetCharacterSpacing** toma la cantidad de espacio que desea antes y después del carácter, el adelanto mínimo permitido y un intervalo de [**\_ texto DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que define el intervalo para aplicar el espaciado.

Si usa un diseño personalizado, [DirectWrite](direct-write-portal.md) admite la configuración del espaciado de caracteres con [**IDWriteTextAnalyzer1:: ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Use este método si necesita un diseño de texto personalizado para tener un control avanzado sobre el diseño. Este método permite proporcionar **ApplyCharacterSpacing** con el espaciado inicial y final, el ancho de avance mínimo, la longitud del mapa de clústeres, el número de glifos, la asignación de intervalos de caracteres a glifos y el ancho de avance de cada glifo si se usa un diseño personalizado. El método devuelve los avances del glifo modificado y una enumeración de [**\_ \_ desplazamiento del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) con los nuevos desplazamientos al origen de cada glifo.

## <a name="kerning"></a>El interletraje

El kerning es el ajuste del espaciado contextual entre pares o triples de letras. El espaciado específico entre conjuntos de caracteres puede aumentar la legibilidad y hacer que el texto sea mejor. La diferencia importante entre el kerning y el espaciado de caracteres es el hecho de que el espaciado entre mayúsculas y minúsculas es independiente del texto que Spaces, mientras que el kerning se usa en determinadas situaciones entre ciertos pares de caracteres, tal y como se define en la fuente.

La imagen es un ejemplo de kerning. La palabra AVATAR de la línea superior está intercalada para que la palabra parezca más natural. Como puede ver en los cuadros rojos que hay alrededor de los caracteres, se aplica más espaciado entre las cuatro primeras letras, mientras que el R del extremo tiene más espacio antes. El texto original sin interletraje está en la segunda línea. El kerning de este ejemplo hace que la palabra sea más legible y más natural.

![un ejemplo de la misma palabra con y sin aplicar el interletraje.](images/kerning.png)

El carácter avanza entre pares de caracteres que la fuente Kerns se almacena en la tabla de kerning y [DirectWrite](direct-write-portal.md) analiza esa tabla y devuelve la información a través de las API de interletraje.

Si desea saber si una fuente admite o no el kerning, puede usar el método [**IDWriteFontFace1:: HasKerningPairs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) . Este método devuelve un valor booleano de 1 si la fuente admite pares de interletraje.

[**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) también tiene un método que le permite obtener acceso a los ajustes del par de interletraje para los índices de glifo. [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) permite especificar una matriz de índices de glifo y [DirectWrite](direct-write-portal.md) devuelve una matriz de ajustes de avance del glifo. Si una fuente no admite la tabla de interletraje, el método devuelve ceros para los ajustes de avance del glifo.

Si usa el diseño de [DirectWrite](direct-write-portal.md) , hay dos métodos en la interfaz [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) que permiten establecer el kerning de pares y obtener más información sobre el kerning de pares en el diseño. El método [**SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) toma una representación booleana de si desea habilitar el kerning de pares y un intervalo de [**\_ texto DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) que define el intervalo de texto al que se va a aplicar. Si desea saber si el kerning está habilitado o no en un intervalo de texto, puede usar el método [**GetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) , que toma la posición actual y devuelve un valor booleano que corresponde a si está habilitado el kerning o no, y el intervalo de texto al que se aplica la configuración de interletraje.

## <a name="justification"></a>Justificación

La justificación es el proceso de alinear texto para que rellene todo el espacio de una columna mediante el aumento de los avances entre los caracteres o los clústeres de glifos o la adición de caracteres de justificación para lograr el mismo efecto. En general, esto se logra determinando dónde se debe agregar espacio a una línea de texto e insertando caracteres de espacio en esas oportunidades de interrupción. Estos elementos de espaciado también pueden ser diferentes, en los scripts latinos, el texto se justifica aumentando el ancho de avance entre los elementos, mientras que en árabe, el texto está justificado con un kashida. A continuación se muestra un ejemplo de script árabe y latín justificado y no justificado.

![un ejemplo de script árabe y latín justificado y no justificado.](images/justification.png)

A partir de Windows 8, [DirectWrite](direct-write-portal.md) tiene varios métodos que le permiten justificar texto en sus aplicaciones.

Hay un valor adicional en la enumeración de [**\_ \_ alineación de texto de DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) . Puede usar el método [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) y pasar la constante de **\_ alineación del texto DWRITE \_ \_ justificada** y [DirectWrite](direct-write-portal.md) justifica el texto e inserta el carácter de justificación adecuado para el script.

Si usa un diseño personalizado, tenga una serie de métodos disponibles para que pueda aprovechar las ventajas de la justificación. [DirectWrite](direct-write-portal.md) tiene tres métodos en la interfaz [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) que puede usar para agregar justificación a un diseño personalizado.

El primer método es [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities), que toma el texto que desea justificar y devuelve una estructura de [**\_ \_ oportunidad de justificación de DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que describe dónde se pueden agregar los caracteres de justificación para justificar el texto.

La segunda función es [**JustifyGlyphAdvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances), que justifica una matriz de avances de glifo para que se ajusten al ancho de línea. Este método toma la estructura de la [**\_ \_ oportunidad de justificación de DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) que genera [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) , los avances del glifo y los desplazamientos del glifo. A continuación, genera los avances del glifo justificado y una enumeración de [**\_ \_ desplazamiento del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) que contiene los desplazamientos del glifo justificado.

La tercera función es [**GetJustifiedGlyphs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs), que rellena los nuevos glifos para los scripts complejos en los que la justificación ha aumentado los avances para los glifos. Solo es necesario llamar a **GetJustifiedGlyphs** si el script tiene un carácter de justificación específico devuelto por [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties). Este método toma información sobre la fuente, la longitud del texto, el tamaño em de los glifos, el script del texto, el número de glifos, el mapa del clúster, los avances/desplazamientos del glifo original, los avances y desplazamientos del glifo justificados y las propiedades del glifo. El método devuelve el número real de glifos, el mapa de clústeres actualizado, los índices de glifo actualizados con glifos de justificación insertados, desplazamientos de glifos actualizados y avances de glifos actualizados.

 

 