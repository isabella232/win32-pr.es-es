---
title: Variables de estado dependientes de la implementación
description: Variables de estado dependientes de la implementación
ms.assetid: 6778b50c-a6ac-4106-9dd6-3a123c257687
keywords:
- Implementation-Dependent State Variables OpenGL
topic_type:
- apiref
api_name:
- Implementation-Dependent State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 645702c9ea91f21d0e3bce5233b8014fd8f86859
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259916"
---
# <a name="implementation-dependent-state-variables"></a>Variables de estado dependientes de la implementación

<dl> <dt><span id="GL_MAX_LIGHTS"></span><span id="gl_max_lights"></span>GL \_ MAX \_ LIGHTS</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------|
| Descripción:     | Número máximo de luces               |
| Grupo de atributos: |                                        |
| Valor inicial:   | 8                                      |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_CLIP_PLANES"></span><span id="gl_max_clip_planes"></span>GL \_ MAX \_ CLIP \_ PLANES</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Número máximo de planos de recorte de usuarios                                           |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 6                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_MODELVIEW_STACK_DEPTH"></span><span id="gl_max_modelview_stack_depth"></span>PROFUNDIDAD \_ DE PILA DE GL MAX \_ MODELVIEW \_ \_</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila modelview-matrix                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PROJECTION_STACK_DEPTH"></span><span id="gl_max_projection_stack_depth"></span>PROFUNDIDAD \_ DE PILA DE \_ \_ PROYECCIÓN MÁXIMA \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila de la matriz de proyección                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_STACK_DEPTH"></span><span id="gl_max_texture_stack_depth"></span>PROFUNDIDAD \_ DE LA PILA DE TEXTURA MÁXIMA \_ \_ \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila de matriz de textura                                            |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 2                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_SUBPIXEL_BITS"></span><span id="gl_subpixel_bits"></span>BITS \_ DE SUBPIXEL DE GL \_</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Número de bits de precisión de subpixel *en x* e *y*                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 4                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_TEXTURE_SIZE"></span><span id="gl_max_texture_size"></span>TAMAÑO \_ MÁXIMO DE TEXTURA \_ \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Alto o ancho máximo de una imagen de textura (sin bordes)                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_PIXEL_MAP_TABLE"></span><span id="gl_max_pixel_map_table"></span>TABLA \_ DE MAPA DE \_ \_ PÍXELES MÁXIMO \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Tamaño máximo de una **tabla de traducción glPixelMap**                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 32                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_NAME_STACK_DEPTH"></span><span id="gl_max_name_stack_depth"></span>PROFUNDIDAD DE \_ PILA \_ DE NOMBRES \_ MÁXIMOS DE \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad de pila de nombre de selección máxima                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_LIST_NESTING"></span><span id="gl_max_list_nesting"></span>\_ANIDAMIENTO \_ DE LISTAS \_ DE GL MAX</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Anidamiento máximo de llamadas de lista de visualización                                                |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 64                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_EVAL_ORDER"></span><span id="gl_max_eval_order"></span>GL \_ MAX \_ EVAL \_ ORDER</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Orden polinómico máximo del evaluador                                               |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 8                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_VIEWPORT_DIMS"></span><span id="gl_max_viewport_dims"></span>GL \_ MAX \_ VIEWPORT \_ DIMS</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Dimensiones máximas de ventanilla                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAX_ATTRIB_STACK_DEPTH"></span><span id="gl_max_attrib_stack_depth"></span>PROFUNDIDAD \_ DE PILA DE GL MAX \_ ATTRIB \_ \_</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Profundidad máxima de la pila de atributos                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 16                                                                               |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUX_BUFFERS"></span><span id="gl_aux_buffers"></span>BÚFERES \_ \_ AUXILIARES GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Número de búferes auxiliares                                                      |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_RGBA_MODE"></span><span id="gl_rgba_mode"></span>MODO \_ RGBA \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | True si los búferes de color almacenan RGBA                                                 |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_MODE"></span><span id="gl_index_mode"></span>MODO \_ DE ÍNDICE \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | True si los búferes de color almacenan índices                                              |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DOUBLEBUFFER"></span><span id="gl_doublebuffer"></span>GL \_ DOUBLEBUFFER</dt> <dd> 

| Propiedad. | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | True si existen búferes front-and-back                                             |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STEREO"></span><span id="gl_stereo"></span>GL \_ STEREO</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | True si existen búferes izquierdos y derecho                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_RANGE"></span><span id="gl_point_size_range"></span>INTERVALO \_ DE TAMAÑO DE PUNTO DE \_ \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Intervalo (bajo a alto) de tamaños de punto con suavizado de contorno                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POINT_SIZE_GRANULARITY"></span><span id="gl_point_size_granularity"></span>GRANULARIDAD \_ DEL TAMAÑO DEL PUNTO \_ \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Granularidad del tamaño de punto suavizado                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_RANGE"></span><span id="gl_line_width_range"></span>INTERVALO DE \_ ANCHO DE LÍNEA DE \_ \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Intervalo (bajo a alto) de anchos de línea suavizados                                 |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH_GRANULARITY"></span><span id="gl_line_width_granularity"></span>GRANULARIDAD \_ DEL ANCHO DE LÍNEA \_ \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Granularidad de ancho de línea suavizado                                             |
| Grupo de atributos: |                                                                                |
| Valor inicial:   |                                                                                |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




