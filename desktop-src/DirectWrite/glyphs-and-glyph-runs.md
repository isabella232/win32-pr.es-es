---
title: Glifos y ejecuciones de glifos
description: Los glifos y las ejecuciones de glifo están disponibles en el nivel más bajo de funcionalidad de la API de DirectWrite, la capa de representación de glifos.
ms.assetid: e670cb65-1fcb-46fd-ac0b-02eaaaa51996
keywords:
- DirectWrite, glifos
- DirectWrite, ejecuciones de glifos
- ejecuciones de glifo
- glifos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32c5c6b30c9a44cde4704e6afd231cebbc91d2be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149382"
---
# <a name="glyphs-and-glyph-runs"></a>Glifos y ejecuciones de glifos

Los glifos y las ejecuciones de glifo están disponibles en el nivel más bajo de funcionalidad de la API de [DirectWrite](direct-write-portal.md) , la capa de representación de glifos.

## <a name="glyphs"></a>Glifos

Un glifo es una representación física de un carácter en una fuente determinada. Los caracteres podrían tener muchos glifos, y cada fuente de un sistema podría definir un glifo diferente para ese carácter.

Dos o más glifos también se pueden combinar en un solo glifo; este proceso se denomina composición de glifos. Esto también se puede hacer en la dirección opuesta, un único glifo que se divide en varios glifos, lo que se conoce como descomposición del glifo.

### <a name="alternate-glyphs"></a>Glifos alternativos

Las fuentes pueden proporcionar glifos alternativos para los caracteres, como los glifos alternativos de estilo para la fuente OpenType de Pericles, tal como se muestra en la siguiente captura de pantalla. Los caracteres ' A ', ' E ' y ' O ' se representan con glifos alternativos de estilo.

![captura de pantalla de "antigua de la mitología verde", con "a", "e" y "o" mediante glifos alternativos](images/opentypealternateglyphs.png)

Otro ejemplo de glifos alternativos son los glifos floreados. En la captura de pantalla siguiente se muestran glifos estándar y floreados para la fuente pescadero.

![captura de pantalla de las letras de la "a" a la "n" en glifos estándar y floreados](images/opentypeswashstandard.png)

Los caracteres floreados y otras características tipográficas, incluidos los glifos alternativos más elaborados, están disponibles a través de [OpenType](../intl/opentype-font-format.md). Las características tipográficas OpenType se pueden aplicar a un intervalo de texto mediante [**IDWriteTextLayout:: SetTypography**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-settypography) y pasando la constante de enumeración de la etiqueta de la [**\_ característica de fuente \_ \_ DWRITE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_feature_tag) asociada a la característica deseada.

## <a name="glyph-runs"></a>Ejecuciones de glifo

Una ejecución de glifo representa un conjunto contiguo de glifos que tienen el mismo tamaño y tipo de fuente, así como el mismo efecto de dibujo del cliente, si existe. El subrayado y el tachado no forman parte de la ejecución del glifo para el intervalo de texto al que se aplican y se dibujan más adelante. Los objetos alineados, como las imágenes, también se dibujan por separado, ya que no forman parte de una fuente.

### <a name="the-idwritefontface-interface"></a>La interfaz IDWriteFontFace

[DirectWrite](direct-write-portal.md) usa el mismo sistema para la clasificación de fuentes que Windows Pesentation Foundation (WPF), por lo que puede haber varias fuentes físicas por cada familia de fuentes. Un tipo de fuente, como la interfaz [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) en DirectWrite, representa una fuente física, con una ponderación, inclinación y ajuste específicos. Contiene el tipo de fuente Font, las referencias de archivo apropiadas, los datos de identificación de caras y diversos datos de fuente, como las métricas, los nombres y los contornos de glifo.

[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) puede crearse directamente a partir de un nombre de fuente u obtenerse de una colección de fuentes.

### <a name="glyph-metrics"></a>Métricas de glifo

Los glifos individuales tienen métricas asociadas. Puede obtener las métricas para todos los glifos de una ejecución de glifo mediante el método [**IDWriteFontFace:: GetDesignGlyphMetrics**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getdesignglyphmetrics) . Esto devuelve una estructura de [**\_ \_ métricas del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) que tiene el ancho de avance, el cojinete de la izquierda y la derecha, el cojinete superior e inferior, el alto y el origen de la línea de base vertical.

En el diagrama siguiente se muestran varias métricas de dos caracteres de glifo diferentes.

![diagrama de las métricas de dos glifos diferentes](images/twoglyphs.png)

## <a name="drawing-a-glyph-run"></a>Dibujar una ejecución de glifos

Al implementar un representador de texto personalizado, la representación de glifos se controla mediante [**IDWriteTextRenderer::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), un método de devolución de llamada que se implementa como parte de una clase derivada de [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer). La estructura de [**\_ \_ ejecución del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) que se pasa a [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) contiene un objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) , denominado *fontFace*, que representa el tipo de fuente para toda la ejecución del glifo.

El objeto [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) también proporciona el método [**GetGlyphRunOutline**](/windows/win32/api/dwrite/nf-dwrite-idwritefontface-getglyphrunoutline) , que calcula los contornos del glifo mediante el uso de una devolución de llamada del receptor de geometría, como [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) , cuando se representa con [Direct2D](../direct2d/direct2d-portal.md).

Para obtener más información, consulte el tema [cómo implementar un representador de texto personalizado](how-to-implement-a-custom-text-renderer.md) .

 

 