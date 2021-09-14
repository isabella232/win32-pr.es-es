---
title: Métricas de texto
description: Para ayudar al diseño, la selección de fuentes personalizadas y otras operaciones de uso intensivo de métricas, a partir de Windows 8, DirectWrite tiene varias API nuevas para expresar toda la información sobre las fuentes que puede necesitar para desarrollar aplicaciones de texto enriquecido.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73647ae4521b23afb399a4c66c8b25cdc46ba1b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069968"
---
# <a name="text-metrics"></a>Métricas de texto

Para ayudar al diseño, la selección de fuentes personalizadas y otras operaciones de uso intensivo de métricas, a partir de [Windows 8, DirectWrite](direct-write-portal.md) tiene varias API nuevas para expresar toda la información sobre las fuentes que puede necesitar para desarrollar aplicaciones de texto enriquecido.

## <a name="panose"></a>PANOSE

PANOSE es un sistema de clasificación visual para identificar tipos de letra. La clasificación PANOSE contiene información sobre la familia, el estilo serif, el peso, la proporción, el contraste, el trazo, el estilo de los brazos, la altura X, etc. Esta información describe el estilo visual de la fuente. Esta información es importante porque las fuentes con valores PANOSE similares tienen un aspecto similar. Esto es muy útil en situaciones en las que una fuente no está disponible y la aplicación debe volver a una fuente disponible. La comparación de valores PANOSE para fuentes permite elegir una fuente similar visualmente a la fuente original.

Para acceder a la información de PANOSE de una fuente, use el método [**GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) en las interfaces [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) e [**IDWriteFontFace1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) Este método devuelve una [**enumeración \_ DWRITE PANOSE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) que contiene toda la información de PANOSE para esa fuente.

## <a name="additional-metrics"></a>Métricas adicionales

A partir Windows 8, la API [de DirectWrite](direct-write-portal.md) también admite varias métricas nuevas para expresar información útil sobre las fuentes a la aplicación. Estas nuevas métricas incluyen esta información.

-   Métricas de rectángulo de selección de glifos izquierda, derecha, superior e inferior.
-   Posición X e Y para elementos de superíndice y subíndice.
-   Información de escalado X e Y para elementos de superíndice y subíndice.
-   Si la fuente tiene o no métricas tipográficos.

Esta información está disponible a través del nuevo [**método GetMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) en las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1.**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) Este método devuelve una estructura [**DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) que contiene toda esta información.

## <a name="caret-metrics"></a>Métricas de caret

Para crear aplicaciones de edición de texto, necesita acceso a información sobre cómo dibujar el elemento de diálogo que navega por el texto. A partir Windows 8, [DirectWrite](direct-write-portal.md) proporciona el método [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) en las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) para este escenario. **GetCaretMetrics devuelve** una enumeración [**\_ DWRITE CARET \_ METRICS**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) que contiene información sobre la pendiente y el desplazamiento del centro de referencia a lo largo de la línea base.

Esta información es específicamente útil si desea poder tener la pendiente del centro de diálogo adecuadamente con texto en cursiva.

## <a name="monospaced-discoverability"></a>Detectabilidad monoespacial

Las aplicaciones que permiten a los usuarios escribir código de equipo suelen usar fuentes monoespaciales en lugar de fuentes más tradicionales. Por lo tanto, puede tener más control sobre la selección de [fuentes](direct-write-portal.md) en aplicaciones relacionadas con el desarrollo, DirectWrite expresa si una fuente está monoespacial o no a través de la API. El [**método IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) de la interfaz [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) devuelve un valor booleano que indica si la fuente está monoespacial o no.

## <a name="font-name-matching"></a>Coincidencia de nombres de fuente

Las aplicaciones de texto enriquecido, como los lectores pdf, deben poder hacer coincidir las fuentes de su contenido con las fuentes del sistema y necesitan acceder a los nombres completos de las fuentes en varios formatos. Para que pueda hacer coincidir mejor las fuentes, [DirectWrite](direct-write-portal.md) contiene una enumeración que expresa la información de nomenclatura completa sobre una fuente en muchos formatos.

use la [**enumeración DWRITE \_ INFORMATIONAL \_ STRING \_ ID**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) para obtener el nombre completo, PostScript nombre y PostScript cid de cualquier fuente del sistema. Esta información es valiosa cuando necesita hacer coincidir las fuentes de la aplicación con las fuentes adecuadas en el sistema local.

## <a name="glyph-advances"></a>Avances de glifo

El **método GetGlyphAdvances** de las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) toma el recuento de glifos y los índices sobre los que necesita información de avances y, a continuación, devuelve los avances de los glifos en cuestión.

## <a name="unicode-ranges"></a>Intervalos Unicode

Las aplicaciones que desean controlar su propia selección de fuentes necesitan tener acceso a los intervalos Unicode admitidos por la fuente. De este modo, si la fuente no admite un punto de código Unicode, la aplicación puede elegir una fuente adecuada que contenga ese glifo. Sin esta información, la aplicación puede usar una fuente que no contenga todos los glifos necesarios para mostrar la información presente.

El [**método GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) de las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) toma el número máximo de intervalos pasados desde el cliente y devuelve los intervalos reales admitidos por la fuente.

## <a name="eudc-font-collection"></a>Colección de fuentes EUDC

Use el [**método GetEudcFontCollection en**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) la [**interfaz IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) para acceder a la colección de fuentes EUDC. Este método funciona de la misma manera que [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection), pero en su lugar devuelve un puntero a una colección de fuentes EUDC.

 

 