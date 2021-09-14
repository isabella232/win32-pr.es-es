---
title: DirectWrite estructuras
description: DirectWrite define las estructuras siguientes.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite,structures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f678be8e02c8afecd849673d97ae20f6b1a710
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069971"
---
# <a name="directwrite-structures"></a>DirectWrite estructuras

DirectWrite define las estructuras siguientes.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](/windows/windows-app-sdk/api/win32/dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32) | Representa los datos de mapa de bits en formato BGRA32. |
| [**MÉTRICAS \_ DE CARET DE DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | La [**estructura DWRITE \_ CARET \_ METRICS**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) especifica las métricas para la selección de ubicación del elemento de inserción en una fuente. |
| [**MÉTRICAS DE CLÚSTER DE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contiene información sobre un clúster de glifos. |
| [**DWRITE \_ COLOR \_ F**](dwrite-color-f.md) | Describe los componentes rojo, verde, azul y alfa de un color. |
| [**EJECUCIÓN DEL \_ GLIFO DE COLOR \_ DWRITE \_**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contiene la información necesaria para que los representadores dibujen ejecuciones de glifo con información de color de glifo. |
| [**DWRITE \_ COLOR \_ GLYPH \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Representa una ejecución de glifo de color. El método IDWriteFactory4::TranslateColorGlyphRun devuelve una colección ordenada de ejecuciones de glifos de color de distintos tipos en función de lo que admita la fuente. |
| [**FRAGMENTO DE \_ ARCHIVO DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Representa un intervalo de bytes en un archivo de fuente. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Representa el intervalo mínimo y máximo de los valores posibles para un eje de fuente. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Representa un valor para un eje de fuente. Se usa al consultar y crear instancias de fuente. |
| [**CARACTERÍSTICA DE \_ FUENTE \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Especifica las propiedades usadas para identificar y ejecutar características tipográficas en la cara de fuente actual. |
| [**MÉTRICAS \_ DE FUENTE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | La [**estructura DWRITE \_ FONT \_ METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) especifica las métricas que son aplicables a todos los glifos dentro de la cara de fuente. |
| [**DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | La [**estructura DWRITE \_ FONT \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) especifica las métricas que son aplicables a todos los glifos dentro de la cara de fuente. |
| [**DWRITE \_ FONT \_ PROPERTY**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Propiedad de fuente utilizada para filtrar conjuntos de fuentes y crear un conjunto de fuentes con propiedades explícitas. |
| [**DATOS DE IMAGEN \_ DE GLIFO \_ DE DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Datos para un único glifo de GetGlyphImageData. |
| [**MÉTRICAS DE GLIFO DE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Especifica las métricas de un glifo individual. |
| [**DESPLAZAMIENTO DEL \_ GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Ajuste opcional a la posición de un glifo. |
| [**EJECUCIÓN DEL \_ GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contiene la información necesaria para que los representadores dibujen ejecuciones de glifo. |
| [**DESCRIPCIÓN DE LA \_ EJECUCIÓN \_ DEL GLIFO DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contiene propiedades adicionales relacionadas con las de [**DWRITE \_ GLYPH \_ RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**MÉTRICAS DE \_ PRUEBAS DE \_ IMPACTO DE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Describe la región obtenida por una prueba de acceso. |
| [**MÉTRICAS DE \_ OBJETOS EN LÍNEA \_ DE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contiene propiedades que describen la medida geométrica de un objeto en línea definido por la aplicación. |
| [**OPORTUNIDAD DE \_ JUSTIFICACIÓN DE DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | La [**estructura DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) especifica la información de justificación por glifo. |
| [**PUNTO DE \_ INTERRUPCIÓN DE LÍNEA \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Características del punto de interrupción de línea de un carácter. |
| [**MÉTRICAS DE LÍNEA DE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contiene información sobre una línea de texto con formato. |
| [**DWRITE \_ LINE \_ METRICS1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contiene información sobre una línea de texto con formato. |
| [**ESPACIADO DE LÍNEA \_ DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | La [**estructura DWRITE \_ MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) especifica la transformación de gráficos que se va a aplicar a los glifos representados. |
| [**MÉTRICAS \_ DE SOBRESALIR DE DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indica la cantidad de DIP visibles (píxeles independientes del dispositivo) sobreshoot en cada lado del diseño o los objetos en línea. |
| [**DWRITE \_ PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | La [**unión \_ DWRITE PANOSE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) describe los valores de clasificación de tipo de letra que se usan con [**IDWriteFont1::GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) para seleccionar y hacer coincidir la fuente. |
| [**ANÁLISIS DE SCRIPTS DE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Almacena la asociación de texto y su script del sistema de escritura, así como algunos atributos para mostrar. |
| [**PROPIEDADES DEL \_ SCRIPT DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | La [**estructura DWRITE \_ SCRIPT \_ PROPERTIES**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) especifica las propiedades de script para la navegación y justificación de los elementos de tipo caret. |
| [**PROPIEDADES DEL GLIFO \_ DE FORMA \_ DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contiene propiedades de salida de forma para un glifo de salida. |
| [**PROPIEDADES DE TEXTO \_ DE FORMA DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Dar forma a las propiedades de salida de un glifo de salida. |
| [**DWRITE \_ STRIKETHROUGH**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contiene información sobre el tamaño y la ubicación de los tachados. |
| [**MÉTRICAS DE TEXTO DE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contiene las métricas asociadas al texto después del diseño. |
| [**DWRITE \_ TEXT \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contiene las métricas asociadas al texto después del diseño. |
| [**INTERVALO DE TEXTO \_ DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Especifica un intervalo de posiciones de texto donde se aplica el formato en el texto representado por un [**objeto IDWriteTextLayout.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) |
| [**RECORTE DE \_ DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Especifica la opción de recorte para el texto que desborda el cuadro de diseño.  |
| [**CARACTERÍSTICAS TIPOGRÁFICAS DE DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contiene un conjunto de características tipográficas que se aplicarán durante el modelado de texto. |
| [**DWRITE \_ UNDERLINE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contiene información sobre el ancho, el grosor, el desplazamiento, el alto de ejecución, la dirección de lectura y la dirección del flujo de un subrayado.  |
| [**INTERVALO \_ UNICODE DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | La [**estructura DWRITE \_ UNICODE \_ RANGE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) especifica el intervalo de puntos de código Unicode. |



 

