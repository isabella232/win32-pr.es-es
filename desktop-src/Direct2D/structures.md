---
title: Estructuras de Direct2D
description: Direct2D proporciona las siguientes estructuras. Las estructuras adicionales se definen en el espacio de nombres D2D1.
ms.assetid: 6c34a8c8-4b0b-4a95-8f13-25ca25c370ba
keywords:
- Direct2D, estructuras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba4b668e143b3ab5b166582e504c68a05722da7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685714"
---
# <a name="direct2d-structures"></a>Estructuras de Direct2D

Direct2D proporciona las siguientes estructuras. Las estructuras adicionales se definen en el [espacio de nombres D2D1](d2d1-namespace.md).

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**\_Color \_ F de D2D**](d2d-color-f.md) | Describe los componentes rojo, verde, azul y alfa de un color. |
| [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) | Representa una matriz de 3 por 2. |
| [**D2D \_ Matrix \_ 4X3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f) | Describe una matriz de punto flotante de 4 por 3. |
| [**\_Matriz D2D \_ 4x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x4_f) | Describe una matriz de punto flotante de 4 por 4. |
| [**D2D \_ Matrix \_ 5x4 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_5x4_f) | Describe una matriz de punto flotante de 5 por 4. |
| [**\_Punto D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2f) | Representa un par de coordenada x e y, expresado como valores de punto flotante, en el espacio bidimensional. |
| [**D2D \_ punto \_ 2L**](/previous-versions/windows/desktop/legacy/jj219217(v=vs.85)) | La \_ \_ estructura de D2D Point 2L define las coordenadas x e y de un punto. |
| [**Punto de D2D \_ \_ 2U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_point_2u) | Representa un par de coordenada x e y, expresado como un valor entero de 32 bits sin signo, en el espacio bidimensional. |
| [**D2D \_ Rect \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) | Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).  |
| [**D2D \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) | La estructura [**D2D \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/jj244059(v=vs.85)) define las coordenadas de las esquinas superior izquierda e inferior derecha de un rectángulo. |
| [**D2D \_ Rect \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_u) | Representa un rectángulo definido por el par de esquina superior izquierda de las coordenadas (izquierda, superior) y el par de esquina inferior derecha de las coordenadas (derecha, inferior). Estas coordenadas se expresan como valores enteros de 32 bits. |
| [**Tamaño de D2D \_ \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_f) | Almacena un par ordenado de valores de punto flotante, normalmente el ancho y el alto de un rectángulo.  |
| [**Tamaño de D2D \_ \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u) | Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo. |
| [**\_Vector D2D \_ 2F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_2f) | Vector 2D compuesto por dos valores de punto flotante de precisión sencilla (x, y).  |
| [**\_Vector D2D \_ 3F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_3f) | Vector 3D que consta de tres valores de punto flotante de precisión sencilla (x, y, z). |
| [**D2D \_ Vector \_ 4F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_vector_4f) | Un vector 4D que consta de cuatro valores de punto flotante de precisión sencilla (x, y, z, w). |
| [**\_Segmento de arco D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_arc_segment) | Describe un arco elíptico entre dos puntos. |
| [**D2D1 \_ \_ segmento Bézier**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) | Representa un segmento de Bézier cúbica dibujada entre dos puntos. |
| [**Propiedades del pincel de mapa de \_ bits D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) | Describe los modos de extensión y el modo de interpolación de un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**D2D1 \_ pincel de mapa de bits \_ \_ PROPERTIES1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_brush_properties1) | Describe los modos de extensión y el modo de interpolación de un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush). |
| [**\_Propiedades de mapa de bits D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bitmap_properties) | Describe el formato de píxel y el PPP de un mapa de bits. |
| [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) | Esta estructura permite crear un [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1) con opciones de mapa de bits e información de contexto de color disponible.  |
| [**Descripción de D2D1 \_ Blend \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description) | Define una descripción de Blend que se va a usar en una transformación de Blend determinada. |
| [**\_Propiedades del pincel D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_brush_properties) | Describe la opacidad y la transformación de un pincel. |
| [**\_Color \_ F de D2D1**](d2d1-color-f.md) | Describe los componentes rojo, verde, azul y alfa de un color. |
| [**\_Propiedades de creación de D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_creation_properties) | Especifica las opciones con las que se crean el dispositivo, el generador y el contexto de dispositivo de [Direct2D](./direct2d-portal.md) .  |
| [**\_Propiedades de \_ búfer de vértice personalizado \_ de D2D1 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties) | Define un sombreador de vértices y la descripción del elemento de entrada para definir el diseño de entrada. |
| [**\_Descripción del \_ Estado del dibujo de D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_drawing_state_description) | Describe el estado de dibujo de un destino de representación.  |
| [**D2D1 \_ Estado de dibujo \_ \_ DESCRIPTION1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_drawing_state_description1) | Describe el estado de dibujo de un contexto de dispositivo. |
| [**\_Descripción de \_ entrada de efecto de D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_effect_input_description) | Describe las características de un efecto. |
| [**\_Elipse D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse) | Contiene el punto central, el radio x y el radio y de una elipse. |
| [**\_Opciones de fábrica de D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_factory_options) | Contiene el nivel de depuración de un objeto [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) .  |
| [**D2D1 \_ de \_ datos de características \_ dobles**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_doubles) | Describe la compatibilidad con los dobles en los sombreadores. |
| [**D2D1 de \_ datos de características de \_ \_ D3D10 \_ X \_ Opciones de hardware \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_feature_data_d3d10_x_hardware_options) | Describe la compatibilidad con el sombreador de cálculo, que es una opción en el nivel de características de D3D10. |
| [**Revisión de la \_ malla de gradiente D2D1 \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch) | Representa una revisión de tensores con 16 puntos de control, 4 colores de esquina y marcas de límite. Un ID2D1GradientMesh se compone de 1 o más parches de malla de gradiente. Use la [**función GradientMeshPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatch) o la [**función GradientMeshPatchFromCoonsPatch**](/windows/desktop/api/d2d1_3helper/nf-d2d1_3helper-gradientmeshpatchfromcoonspatch) para crear una.  |
| [**D2D1 delimitador de \_ degradado \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_gradient_stop) | Contiene la posición y el color de un delimitador de degradado.  |
| [**\_Propiedades de \_ destino de representación de HWND D2D1 \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) | Contiene las opciones HWND, tamaño de píxel y presentación para un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget). |
| [**D2D1 \_ \_ propiedades de estilo de tinta \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_style_properties) | Define la forma general de la sugerencia de lápiz y la transformación utilizada en un objeto [**ID2D1InkStyle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle) .  |
| [**\_Propiedades del \_ pincel de imagen D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_image_brush_properties) | Describe las características del pincel de imagen. |
| [**D2D1 \_ \_ segmento Bézier de tinta \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment) | Representa un segmento Bézier que se va a utilizar en la creación de un objeto [**ID2D1Ink**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink) . Esta estructura difiere del [**\_ \_ segmento de Bézier D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_bezier_segment) en que se compone de [**D2D1 \_ de \_ punto de tinta**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point), que contienen un radio además de las coordenadas x e y.  |
| [**D2D1 \_ punto de tinta \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_point) | Representa un par de punto y radio que forma parte de un [**\_ segmento de \_ Bézier \_ de tinta de D2D1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_ink_bezier_segment). |
| [**\_Descripción de entrada de D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_description) | Describe las opciones que las transformaciones pueden establecer en las texturas de entrada. |
| [**\_Descripción del \_ elemento de entrada D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_input_element_desc) | Una descripción de un solo elemento para el diseño de vértices. |
| [**Parámetros de la \_ capa D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) | Contiene los límites de contenido, la información de máscara, la configuración de opacidad y otras opciones de un recurso de capa.  |
| [**Nivel de D2D1 \_ \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) | Contiene los límites de contenido, la información de máscara, la configuración de opacidad y otras opciones de un recurso de capa. |
| [**D2D1 \_ \_ propiedades del pincel de degradado lineal \_ \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) | Contiene el punto inicial y el punto de conexión del eje de degradado para un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).  |
| [**D2D1 \_ Matrix \_ 3x2 \_ F**](d2d1-matrix-3x2-f.md) | Representa una matriz de 3 por 2.  |
| [**D2D1 \_ Matrix \_ 4X3 \_ F**](d2d1-matrix-4x3-f.md) | Representa una matriz de 4 por 3.  |
| [**\_Matriz D2D1 \_ 4x4 \_ F**](d2d1-matrix-4x4-f.md) | Representa una matriz de 4 por 4.  |
| [**D2D1 \_ Matrix \_ 5x4 \_ F**](d2d1-matrix-5x4-f.md) | Representa una matriz de 5 por 4.  |
| [**D2D1 \_ de \_ rectángulo asignado**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_mapped_rect) | Describe la memoria asignada de la API [**ID2D1Bitmap1:: Map**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1bitmap1-map) . |
| [**\_Formato de píxel de D2D1 \_**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) | Contiene el formato de datos y el modo alfa para un mapa de bits o un destino de representación.  |
| [**\_Punto D2D1 \_ 2F**](d2d1-point-2f.md) | Representa un par de coordenadas x e y en un espacio bidimensional. |
| [**D2D1 \_ punto \_ 2L**](/previous-versions/windows/desktop/legacy/hh847948(v=vs.85)) | La estructura POINT define las coordenadas x e y de un punto. |
| [**Punto de D2D1 \_ \_ 2U**](d2d1-point-2u.md) | Representa un par de coordenadas x e y en un espacio bidimensional.  |
| [**\_Descripción del punto de D2D1 \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_point_description) | Describe un punto en una geometría de trazado. |
| [**D2D1 \_ \_ propiedades del control de impresión \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_print_control_properties) | Las propiedades de creación de un objeto [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol) . |
| [**Enlace de la \_ propiedad D2D1 \_**](/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_property_binding) | Define un enlace de propiedad a un par de funciones que obtienen y establecen la propiedad correspondiente.  |
| [**D2D1 \_ \_ segmento Bézier cuadrático \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_quadratic_bezier_segment) | Contiene el punto de control y el punto final de un segmento de Bézier cuadrática. |
| [**\_Propiedades del \_ pincel de degradado radial de \_ D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) | Contiene el desplazamiento del origen del degradado y el tamaño y la posición de la elipse de degradado para un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).  |
| [**D2D1 \_ Rect \_ F**](d2d1-rect-f.md) | Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).  |
| [**D2D1 \_ Rect \_ L**](/previous-versions/windows/desktop/legacy/hh847950(v=vs.85)) | La estructura RECT define las coordenadas de las esquinas superior izquierda e inferior derecha de un rectángulo. |
| [**D2D1 \_ Rect \_ U**](d2d1-rect-u.md) | Representa un rectángulo definido por las coordenadas de la esquina superior izquierda (izquierda, superior) y las coordenadas de la esquina inferior derecha (derecha, inferior).  |
| [**Propiedades de la \_ textura de recursos D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_resource_texture_properties) | Define una textura de recursos cuando se crea la textura de recursos original. |
| [**\_Uso de recursos de D2D1 \_**](/previous-versions/windows/desktop/legacy/hh404326(v=vs.85)) | Describe la memoria utilizada por las texturas y los sombreadores de la imagen. |
| [**\_Propiedades de \_ destino de representación de D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) | Contiene opciones de representación (hardware o software), formato de píxeles, información de PPP, opciones de comunicación remota y requisitos de compatibilidad de Direct3D para un destino de representación.  |
| [**Controles de representación de D2D1 \_ \_**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_rendering_controls) | Describe las limitaciones que se aplicarán a un representador de efectos de imagen. |
| [**D2D1 \_ rectángulo redondeado \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_rounded_rect) | Contiene las dimensiones y los radios de esquina de un rectángulo redondeado. |
| [**\_Perfil de \_ color \_ simple de D2D1**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_simple_color_profile) | Descripción simple de un espacio de colores. |
| [**Tamaño de D2D1 \_ \_ F**](d2d1-size-f.md) | Almacena un par ordenado de flotantes, normalmente el ancho y el alto de un rectángulo. |
| [**Tamaño de D2D1 \_ \_ U**](d2d1-size-u.md) | Almacena un par de enteros ordenados, normalmente el ancho y el alto de un rectángulo. |
| [**\_Propiedades de \_ estilo de trazo de D2D1 \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_stroke_style_properties) | Describe el trazo que esquematiza una forma.  |
| [**D2D1 \_ estilo de trazo \_ \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_stroke_style_properties1) | Describe el trazo que esquematiza una forma. |
| [**\_Longitud de SVG de D2D1 \_**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_length) | Representa una longitud de SVG. |
| [**D2D1 \_ \_ formato SVG \_ conservar \_ relación de aspecto**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_preserve_aspect_ratio) | Representa todos los valores de preserveAspectRatio SVG. |
| [**D2D1 \_ SVG \_ VIEWBOX**](/windows/desktop/api/d2d1svg/ns-d2d1svg-d2d1_svg_viewbox) | Representa un viewBox de SVG. |
| [**Propiedades de origen de la \_ imagen transformada D2D1 \_ \_ \_**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_transformed_image_source_properties) | Propiedades de un origen de imagen transformado. |
| [**\_Triángulo D2D1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_triangle) | Contiene los tres vértices que describen un triángulo. |
| [**\_Vector D2D1 \_ 2F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_2f) | Vector de 2 valores FLOAT (x, y). |
| [**\_Vector D2D1 \_ 3F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_3f) | Vector de 3 valores FLOAT (x, y, z). |
| [**D2D1 \_ Vector \_ 4F**](/windows/win32/api/dcommon/ns-dcommon-d2d_vector_4f) | Vector de 4 valores FLOAT (x, y, z, w). |
| [**\_Propiedades de búfer de vértices D2D1 \_ \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties) | Define las propiedades de un búfer de vértice que son estándar para todas las definiciones de sombreador de vértices. |
| [**\_Rango de vértices de D2D1 \_**](/windows/desktop/api/D2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range) | Define un intervalo de vértices que se usa al representar un número menor que el contenido completo de un búfer de vértice. |
| [**D3DCOLORVALUE**](/previous-versions/windows/desktop/legacy/dd368193(v=vs.85)) | Almacena información de color y de canal alfa. |
| [*\_Generador de efectos de PD2D1 \_*](/windows/desktop/api/D2D1_1/nc-d2d1_1-pd2d1_effect_factory) | Describe la implementación de un efecto. |