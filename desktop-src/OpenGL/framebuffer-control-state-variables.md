---
title: Variables de estado del control fotogramas
description: Variables de estado del control fotogramas
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variables de estado del control fotogramas OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d44327858ae43212fcaa4364ed23045de5e0296f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103903938"
---
# <a name="framebuffer-control-state-variables"></a>Variables de estado del control fotogramas

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>\_búfer de dibujo de GL \_</dt> <dd> 

|                  |                                        |
|------------------|----------------------------------------|
| Descripción:     | Búferes seleccionados para dibujar           |
| Grupo de atributos: | búfer de color                           |
| Valor inicial:   |                                        |
| Obtener comando:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL \_ index \_ WRITEMASK</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Writemask de índice de color                                                            |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | 1                                                                              |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>\_WRITEMASK de color de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | La escritura en color habilita; R, G, B o A                                               |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ true                                                                         |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>profundidad de GL \_ \_ WRITEMASK</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Búfer de profundidad habilitado para escritura                                                 |
| Grupo de atributos: | búfer de profundidad                                                                     |
| Valor inicial:   | GL \_ true                                                                         |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>\_Galería de símbolos GL \_ WRITEMASK</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Cliché-búfer writemask                                                         |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | 1                                                                              |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>\_ \_ valor sin formato de color de GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Valor sin formato del búfer de color (modo RGBA)                                           |
| Grupo de atributos: | búfer de color                                                                   |
| Valor inicial:   | 0, 0, 0, 0                                                                     |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>\_ \_ valor sin formato de índice de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Valor sin formato de búfer de color (modo de índice de color)                                    |
| Grupo de atributos: | búfer de color                                                                   |
| Valor inicial:   | 0                                                                              |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>\_ \_ valor sin formato de profundidad de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor sin formato de búfer de profundidad                                                         |
| Grupo de atributos: | búfer de profundidad                                                                     |
| Valor inicial:   | 1                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>\_ \_ valor sin formato de estarcido GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Estarcido: valor sin formato del búfer                                                       |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | 0                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>\_valor no \_ cifrado de GL acumulado \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Acumulación: valor sin formato del búfer                                                |
| Grupo de atributos: | búfer acumulado                                                                   |
| Valor inicial:   | 0                                                                              |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




