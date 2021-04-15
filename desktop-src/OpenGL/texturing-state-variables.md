---
title: Variables de estado de texturización
description: Variables de estado de texturización
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Variables de estado de texturización OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a9894e9f3723cca957fdeeb2882ede8f689ee7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "105665757"
---
# <a name="texturing-state-variables"></a>Variables de estado de texturización

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>\_Textura GL \_ *x*</dt> <dd> 

|                  |                                                       |
|------------------|-------------------------------------------------------|
| Descripción:     | True si está   habilitada la texturización x-d (*x* es 1-d o 2-d) |
| Grupo de atributos: | textura/habilitar                                        |
| Valor inicial:   | CONTABILIDAD \_ falsa                                             |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>\_textura GL</dt> <dd> 

|                  |                                              |
|------------------|----------------------------------------------|
| Descripción:     | *x*   -D imagen de textura en el nivel de detalle *i* |
| Grupo de atributos: |                                              |
| Valor inicial:   |                                              |
| Obtener comando:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>\_ancho de textura de GL \_</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descripción:     | *x*   -D *textura imagen*   de ancho                       |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Obtener comando:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>\_alto de textura de GL \_</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descripción:     | *x*   Alto de la imagen *de* textura-D                        |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Obtener comando:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>\_borde de textura GL \_</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descripción:     | *x*   -D textura imagen *i*                        |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Obtener comando:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>\_componentes de textura de GL \_</dt> <dd> 

|                  |                                                          |
|------------------|----------------------------------------------------------|
| Descripción:     | Componentes de imagen de textura                                 |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 1                                                        |
| Obtener comando:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>\_color de \_ borde de textura GL \_</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descripción:     | Color de borde de textura                           |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | 0, 0, 0, 0                                     |
| Obtener comando:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>\_ \_ filtro mínimo de textura de GL \_</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descripción:     | Texture minificación función)                  |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | el \_ \_ MIP \_ lineal más cercano de contabilidad                    |
| Obtener comando:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>\_filtro de textura de GL \_ \_</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descripción:     | Función de aumento de textura                 |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | CONTABILIDAD \_ lineal                                     |
| Obtener comando:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>Ajuste de textura de GL \_ \_ \_ *x*</dt> <dd> 

|                  |                                                |
|------------------|------------------------------------------------|
| Descripción:     | Modo de ajuste de textura (*x*   es S o T)              |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | repetición de GL \_                                     |
| Obtener comando:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>\_modo de textura del libro de contabilidad \_ \_</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descripción:     | Función de aplicación de textura         |
| Grupo de atributos: | textura                              |
| Valor inicial:   | \_modular GL                         |
| Obtener comando:     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>\_color de textura de libro de contabilidad \_ \_</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descripción:     | Color del entorno de textura            |
| Grupo de atributos: | textura                              |
| Valor inicial:   | 0, 0, 0, 0                           |
| Obtener comando:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ Texture \_ gen \_ *x*</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Texgen está habilitado (*x*   es S, T, R o Q) |
| Grupo de atributos: | textura/habilitar                           |
| Valor inicial:   | CONTABILIDAD \_ falsa                                |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>\_plano de ojo de contabilidad \_</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descripción:     | Coeficientes de ecuación del plano Texgen   |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Obtener comando:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>\_plano del objeto GL \_</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descripción:     | Coeficientes lineales del objeto Texgen    |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Obtener comando:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>\_modo de generación de texturas GL \_ \_</dt> <dd> 

|                  |                                      |
|------------------|--------------------------------------|
| Descripción:     | Función usada para texgen             |
| Grupo de atributos: | textura                              |
| Valor inicial:   | \_ojo \_ lineal de contabilidad                      |
| Obtener comando:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




