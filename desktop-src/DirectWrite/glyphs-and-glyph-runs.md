---
title: Glifos y ejecuciones de glifos
description: Los glifos y las ejecuciones de glifos están disponibles en la capa más baja de funcionalidad de DirectWrite API, la capa de representación de glifos.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite,glyphs
- DirectWrite, ejecuciones de glifo
- ejecuciones de glifo
- glifos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b39d1ca47249adf11f4e1e2072620f24553f7e299e0690c1cc147c4f74a4939f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902930"
---
# <a name="glyphs-and-glyph-runs"></a>Glifos y ejecuciones de glifos

Los glifos y las ejecuciones de glifos están disponibles en la capa más baja de funcionalidad de DirectWrite [API,](direct-write-portal.md) la capa de representación de glifos.

## <a name="glyphs"></a>Glifos

Un glifo es una representación física de un carácter en una fuente determinada. Los caracteres pueden tener muchos glifos, y cada fuente de un sistema podría definir un glifo diferente para ese carácter.

También se pueden combinar dos o más glifos en un único glifo; este proceso se denomina composición de glifos. Esto también se puede hacer en la dirección opuesta, un único glifo que se divide en varios glifos, lo que se conoce como descomposición del glifo.

### <a name="alternate-glyphs"></a>Glifos alternativos

Las fuentes pueden proporcionar glifos alternativos para los caracteres, como los glifos alternativos estilísticos para la fuente OpenType de Pericles, como se muestra en la siguiente captura de pantalla. Los caracteres "A", "E" y "O" se representan con glifos alternativos estilísticos.

![captura de pantalla de la "insondez verde", con "a", "e" y "o" mediante glifos alternativos](images/opentypealternateglyphs.png)

Otro ejemplo de glifos alternativos son glifos de bañar. En la captura de pantalla siguiente se muestran los glifos estándar y de color para la fuente Descalado.

![captura de pantalla de las letras "a" a "n" en glifos standard y swash](images/opentypeswashstandard.png)

Los Swashes y otras características tipográficas, incluidos glifos alternativos más elaborados, están disponibles a través [de OpenType](../intl/opentype-font-format.md). Las características tipográficas de OpenType se pueden aplicar a un intervalo de texto mediante [**IDWriteTextLayout::SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) y pasando la constante de enumeración [**DWRITE \_ FONT FEATURE \_ \_ TAG**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) asociada a la característica deseada.

## <a name="glyph-runs"></a>Ejecuciones de glifo

Una ejecución de glifo representa un conjunto contiguo de glifos que tienen la misma cara y tamaño de fuente, así como el mismo efecto de dibujo de cliente, si los hay. El subrayado y el tachado no forman parte de la ejecución del glifo para el intervalo de texto al que se aplican y se dibujan más adelante. Los objetos en línea, como las imágenes, también se dibujan por separado, ya que no forman parte de una fuente.

### <a name="the-idwritefontface-interface"></a>La interfaz IDWriteFontFace

[DirectWrite](direct-write-portal.md) usa el mismo sistema para la clasificación de fuentes que Windows Pesentation Foundation (WPF), por lo que puede haber varias fuentes físicas por cada familia de fuentes. Una cara de fuente, como la interfaz [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) de DirectWrite, representa una fuente física, con un peso, inclinado y extendido específicos. Contiene el tipo de cara de fuente, las referencias de archivo adecuadas, los datos de identificación de caras y varios datos de fuente, como métricas, nombres y contornos de glifo.

[**IdWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) se puede crear directamente a partir de un nombre de fuente u obtenerse de una colección de fuentes.

### <a name="glyph-metrics"></a>Métricas de glifo

Los glifos individuales tienen métricas asociadas. Puede obtener las métricas de todos los glifos de una ejecución de glifo mediante el [**método IDWriteFontFace::GetDesignGlyphMetrics.**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) Esto devuelve una estructura [**DWRITE \_ GLYPH \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) que tiene el ancho de avance, el grosor de los lados izquierdo y derecho, el soporte lateral superior e inferior, el alto y el origen de línea de base vertical.

En el diagrama siguiente se muestran varias métricas de dos caracteres de glifo diferentes.

![diagrama de las métricas de dos glifos diferentes](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Dibujar una ejecución de glifo

Al implementar un representador de texto personalizado, la representación de glifos se controla mediante [**IDWriteTextRenderer::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), un método de devolución de llamada que se implementa como parte de una clase derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). La [**estructura DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que se pasa a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contiene un objeto [**IDWriteFontFace,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) denominado *fontFace,* que representa la cara de fuente para toda la ejecución del glifo.

El objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) también proporciona el método [**GetGlyphRunOutline,**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) que calcula los contornos del glifo mediante una devolución de llamada de receptor de geometría especificada, como [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) al representar con [Direct2D.](../direct2d/direct2d-portal.md)

Para obtener más información, vea [el tema How to Implement a Custom Text Renderer](how-to-implement-a-custom-text-renderer.md) ( Cómo implementar un representador de texto personalizado).

 

 