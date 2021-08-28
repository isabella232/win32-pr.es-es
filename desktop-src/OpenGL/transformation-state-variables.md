---
title: Variables de estado de la transformación
description: Variables de estado de la transformación
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
ms.openlocfilehash: 3c79b4363419d97a64184dd2408a9f6221ada52adc49adbb28eb3d049a4b2a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011923"
---
# <a name="transformation-state-variables"></a>Variables de estado de la transformación

<dl> <dt><span id="GL_MODELVIEW_MATRIX"></span><span id="gl_modelview_matrix"></span>GL \_ MODELVIEW \_ MATRIX</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Pila de matriz modelview             |
| Grupo de atributos: |                                    |
| Valor inicial:   | Identidad                           |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_PROJECTION_MATRIX"></span><span id="gl_projection_matrix"></span>MATRIZ \_ DE \_ PROYECCIÓN DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Pila de matriz de proyección                                                        |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidad                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_MATRIX"></span><span id="gl_texture_matrix"></span>MATRIZ \_ DE TEXTURA \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Pila de matriz de textura                                                           |
| Grupo de atributos: |                                                                                |
| Valor inicial:   | Identidad                                                                       |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_VIEWPORT"></span><span id="gl_viewport"></span>VENTANILLA \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Origen y extensión de la ventanilla                                                       |
| Grupo de atributos: | ventanilla                                                                         |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_RANGE"></span><span id="gl_depth_range"></span>INTERVALO \_ DE PROFUNDIDAD DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Intervalo de profundidad cerca y lejos                                                       |
| Grupo de atributos: | ventanilla                                                                       |
| Valor inicial:   | 0, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MODELVIEW_STACK_DEPTH"></span><span id="gl_modelview_stack_depth"></span>PROFUNDIDAD DE \_ PILA DE GL MODELVIEW \_ \_</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Puntero de pila de la matriz modelview                                                   |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_PROJECTION_STACK_DEPTH"></span><span id="gl_projection_stack_depth"></span>PROFUNDIDAD DE \_ LA PILA \_ DE \_ PROYECCIÓN DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Puntero de pila de matriz de proyección                                                  |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_TEXTURE_STACK_DEPTH"></span><span id="gl_texture_stack_depth"></span>PROFUNDIDAD DE \_ LA PILA DE TEXTURA \_ \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Puntero de pila de la matriz de textura                                                     |
| Grupo de atributos: |                                                                                  |
| Valor inicial:   | 1                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MATRIX_MODE"></span><span id="gl_matrix_mode"></span>MODO DE \_ \_ MATRIZ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Modo de matriz actual                                                              |
| Grupo de atributos: | transform                                                                        |
| Valor inicial:   | GL \_ MODELVIEW                                                                    |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_NORMALIZE"></span><span id="gl_normalize"></span>GL \_ NORMALIZE</dt> <dd> 

| Propiedad | Value |
|------------------|-------------------------------------|
| Descripción:     | Normalización actual de encendido y apagado |
| Grupo de atributos: | transform/enable                    |
| Valor inicial:   | GL \_ FALSE                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)  |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Coeficientes del plano de recorte de usuario         |
| Grupo de atributos: | transform                                |
| Valor inicial:   | 0, 0, 0, 0                               |
| Comando Get:     | [**glGetClipPlane**](glgetclipplane.md) |



 

</dd> <dt><span id="GL_CLIP_PLANE_i"></span><span id="gl_clip_plane_i"></span><span id="GL_CLIP_PLANE_I"></span>GL \_ CLIP \_ PLANE *i*</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | *Plano de* recorte de usuario habilitado |
| Grupo de atributos: | transform/enable                   |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> </dl>

 

 




