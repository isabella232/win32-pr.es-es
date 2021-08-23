---
title: Texto vertical
description: A partir de Windows 8, DirectWrite tiene varias API nuevas que le permiten usar texto vertical en las aplicaciones.
ms.assetid: F40A79AE-F7BF-4CAC-9480-1489CD212DA8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6aa5e6626ae77e610c38bfb90def7cfe068db80f7f300f58a734969fb107a46a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632555"
---
# <a name="vertical-text"></a>Texto vertical

A partir de Windows 8, [DirectWrite](direct-write-portal.md) tiene varias API nuevas que permiten usar texto vertical en las aplicaciones.

## <a name="drawing-vertical-text"></a>Dibujo de texto vertical

Puede dibujar texto vertical con Direct2D mediante los métodos [**DrawTextLayout.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) Para dibujar el texto verticalmente, pase [**DWRITE \_ READING DIRECTION TOP TO \_ \_ \_ \_ BOTTOM**](/windows/win32/api/dwrite/ne-dwrite-dwrite_reading_direction) al método [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) y [**DWRITE FLOW DIRECTION RIGHT \_ \_ TO \_ \_ \_ LEFT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_flow_direction) al [**método IDWriteTextFormatSetFlowDirection.**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setflowdirection) A continuación, puede crear y dibujar un [**objeto IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) vertical.

## <a name="analyzing-character-orientation"></a>Análisis de la orientación de caracteres

Cada carácter tiene una orientación de caracteres preferida o la dirección en la que el carácter debe estar orientado en cualquier diseño direccional. Por ejemplo, en el diseño horizontal tradicional, tanto el texto latino como el texto chino están orientados verticalmente. Por otro lado, en un diseño vertical, el texto chino permanece vertical y el texto latino gira 90 grados. Esta diferencia en la orientación se observa en el ejemplo aquí.

![una imagen de texto en inglés y chino en diseños horizontales y verticales.](images/vertical-text.png)

Para determinar la orientación del texto que tiene, debe implementar las interfaces [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) El origen y el receptor toman las ejecuciones del glifo y permiten comprobar si están orientadas verticalmente o no.

Después de implementar el origen y el receptor, llame al [**método AnalyzeVerticalGlyphOrientation.**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) En la imagen de ejemplo, esta función devuelve 3 ejecuciones: "English", "principal" e "English".

## <a name="going-from-characters-to-glyphs"></a>Pasar de caracteres a glifos

Ahora que sabe que la ejecución contiene glifos verticales, debe obtener acceso a esos glifos. En el ejemplo hasta ahora, hay tres ejecuciones: una con glifos verticales y dos sin . Para realizar la transición de caracteres a glifos, llame a [**GetGlyphIndices**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphindices). Este método devuelve los índices de glifo correspondientes para los caracteres del ejemplo. Dado que el método [**AnalyzeVerticalGlyphOrientation**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-analyzeverticalglyphorientation) devuelve una ejecución con glifos verticales, debe llamar a [**GetVerticalGlyphVariants**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getverticalglyphvariants), que devuelve los ID de glifo orientados verticalmente en lugar de los actuales.

## <a name="drawing-text-vertically"></a>Dibujar texto verticalmente

Por último, debe crear y dibujar el texto. Dado que dibuja el texto verticalmente, debe obtener más información para que el texto latino se dibuja correctamente. Si dibuja todo el texto a lo largo de la línea base central, el texto latino parece flotar en el centro de la línea. Necesita acceso a la línea base central y a la base de referencia de Román para alinear el texto correctamente. Use el [**método IDWriteTextAnalyzer1::GetBaseline**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getbaseline) para obtener los valores numéricos de las líneas base que especifique. Puede restar la línea base de Román de la línea base central para obtener el desplazamiento entre los dos.

Con toda esta información, puede dibujar el texto en la pantalla. En primer lugar, llame al [**método GetGlyphOrientationTransform**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getglyphorientationtransform) con los resultados de los objetos [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) e [**IDWriteTextAnalysisSource1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1)

Si usa [Direct2D, también](rendering-by-using-direct2d.md) debe establecer la transformación del mundo en el destino de representación de Direct2D para la representación vertical.

Por último, llame [**a DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) tres veces, una vez en cada bloque de texto. En los dos bloques de texto que están en inglés, debe aplicar el desplazamiento que calculamos entre las líneas base de Román y centrales.

Ahora, el texto de la aplicación se dibujará verticalmente, con la orientación correcta del glifo.

 

 