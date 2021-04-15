---
title: Estructuras de DirectWrite
description: DirectWrite define las siguientes estructuras.
ms.assetid: 348dd001-bad9-4f1a-a5f5-84b118a5e2d4
keywords:
- DirectWrite, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea132cde1ea6b740cc02b938767f941e9c999e5a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105689610"
---
# <a name="directwrite-structures"></a>Estructuras de DirectWrite

DirectWrite define las siguientes estructuras.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**DWRITE_BITMAP_DATA_BGRA32**](./dwrite_3/ns-dwrite_3-dwrite_bitmap_data_bgra32.md) | Representa los datos de mapa de bits en formato BGRA32. |
| [**DWRITE \_ métricas de intercalación \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) | La estructura de [**\_ \_ métricas del símbolo de intercalación de DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_caret_metrics) especifica las métricas de la posición del símbolo de intercalación en una fuente. |
| [**\_métricas de clúster de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_cluster_metrics) | Contiene información acerca de un clúster de glifos. |
| [**\_color \_ F de DWRITE**](dwrite-color-f.md) | Describe los componentes rojo, verde, azul y alfa de un color. |
| [**DWRITE \_ \_ ejecución del glifo de color \_**](/windows/win32/api/DWrite_2/ns-dwrite_2-dwrite_color_glyph_run) | Contiene la información necesaria para que los representadores dibujen ejecuciones de glifos con información de color del glifo. |
| [**DWRITE \_ glifo de color \_ \_ RUN1**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_color_glyph_run1) | Representa una ejecución de glifo de color. El método IDWriteFactory4:: TranslateColorGlyphRun devuelve una colección ordenada de ejecuciones de glifos de color de tipos diferentes en función de lo que admita la fuente. |
| [**\_fragmento de archivo DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_file_fragment) | Representa un intervalo de bytes en un archivo de fuente. |
| [**DWRITE_FONT_AXIS_RANGE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range) | Representa el intervalo mínimo y máximo de los valores posibles para un eje de fuente. |
| [**DWRITE_FONT_AXIS_VALUE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) | Representa un valor para un eje de fuentes. Se utiliza al consultar y crear instancias de fuentes. |
| [**\_característica de fuente DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_feature) | Especifica las propiedades que se utilizan para identificar y ejecutar características tipográficas en la fuente actual. |
| [**DWRITE \_ \_ métricas de fuente**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) | La estructura de [**\_ \_ métricas de fuentes DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics) especifica las métricas que se aplican a todos los glifos dentro de la fuente. |
| [**DWRITE \_ Font \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) | La estructura [**DWRITE \_ Font \_ METRICS1**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_font_metrics1) especifica las métricas que se aplican a todos los glifos dentro de la fuente. |
| [**\_propiedad de fuente DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) | Propiedad de fuente usada para filtrar conjuntos de fuentes y generar un conjunto de fuentes con propiedades explícitas. |
| [**\_datos de \_ imagen de GLIFO de DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_glyph_image_data) | Datos para un solo glifo de GetGlyphImageData. |
| [**\_métricas del glifo de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) | Especifica las métricas de un glifo individual. |
| [**\_desplazamiento del glifo de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) | Ajuste opcional a la posición de un glifo. |
| [**\_ejecución del glifo de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) | Contiene la información necesaria para que los representadores dibujen las ejecuciones del glifo. |
| [**\_Descripción de \_ ejecución del GLIFO de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run_description) | Contiene propiedades adicionales relacionadas con las de [**la \_ \_ ejecución del glifo de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run). |
| [**métricas de la prueba de posicionamiento de DWRITE \_ \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_hit_test_metrics) | Describe la región obtenida por una prueba de posicionamiento. |
| [**DWRITE \_ \_ métricas de objeto insertado \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics) | Contiene propiedades que describen la medida geométrica de un objeto insertado definido por la aplicación. |
| [**\_oportunidad de justificación de DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) | La estructura de la [**\_ \_ oportunidad de justificación de DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) especifica la información de justificación por glifo. |
| [**punto de interrupción de \_ línea DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_breakpoint) | Características de punto de interrupción de línea de un carácter. |
| [**\_métricas de línea de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_line_metrics) | Contiene información sobre una línea de texto con formato. |
| [**\_METRICS1 DWRITE line \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1) | Contiene información sobre una línea de texto con formato. |
| [**\_espaciado de línea de DWRITE \_**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_spacing) | |
| [**\_matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) | La estructura de la [**\_ matriz DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) especifica la transformación de gráficos que se va a aplicar a los glifos representados. |
| [**\_métricas salientes de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics) | Indica cuántos DIP visibles (píxeles independientes del dispositivo) sobretoman cada lado del diseño o los objetos insertados. |
| [**DWRITE \_ PAnose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) | La [**DWRITE \_ Panose**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_panose) Union describe los valores de clasificación de tipos de letra que se usan con [**IDWriteFont1:: GetPanose**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefont1-getpanose) para seleccionar y coincidir con la fuente. |
| [**\_análisis de scripts de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) | Almacena la Asociación de texto y su script del sistema de escritura, así como algunos atributos de visualización. |
| [**\_propiedades del script DWRITE \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) | La estructura de [**\_ \_ propiedades del script DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_script_properties) especifica propiedades de script para la exploración y la justificación del símbolo de intercalación. |
| [**\_ \_ propiedades del glifo \_ de forma de DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) | Contiene propiedades de salida de forma para un glifo de salida. |
| [**\_ \_ propiedades de texto \_ de forma DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties) | Dar forma a las propiedades de salida de un glifo de salida. |
| [**\_tachado DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_strikethrough) | Contiene información sobre el tamaño y la posición de los tachados. |
| [**DWRITE \_ \_ métricas de texto**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_metrics) | Contiene las métricas asociadas al texto después del diseño. |
| [**DWRITE \_ Text \_ METRICS1**](/windows/win32/api/dwrite_2/ns-dwrite_2-dwrite_text_metrics1) | Contiene las métricas asociadas al texto después del diseño. |
| [**\_intervalo de texto de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) | Especifica un intervalo de posiciones de texto donde se aplica el formato en el texto representado por un objeto [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) . |
| [**recorte de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_trimming) | Especifica la opción de recorte para el desbordamiento de texto en el cuadro de diseño.  |
| [**\_características tipográficas de DWRITE \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) | Contiene un conjunto de características tipográficas que se van a aplicar durante la forma de texto. |
| [**\_subrayado DWRITE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_underline) | Contiene información sobre el ancho, el grosor, el desplazamiento, el alto de la ejecución, la dirección de lectura y la dirección del flujo de un subrayado.  |
| [**DWRITE \_ intervalo de UNIcode \_**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) | La estructura de [**\_ \_ intervalo Unicode DWRITE**](/windows/win32/api/dwrite_1/ns-dwrite_1-dwrite_unicode_range) especifica el intervalo de puntos de código Unicode. |



 

