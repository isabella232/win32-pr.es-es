---
title: Variables de estado de transformación
description: Variables de estado de transformación
ms.assetid: 3a6be5ac-ac7a-4c3e-8b65-0404849ae67c
keywords:
- Variables de estado de transformación OpenGL
topic_type:
- apiref
api_name:
- Transformation State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3434fe9f9aa528aa8d201b56ed363753c594690f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104358172"
---
# <a name="transformation-state-variables"></a>Variables de estado de transformación

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>\_matriz MODELVIEW de GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Pila de matriz MODELVIEW             |
| Grupo de atributos: |                                    |
| Valor inicial:   | Identidad                           |
| Obtener comando:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>\_matriz de proyección de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Pila de la matriz de proyección                                                        |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidad                                                                       |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>\_matriz de textura de GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Pila de la matriz de textura                                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidad                                                                       |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>ventanilla de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Origen y extensión de la ventanilla                                                       |
| Grupo de atributos: | ventanilla                                                                         |
| Valor inicial:   |                                                                                  |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>\_rango de profundidad de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Rango de profundidad Near y Far                                                       |
| Grupo de atributos: | ventanilla                                                                       |
| Valor inicial:   | 0, 1                                                                           |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>profundidad de la pila de GL \_ MODELVIEW \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | MODELVIEW puntero de pila de matriz                                                   |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>profundidad de la pila de proyección de contabilidad \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Puntero de pila de matriz de proyecciones                                                  |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>profundidad de la pila de textura de GL \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Puntero de pila de matriz de textura                                                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>\_modo de matriz de contabilidad general \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Modo de matriz actual                                                              |
| Grupo de atributos: | transform                                                                        |
| Valor inicial:   | GL \_ MODELVIEW                                                                    |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>normalizar libro de contabilidad \_</dt> <dd> 

|                  |                                     |
|------------------|-------------------------------------|
| Descripción:     | Normalización/desactivación normal actual |
| Grupo de atributos: | transformar/habilitar                    |
| Valor inicial:   | CONTABILIDAD \_ falsa                           |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plano de clip de contabilidad \_ </dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Coeficientes de plano de recorte de usuario         |
| Grupo de atributos: | transform                                |
| Valor inicial:   | 0, 0, 0, 0                               |
| Obtener comando:     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>\_Plano de clip de contabilidad \_ </dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     |  plano de recorte de usuario habilitado |
| Grupo de atributos: | transformar/habilitar                   |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




