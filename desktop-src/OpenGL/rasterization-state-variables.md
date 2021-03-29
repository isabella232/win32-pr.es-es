---
title: Variables de estado de rasterización
description: Variables de estado de rasterización
ms.assetid: 57ce3dc0-3983-449a-bbe1-153232727ff8
keywords:
- Variables de estado de rasterización OpenGL
topic_type:
- apiref
api_name:
- Rasterization State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a1667c530ea1db8c9e463be0edad5de98e8b107
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103784036"
---
# <a name="rasterization-state-variables"></a>Variables de estado de rasterización

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>tamaño de los puntos de contabilidad \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Tamaño del punto                         |
| Grupo de atributos: | point                              |
| Valor inicial:   | 1,0                                |
| Obtener comando:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>\_suavidad de punto de contabilidad \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Alias de punto activado                  |
| Grupo de atributos: | señalar/habilitar                       |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>\_ancho de línea de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Ancho de línea                                                                     |
| Grupo de atributos: | line                                                                           |
| Valor inicial:   | 1,0                                                                            |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>\_suavizado de línea de contabilidad \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Suavizado de línea en               |
| Grupo de atributos: | línea/habilitar                        |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>\_ \_ patrón punteado de línea de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Línea punteada                                                                     |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                              |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>\_ \_ repetición punteada de línea de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Repetición punteada de línea                                                              |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>línea de contabilidad \_ \_ punteada</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Habilitar línea punteada                |
| Grupo de atributos: | línea/habilitar                        |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>\_cara de selección de contabilidad \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Selección de polígonos habilitada            |
| Grupo de atributos: | Polígono/habilitar                     |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>\_modo de \_ cara de selección de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Desactivación de polígonos hacia delante o hacia atrás                                           |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | libro \_ de contabilidad                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>\_cara frontal de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Indicador de la cara frontal CW/CCW                                              |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | CCW de contabilidad \_                                                                          |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>retorno de polígono de GL \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Suavizado de contorno de polígono activado            |
| Grupo de atributos: | Polígono/habilitar                     |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>\_modo de polígono de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Modo de rasterización de Polígono (anverso y trasero)                                      |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | relleno de contabilidad \_                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>punteado de cont. \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Habilitar polígono punteado             |
| Grupo de atributos: | Polígono/habilitar                     |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 



|                  |                                                    |
|------------------|----------------------------------------------------|
| Descripción:     | Patrón punteado de polígono                            |
| Grupo de atributos: | Polígono-punteado                                    |
| Valor inicial:   | 1                                                |
| Obtener comando:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




