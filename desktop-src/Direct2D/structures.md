---
title: Estructuras de Direct2D
description: Direct2D proporciona las estructuras siguientes. Las estructuras adicionales se definen en el espacio de nombres D2D1.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6be3735335abc5b9242ec150ac583f837ae5c15936aaca677b322526b1c19f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537705"
---
# <a name="direct2d-structures"></a>Estructuras de Direct2D

Direct2D proporciona las estructuras siguientes. Las estructuras adicionales se definen en el espacio [de nombres D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**D2D \_ COLOR \_ F**](d2d-color-f.md) | Describe los componentes rojo, verde, azul y alfa de un color. |
| [**MATRIZ D2D \_ \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Representa una matriz de 3 por 2. |
| [**MATRIZ D2D \_ \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Describe una matriz de punto flotante de 4 por 3. |
| [**MATRIZ D2D \_ \_ 4X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Describe una matriz de punto flotante de 4 por 4. |
| [**MATRIZ D2D \_ \_ 5X4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Describe una matriz de punto flotante de 5 por 4. |
| [**D2D \_ POINT \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Representa un par de coordenadas X e y coordenadas, expresados como valores de punto flotante, en un espacio bidimensional. |
| [**D2D \_ POINT \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | La estructura D2D \_ POINT \_ 2L define las coordenadas x e y de un punto. |
| [**D2D \_ POINT \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Representa un par de coordenadas x e y coordenadas, expresado como un valor entero de 32 bits sin signo, en un espacio bidimensional. |
| [**D2D \_ RECT \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).  |
| [**D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | La [**estructura D2D \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) define las coordenadas de las esquinas superior izquierda e inferior derecha de un rectángulo. |
| [**D2D \_ RECT \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Representa un rectángulo definido por el par de coordenadas de la esquina superior izquierda (izquierda, superior) y el par de coordenadas de la esquina inferior derecha (derecha, inferior). Estas coordenadas se expresan como valores enteros de 32 bits. |
| [**D2D \_ SIZE \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Almacena un par ordenado de valores de punto flotante, normalmente el ancho y alto de un rectángulo.  |
| [**D2D \_ SIZE \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo. |
| [**VECTOR \_ \_ 2F D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Vector 2D que consta de dos valores de punto flotante de precisión sencilla (x, y).  |
| [**VECTOR \_ 3F D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Vector 3D que consta de tres valores de punto flotante de precisión sencilla (x, y, z). |
| [**VECTOR \_ 4F D2D \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Vector 4D que consta de cuatro valores de punto flotante de precisión sencilla (x, y, z, w). |
| [**SEGMENTO DE ARC D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Describe un arco elíptico entre dos puntos. |
| [**SEGMENTO BÉZIER D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Representa un segmento bézier cúbica dibujado entre dos puntos. |
| [**PROPIEDADES DEL PINCEL DE MAPA DE BITS D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Describe los modos de extensión y el modo de interpolación de [**un objeto ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) |
| [**D2D1 \_ BITMAP \_ BRUSH \_ PROPERTIES1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Describe los modos de extensión y el modo de interpolación de [**un objeto ID2D1BitmapBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) |
| [**PROPIEDADES DE MAPA DE BITS D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Describe el formato de píxel y los ppp de un mapa de bits. |
| [**D2D1 \_ BITMAP \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Esta estructura permite crear un [**ID2D1Bitmap1 con**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) opciones de mapa de bits e información de contexto de color disponible.  |
| [**DESCRIPCIÓN DE BLEND D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Define una descripción de mezcla que se va a usar en una transformación de mezcla determinada. |
| [**PROPIEDADES DE PINCEL D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Describe la opacidad y transformación de un pincel. |
| [**D2D1 \_ COLOR \_ F**](d2d1-color-f.md) | Describe los componentes rojo, verde, azul y alfa de un color. |
| [**PROPIEDADES DE CREACIÓN DE D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | Especifica las opciones con las que se crean el dispositivo [Direct2D,](./direct2d-portal.md) la fábrica y el contexto del dispositivo.  |
| [**PROPIEDADES PERSONALIZADAS DEL BÚFER DE \_ \_ \_ VÉRTICES D2D1 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Define un sombreador de vértices y la descripción del elemento de entrada para definir el diseño de entrada. |
| [**D2D1 \_ DRAWING \_ STATE \_ DESCRIPTION**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Describe el estado de dibujo de un destino de representación.  |
| [**D2D1 \_ DRAWING \_ STATE \_ DESCRIPTION1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Describe el estado de dibujo de un contexto de dispositivo. |
| [**DESCRIPCIÓN DE ENTRADA DEL EFECTO D2D1 \_ \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Describe las características de un efecto. |
| [**ELIPSE D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Contiene el punto central, el radio X y el radio Y de una elipse. |
| [**OPCIONES DE GENERADOR D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Contiene el nivel de depuración de [**un objeto ID2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)  |
| [**D2D1 \_ FEATURE \_ DATA \_ DOUBLES**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Describe la compatibilidad con los dobles en sombreadores. |
| [**D2D1 \_ FEATURE \_ DATA \_ D3D10 \_ X \_ HARDWARE \_ OPTIONS**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Describe la compatibilidad con el sombreador de proceso, que es una opción en el nivel de característica D3D10. |
| [**REVISIÓN DE MALLA DE DEGRADADO D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Representa una revisión de tensor con 16 puntos de control, 4 colores de esquina y marcas de límite. Id2D1GradientMesh se consiente de 1 o más revisiones de malla de degradado. Use la [**función GradientMeshPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) o la [**función GradientMeshPatchFromCoonsPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) para crear una.  |
| [**D2D1 \_ GRADIENT \_ STOP**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Contiene la posición y el color de un delimitador de degradado.  |
| [**PROPIEDADES DE DESTINO DE \_ REPRESENTACIÓN DE HWND D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Contiene las opciones HWND, tamaño de píxel y presentación de [**id2D1HwndRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) |
| [**PROPIEDADES DE ESTILO DE LÁPIZ D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Define la forma general de la punta de lápiz y la transformación utilizada en un [**objeto ID2D1InkStyle.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)  |
| [**PROPIEDADES DEL PINCEL DE IMAGEN D2D1 \_ \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Describe las características del pincel de imagen. |
| [**SEGMENTO D2D1 \_ INK \_ BEZIER \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Representa un segmento Bézier que se va a usar en la creación de un [**objeto ID2D1Ink.**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) Esta estructura difiere de [**D2D1 \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) en que se compone de [**D2D1 \_ INK \_ POINT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point)s, que contienen un radio además de las coordenadas x e y.  |
| [**PUNTO DE ENTRADA DE LÁPIZ D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Representa un par de punto y radio que forma parte de un [**segmento D2D1 \_ INK \_ BEZIER \_ SEGMENT**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment). |
| [**D2D1 \_ INPUT \_ DESCRIPTION**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Describe las opciones que las transformaciones pueden establecer en las texturas de entrada. |
| [**D2D1 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Descripción de un único elemento para el diseño del vértice. |
| [**PARÁMETROS DE CAPA D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Contiene los límites de contenido, la información de máscara, la configuración de opacidad y otras opciones para un recurso de capa.  |
| [**PARÁMETROS DE CAPA D2D11 \_ \_**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Contiene los límites de contenido, la información de máscara, la configuración de opacidad y otras opciones para un recurso de capa. |
| [**PROPIEDADES DEL PINCEL DE DEGRADADO LINEAL D2D1 \_ \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Contiene el punto inicial y el punto de conexión del eje de degradado para [**un objeto ID2D1LinearGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)  |
| [**MATRIZ D2D1 \_ \_ 3X2 \_ F**](d2d1-matrix-3x2-f.md) | Representa una matriz de 3 por 2.  |
| [**MATRIZ D2D1 \_ \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | Representa una matriz de 4 por 3.  |
| [**MATRIZ D2D1 \_ \_ 4X4 \_ F**](d2d1-matrix-4x4-f.md) | Representa una matriz de 4 por 4.  |
| [**MATRIZ D2D1 \_ \_ 5X4 \_ F**](d2d1-matrix-5x4-f.md) | Representa una matriz de 5 por 4.  |
| [**D2D1 \_ MAPPED \_ RECT**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Describe la memoria asignada de [**ID2D1Bitmap1::Map**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) API. |
| [**FORMATO DE PÍXELES D2D1 \_ \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Contiene el formato de datos y el modo alfa para un mapa de bits o un destino de representación.  |
| [**D2D1 \_ POINT \_ 2F**](d2d1-point-2f.md) | Representa un par de coordenadas X e y coordenadas en un espacio bidimensional. |
| [**D2D1 \_ POINT \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | La estructura POINT define las coordenadas x e y de un punto. |
| [**D2D1 \_ POINT \_ 2U**](d2d1-point-2u.md) | Representa un par de coordenadas X e y coordenadas en un espacio bidimensional.  |
| [**DESCRIPCIÓN DEL PUNTO D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Describe un punto en una geometría de ruta de acceso. |
| [**PROPIEDADES DEL CONTROL DE IMPRESIÓN D2D1 \_ \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | Propiedades de creación de un [**objeto ID2D1PrintControl.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) |
| [**ENLACE DE PROPIEDADES D2D1 \_ \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Define un enlace de propiedad a un par de funciones que obtienen y establecen la propiedad correspondiente.  |
| [**SEGMENTO D2D1 \_ QUADRATIC \_ BEZIER \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Contiene el punto de control y el punto final de un segmento Bézier cuadrático. |
| [**PROPIEDADES DEL PINCEL \_ DE DEGRADADO RADIAL D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Contiene el desplazamiento de origen del degradado y el tamaño y la posición de la elipse de degradado para [**un objeto ID2D1RadialGradientBrush.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)  |
| [**D2D1 \_ RECT \_ F**](d2d1-rect-f.md) | Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).  |
| [**D2D1 \_ RECT \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | La estructura RECT define las coordenadas de las esquinas superior izquierda e inferior derecha de un rectángulo. |
| [**D2D1 \_ RECT \_ U**](d2d1-rect-u.md) | Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).  |
| [**PROPIEDADES DE TEXTURA DE RECURSOS D2D1 \_ \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Define una textura de recurso cuando se crea la textura del recurso original. |
| [**USO DE RECURSOS D2D1 \_ \_**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Describe la memoria utilizada por las texturas de imagen y los sombreadores. |
| [**PROPIEDADES DE DESTINO DE REPRESENTACIÓN DE D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Contiene opciones de representación (hardware o software), formato de píxel, información de PPP, opciones de comunicación remota y requisitos de compatibilidad de Direct3D para un destino de representación.  |
| [**CONTROLES DE REPRESENTACIÓN D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Describe las limitaciones que se deben aplicar a un representador de efectos de creación de imágenes. |
| [**D2D1 \_ ROUNDED \_ RECT**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Contiene las dimensiones y los radios de esquina de un rectángulo redondeado. |
| [**PERFIL DE \_ COLOR SIMPLE D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Descripción simple de un espacio de colores. |
| [**D2D1 \_ SIZE \_ F**](d2d1-size-f.md) | Almacena un par ordenado de flotantes, normalmente el ancho y alto de un rectángulo. |
| [**D2D1 \_ SIZE \_ U**](d2d1-size-u.md) | Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo. |
| [**PROPIEDADES DE ESTILO DE TRAZO D2D1 \_ \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Describe el trazo que describe una forma.  |
| [**D2D1 PROPIEDADES DE \_ ESTILO \_ DE \_ TRAZO1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Describe el trazo que describe una forma. |
| [**LONGITUD SVG \_ D2D1 \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Representa una longitud SVG. |
| [**RELACIÓN DE ASPECTO DE \_ CONSERVACIÓN DE SVG D2D1 \_ \_ \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Representa toda la configuración de SVG preserveAspectRatio. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Representa un viewBox SVG. |
| [**PROPIEDADES DEL ORIGEN DE \_ LA IMAGEN TRANSFORMADA D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Propiedades de un origen de imagen transformado. |
| [**TRIÁNGULO D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Contiene los tres vértices que describen un triángulo. |
| [**D2D1 \_ VECTOR \_ 2F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Vector de 2 valores FLOAT (x, y). |
| [**D2D1 \_ VECTOR \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Vector de 3 valores FLOAT (x, y, z). |
| [**D2D1 \_ VECTOR \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Vector de 4 valores FLOAT (x, y, z, w). |
| [**PROPIEDADES DEL BÚFER DE \_ \_ VÉRTICES D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Define las propiedades de un búfer de vértices que son estándar para todas las definiciones de sombreador de vértices. |
| [**INTERVALO DE VÉRTICES D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Define un intervalo de vértices que se usan al representar menos que el contenido completo de un búfer de vértices. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Almacena información de color y canal alfa. |
| [*PD2D1 \_ EFFECT \_ FACTORY*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Describe la implementación de un efecto. |