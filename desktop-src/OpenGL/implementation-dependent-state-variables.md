---
title: Variables de estado de Implementation-Dependent
description: Variables de estado de Implementation-Dependent
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Variables de estado de Implementation-Dependent OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: afb42c13765678218efcaf58f2b02a01d2f0e160
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076764"
---
# <a name="implementation-dependent-state-variables"></a>Variables de estado de Implementation-Dependent

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>\_luces máximas de GL \_</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Descripción:     | Número máximo de luces               |
| Grupo de atributos: |                                        |
| Valor inicial:   | 8                                      |
| Obtener comando:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>\_planos de \_ recortes Max de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Número máximo de planos de recorte de usuarios                                           |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 6                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>\_profundidad máxima de la \_ \_ pila MODELVIEW \_ de GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila MODELVIEW                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>\_profundidad máxima de la \_ pila de proyección de \_ GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila de la matriz de proyección                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>\_profundidad máxima de la \_ pila de textura de \_ GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila de la matriz de textura                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>\_bits de SUBpíxeles de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Número de bits de precisión de subpíxeles en *x*   e *y*                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 4                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>\_tamaño máximo de \_ textura \_ de GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Alto o ancho máximo de una imagen de textura (sin bordes)                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>\_tabla de \_ mapa de píxeles Max \_ de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Tamaño máximo de una tabla de traducción de **glPixelMap**                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>\_profundidad máxima de la \_ pila de nombres de \_ GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Selección máxima: profundidad de la pila de nombres                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_anidamiento de \_ lista \_ Max de GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Anidamiento de llamadas de lista de visualización máxima                                                |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>\_orden de \_ evaluación \_ Max de GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Orden Polinómico de evaluador máximo                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 8                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>la \_ ventanilla Max de GL está \_ \_ atenuada</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Dimensiones máximas de la ventanilla                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>\_profundidad máxima de la \_ \_ pila atrib \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila de atributos                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 16                                                                               |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>\_búferes auxiliares de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Número de búferes auxiliares                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 0                                                                                |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>\_modo RGBA de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | True si los búferes de color almacenan RGBA                                                 |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>\_modo de índice de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | True si los búferes de color almacenan índices                                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | True si existen búferes Front y back                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>estéreo de GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | True si existen los búferes izquierdo y derecho                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>\_intervalo de \_ tamaño de punto de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Intervalo (de baja a alta) de tamaños de punto con suavizado                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1,1                                                                           |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>\_granularidad de \_ tamaño de punto de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Granularidad de tamaño de punto de suavizado                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>\_rango de \_ ancho de línea de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Intervalo (de baja a alta) de ancho de línea con suavizado de contorno                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1,1                                                                           |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>\_granularidad de \_ ancho de línea de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Granularidad de ancho de línea antialias                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




