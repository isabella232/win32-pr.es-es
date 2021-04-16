---
title: Métricas de texto
description: Con el fin de ayudarle en el diseño, la selección de fuentes personalizada y otras operaciones intensivas de métricas, a partir de Windows 8, DirectWrite tiene varias API nuevas para expresar toda la información sobre las fuentes que puede necesitar para desarrollar aplicaciones de texto enriquecido.
ms.assetid: 9df8c675-6f4d-4de7-916e-7dc51f5f04aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73647ae4521b23afb399a4c66c8b25cdc46ba1b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685794"
---
# <a name="text-metrics"></a>Métricas de texto

Con el fin de ayudarle en el diseño, la selección de fuentes personalizada y otras operaciones intensivas de métricas, a partir de Windows 8, [DirectWrite](direct-write-portal.md) tiene varias API nuevas para expresar toda la información sobre las fuentes que puede necesitar para desarrollar aplicaciones de texto enriquecido.

## <a name="panose"></a>PANOSE

Panose es un sistema de clasificación visual que identifica los tipos de letra. La clasificación Panose contiene información sobre la familia, estilo serif, peso, proporción, contraste, trazo, estilo ARM, altura X, etc. Esta información describe el estilo visual de la fuente. Esta información es importante porque las fuentes con valores Panose similares son similares. Esto es muy útil en situaciones en las que una fuente no está disponible y la aplicación debe revertir a una fuente que esté disponible. La comparación de los valores de la Panose con las fuentes permite elegir una fuente similar visualmente a la fuente original.

Para tener acceso a la información de la Panose de una fuente, use el método [**GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) en las interfaces [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) y [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) . Este método devuelve una enumeración [**\_ Panose DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_panose) que contiene toda la información de la Panose de esa fuente.

## <a name="additional-metrics"></a>Métricas adicionales

A partir de Windows 8, la API de [DirectWrite](direct-write-portal.md) también admite varias métricas nuevas con el fin de expresar información útil sobre las fuentes en la aplicación. Estas nuevas métricas incluyen esta información.

-   Métricas de los rectángulos de selección de borde izquierdo, derecho, superior e inferior.
-   Posición X e y para elementos de superíndice y subíndice.
-   Información de escalado X e y para elementos de superíndice y subíndice.
-   Indica si la fuente tiene métricas tipográficas o no.

Esta información está disponible a través del nuevo método [**GetMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getmetrics) en las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) y [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) . Este método devuelve una estructura [**DWRITE \_ Font \_ METRICS1**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_font_metrics1) que contiene toda esta información.

## <a name="caret-metrics"></a>Métricas de símbolo de intercalación

Para crear aplicaciones de edición de texto, necesita acceso a información sobre cómo dibujar el símbolo de intercalación que navega por el texto. A partir de Windows 8, [DirectWrite](direct-write-portal.md) proporciona el método [**GetCaretMetrics**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getcaretmetrics) en las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) e [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) para este escenario. **GetCaretMetrics** devuelve una enumeración de [**\_ \_ métricas del símbolo de intercalación DWRITE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_caret_metrics) que contiene información sobre la pendiente y el desplazamiento para el símbolo de intercalación a lo largo de la línea base.

Esta información es especialmente útil si desea poder tener la pendiente del símbolo de intercalación apropiadamente con texto en cursiva.

## <a name="monospaced-discoverability"></a>Detectabilidad monoespaciada

Las aplicaciones que permiten a los usuarios escribir código de equipo suelen usar fuentes monoespaciadas en lugar de fuentes más tradicionales. Por lo tanto, puede tener más control sobre la selección de fuentes en las aplicaciones relacionadas con el desarrollo, [DirectWrite](direct-write-portal.md) expresa si una fuente está monoespaciada a través de la API. El método [**IsMonospacedFont**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-ismonospacedfont) de la interfaz [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) devuelve un valor booleano que indica si la fuente está monoespaciada o no.

## <a name="font-name-matching"></a>Coincidencia de nombres de fuente

Las aplicaciones de texto enriquecido como los lectores de PDF deben ser capaces de hacer coincidir las fuentes de su contenido con las fuentes del sistema, necesitan tener acceso a los nombres completos de las fuentes en varios formatos. Por lo que puede coincidir mejor con fuentes, [DirectWrite](direct-write-portal.md) contiene una enumeración que expresa información de nombres completos sobre una fuente en muchos formatos.

Use la enumeración [**DWRITE \_ informativa de \_ \_ identificador de cadena**](/windows/win32/api/dwrite/ne-dwrite-dwrite_informational_string_id) para obtener el nombre completo, el nombre POSTscript y el nombre CID PostScript de cualquier fuente del sistema. Esta información es útil si necesita hacer coincidir las fuentes de la aplicación con las fuentes adecuadas en el sistema local.

## <a name="glyph-advances"></a>Avances de glifo

El método **GetGlyphAdvances** en las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) y [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) toma el recuento de glifos y los índices en los que necesita más información y, a continuación, devuelve los avances para los glifos en cuestión.

## <a name="unicode-ranges"></a>Intervalos Unicode

Las aplicaciones que desean administrar su propia selección de fuente necesitan tener acceso a los intervalos Unicode admitidos por la fuente. De este modo, si la fuente no admite un punto de código Unicode, la aplicación puede elegir una fuente adecuada que contenga ese glifo. Sin esta información, la aplicación puede usar una fuente que no contenga todos los glifos necesarios para mostrar la información presente.

El método [**GetUnicodeRanges**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getunicoderanges) en las interfaces [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) y [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) toma el número máximo de intervalos pasados desde el cliente y devuelve los intervalos reales admitidos por la fuente.

## <a name="eudc-font-collection"></a>Colección de fuentes EUDC

Use el método [**GetEudcFontCollection**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefactory1-geteudcfontcollection) de la interfaz [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) para acceder a la colección de fuentes EUDC. Este método funciona de la misma forma que [**GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection), pero en su lugar devuelve un puntero a una colección de fuentes EUDC.

 

 