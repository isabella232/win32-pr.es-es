---
title: Variables de estado del control del buffer de fotogramas
description: Variables de estado del control del buffer de fotogramas
ms.assetid: ab57e07d-a694-45e7-a3b3-2e856111b87d
keywords:
- Variables de estado de control framebuffer OpenGL
topic_type:
- apiref
api_name:
- Framebuffer Control State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 276019f790e5f4750e446cf4ae2d035e0178d0e79130100a5a5e1954cbdcb73a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061917"
---
# <a name="framebuffer-control-state-variables"></a>Variables de estado del control del buffer de fotogramas

<dl> <dt><span id="GL_DRAW_BUFFER"></span><span id="gl_draw_buffer"></span>BÚFER \_ DE DIBUJO DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------|
| Descripción:     | Búferes seleccionados para dibujar           |
| Grupo de atributos: | búfer de color                           |
| Valor inicial:   |                                        |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_WRITEMASK"></span><span id="gl_index_writemask"></span>GL \_ INDEX \_ WRITEMASK</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Máscara de escritura de índice de color                                                            |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_WRITEMASK"></span><span id="gl_color_writemask"></span>GL \_ COLOR \_ WRITEMASK</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Habilita la escritura en color; R, G, B o A                                               |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_WRITEMASK"></span><span id="gl_depth_writemask"></span>GL \_ DEPTH \_ WRITEMASK</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Búfer de profundidad habilitado para escritura                                                 |
| Grupo de atributos: | depth-buffer                                                                     |
| Valor inicial:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_WRITEMASK"></span><span id="gl_stencil_writemask"></span>GL \_ STENCIL \_ WRITEMASK</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Máscara de escritura de búfer de galería de símbolos                                                         |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_CLEAR_VALUE"></span><span id="gl_color_clear_value"></span>GL \_ COLOR \_ CLEAR \_ VALUE</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Valor de borrar búfer de color (modo RGBA)                                           |
| Grupo de atributos: | búfer de color                                                                   |
| Valor inicial:   | 0, 0, 0, 0                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_INDEX_CLEAR_VALUE"></span><span id="gl_index_clear_value"></span>GL \_ INDEX \_ CLEAR \_ VALUE</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Valor sin borrar del búfer de color (modo de índice de color)                                    |
| Grupo de atributos: | búfer de color                                                                   |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_CLEAR_VALUE"></span><span id="gl_depth_clear_value"></span>GL \_ DEPTH \_ CLEAR \_ VALUE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor sin borrar del búfer de profundidad                                                         |
| Grupo de atributos: | depth-buffer                                                                     |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_CLEAR_VALUE"></span><span id="gl_stencil_clear_value"></span>GL \_ STENCIL \_ CLEAR \_ VALUE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor sin borrar del búfer de galería de símbolos                                                       |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ACCUM_CLEAR_VALUE"></span><span id="gl_accum_clear_value"></span>GL \_ ACCUM \_ CLEAR \_ VALUE</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Valor clear del búfer de acumulación                                                |
| Grupo de atributos: | accum-buffer                                                                   |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




