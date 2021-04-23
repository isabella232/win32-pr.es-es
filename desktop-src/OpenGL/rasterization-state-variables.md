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
ms.openlocfilehash: 6210f93c23dc52f19f3e01ea01ebe8fc9d631c8c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909843"
---
# <a name="rasterization-state-variables"></a>Variables de estado de rasterización

<dl> <dt><span id="GL_POINT_SIZE"></span><span id="gl_point_size"></span>TAMAÑO \_ DE PUNTO DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Tamaño del punto                         |
| Grupo de atributos: | point                              |
| Valor inicial:   | 1.0                                |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_POINT_SMOOTH"></span><span id="gl_point_smooth"></span>GL \_ POINT \_ SMOOTH</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Alias de punto en                  |
| Grupo de atributos: | point/enable                       |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_WIDTH"></span><span id="gl_line_width"></span>ANCHO \_ DE LÍNEA DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Ancho de línea                                                                     |
| Grupo de atributos: | line                                                                           |
| Valor inicial:   | 1.0                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_SMOOTH"></span><span id="gl_line_smooth"></span>GL \_ LINE \_ SMOOTH</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Suavizado de contorno de línea en               |
| Grupo de atributos: | line/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_PATTERN"></span><span id="gl_line_stipple_pattern"></span>PATRÓN \_ DE \_ STIPPLE DE LÍNEA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Tipple de línea                                                                     |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE_REPEAT"></span><span id="gl_line_stipple_repeat"></span>GL \_ LINE \_ STIPPLE \_ REPEAT</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Repetición de latippla de línea                                                              |
| Grupo de atributos: | line                                                                             |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LINE_STIPPLE"></span><span id="gl_line_stipple"></span>GL \_ LINE \_ STIPPLE</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Habilitación de la información sobre la línea                |
| Grupo de atributos: | line/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE"></span><span id="gl_cull_face"></span>GL \_ CULL \_ FACE</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Selección de polígono habilitada            |
| Grupo de atributos: | polygon/enable                     |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_CULL_FACE_MODE"></span><span id="gl_cull_face_mode"></span>GL \_ CULL \_ FACE \_ MODE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Polígonos orientados hacia delante y hacia atrás de Cull                                           |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | GL \_ BACK                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_FRONT_FACE"></span><span id="gl_front_face"></span>GL \_ FRONT \_ FACE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Indicador cw/CCW de la cara frontal del polígono                                              |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | GL \_ CCW                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_SMOOTH"></span><span id="gl_polygon_smooth"></span>GL \_ POLYGON \_ SMOOTH</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Suavizado de contorno de polígono en            |
| Grupo de atributos: | polygon/enable                     |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_POLYGON_MODE"></span><span id="gl_polygon_mode"></span>MODO \_ DE POLÍGONO DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Modo de rasterización de polígono (delante y atrás)                                      |
| Grupo de atributos: | polygon                                                                          |
| Valor inicial:   | GL \_ FILL                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_POLYGON_STIPPLE"></span><span id="gl_polygon_stipple"></span>GL \_ POLYGON \_ STIPPLE</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Habilitación de latippla de polígono             |
| Grupo de atributos: | polygon/enable                     |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 



| Propiedad | Value |
|------------------|----------------------------------------------------|
| Descripción:     | Patrón detippla de polígono                            |
| Grupo de atributos: | polygon-stipple                                    |
| Valor inicial:   | 1                                                |
| Comando Get:     | [**glGetPolygonStipple**](glgetpolygonstipple.md) |



 

</dd> </dl>

 

 




