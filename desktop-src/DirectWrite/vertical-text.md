---
title: Texto vertical
description: A partir de Windows 8, DirectWrite tiene una serie de nuevas API que le permiten usar texto vertical en sus aplicaciones.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db8788a6be97a55911694942a930e17dc69976a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995299"
---
# <a name="vertical-text"></a>Texto vertical

A partir de Windows 8, [DirectWrite](direct-write-portal.md) tiene una serie de nuevas API que le permiten usar texto vertical en sus aplicaciones.

## <a name="drawing-vertical-text"></a>Dibujo de texto vertical

Puede dibujar texto vertical con Direct2D mediante los métodos [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) . Para dibujar el texto verticalmente, pase [**la \_ dirección de lectura de DWRITE \_ \_ de arriba a \_ \_ abajo**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) al método [**IDWriteTextFormat:: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) y [**DWRITE la dirección de flujo de \_ \_ \_ derecha \_ a \_ izquierda**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) al método [**IDWriteTextFormatSetFlowDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) . Después, puede crear y dibujar un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vertical.

## <a name="analyzing-character-orientation"></a>Analizar la orientación de los caracteres

Cada carácter tiene una orientación de carácter preferida o la dirección en la que se debe orientar el carácter en cualquier diseño direccional. Por ejemplo, en el diseño horizontal tradicional, tanto el texto latino como el texto chino están orientados verticalmente. Por otro lado, en un diseño vertical, el texto chino permanece vertical y el texto latino gira 90 grados. Esta diferencia de orientación se muestra en el ejemplo.

![imagen de texto en inglés y chino en diseños horizontales y verticales.](images/vertical-text.png)

Para determinar la orientación del texto que tiene, debe implementar las interfaces [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) y [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) . El origen y el receptor tardan en ejecutarse y permiten comprobar si están orientados verticalmente o no.

Después de implementar el origen y el receptor, llame al método [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) . En la imagen de ejemplo, esta función devuelve 3 ejecuciones: "English", "中国" y "English".

## <a name="going-from-characters-to-glyphs"></a>Pasar de caracteres a glifos

Ahora que sabe que la ejecución contiene glifos verticales, debe obtener acceso a esos glifos. En el ejemplo hasta ahora, hay 3 ejecuciones: una con glifos verticales y dos sin. Para pasar de los caracteres a los glifos, llame a [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Este método devuelve los índices de glifo correspondientes para los caracteres en el ejemplo. Dado que el método [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) devuelve una ejecución con glifos verticales, debe llamar a [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), que devuelve los identificadores de glifo orientados verticalmente en lugar de los identificadores de glifo actuales.

## <a name="drawing-text-vertically"></a>Dibujar texto verticalmente

Por último, debe diseñar y dibujar el texto. Dado que está dibujando el texto verticalmente, deberá obtener algo más de información para que el texto latino se dibuje correctamente. Si dibuja todo el texto a lo largo de la línea de base central, el texto latino parece flotar en el centro de la línea. Necesita acceso a la línea de base central y Latina para alinear el texto correctamente. Use el método [**IDWriteTextAnalyzer1:: GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) para obtener los valores numéricos de las líneas de base que especifique. Puede restar la línea de base Roman de la línea de base central para obtener el desplazamiento entre los dos.

Con toda esta información, puede dibujar el texto en la pantalla. En primer lugar, llame al método [**GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) con los resultados de los objetos [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) y [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) .

Si utiliza [Direct2D](rendering-by-using-direct2d.md) , también debe establecer la transformación universal en el destino de representación de direct2d para la representación vertical.

Por último, llame a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tres veces, una vez en cada bloque de texto. En los dos bloques de texto que están en inglés, debe aplicar el desplazamiento que calculamos entre las líneas de base romanos y centrales.

Ahora, el texto de la aplicación se dibujará verticalmente, con la orientación del glifo correcta.

 

 