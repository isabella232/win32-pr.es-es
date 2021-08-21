---
title: Variables de estado de la opción de texturas
description: Variables de estado de la opción de texturas
ms.assetid: 2d9d3d8b-ecaa-412c-8105-ae2ca801784e
keywords:
- Texturing State Variables OpenGL
topic_type:
- apiref
api_name:
- Texturing State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7393fc6e700b028ba3783e5c78d8175e0c3fba4937bf3830d5cae8897aa0d4db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776585"
---
# <a name="texturing-state-variables"></a>Variables de estado de la opción de texturas

<dl> <dt><span id="GL_TEXTURE_x"></span><span id="gl_texture_x"></span><span id="GL_TEXTURE_X"></span>GL \_ TEXTURE \_ *x*</dt> <dd> 

| Propiedad | Valor |
|------------------|-------------------------------------------------------|
| Descripción:     | True si *x* - D texturing enabled *(x* es 1D o 2D) |
| Grupo de atributos: | texture/enable                                        |
| Valor inicial:   | GL \_ FALSE                                             |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)                    |



 

</dd> <dt><span id="GL_TEXTURE"></span><span id="gl_texture"></span>TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------|
| Descripción:     | *imagen de* textura x - D en el nivel de *detalle i* |
| Grupo de atributos: |                                              |
| Valor inicial:   |                                              |
| Comando Get:     | [**glGetTexImage**](glgetteximage.md)       |



 

</dd> <dt><span id="GL_TEXTURE_WIDTH"></span><span id="gl_texture_width"></span>ANCHO DE \_ TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------|
| Descripción:     | *x* - D texture image *i* 's width                       |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_HEIGHT"></span><span id="gl_texture_height"></span>ALTO \_ DE TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------|
| Descripción:     | *x* - D texture image *i* 's height                      |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER"></span><span id="gl_texture_border"></span>BORDE DE \_ TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------|
| Descripción:     | *x* - D texture image *i* 's border                      |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 0                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_COMPONENTS"></span><span id="gl_texture_components"></span>COMPONENTES DE \_ TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------|
| Descripción:     | Componentes de imagen de textura                                 |
| Grupo de atributos: |                                                          |
| Valor inicial:   | 1                                                        |
| Comando Get:     | [**glGetTexLevelParameter**](glgettexlevelparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_BORDER_COLOR"></span><span id="gl_texture_border_color"></span>COLOR DEL \_ BORDE \_ DE TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------------|
| Descripción:     | Color del borde de textura                           |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | 0, 0, 0, 0                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MIN_FILTER"></span><span id="gl_texture_min_filter"></span>FILTRO MÍNIMO \_ \_ DE TEXTURA DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------------|
| Descripción:     | Función de minificación de textura                  |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ NEAREST \_ MIPMAP \_ LINEAR                    |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_MAG_FILTER"></span><span id="gl_texture_mag_filter"></span>FILTRO GL \_ TEXTURE \_ MAG \_</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------------|
| Descripción:     | Función de ampliación de textura                 |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ LINEAR                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_WRAP__x"></span><span id="gl_texture_wrap__x"></span><span id="GL_TEXTURE_WRAP__X"></span>GL \_ TEXTURE \_ WRAP \_ *x*</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------------|
| Descripción:     | Modo de ajuste de textura *(x* es S o T)              |
| Grupo de atributos: | textura                                        |
| Valor inicial:   | GL \_ REPEAT                                     |
| Comando Get:     | [**glGetTexParameter**](glgettexparameter.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_MODE"></span><span id="gl_texture_env_mode"></span>MODO DE \_ ENV DE \_ TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------|
| Descripción:     | Función de aplicación de textura         |
| Grupo de atributos: | textura                              |
| Valor inicial:   | \_GLMODULTE                         |
| Comando Get:     | [**glGetTexEnviv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_ENV_COLOR"></span><span id="gl_texture_env_color"></span>COLOR DE \_ \_ ENV DE TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------|
| Descripción:     | Color del entorno de textura            |
| Grupo de atributos: | textura                              |
| Valor inicial:   | 0, 0, 0, 0                           |
| Comando Get:     | [**glGetTexEnvfv**](glgettexenv.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN__x"></span><span id="gl_texture_gen__x"></span><span id="GL_TEXTURE_GEN__X"></span>GL \_ TEXTURE \_ GEN \_ *x*</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Texgen está habilitado *(x* es S, T, R o Q) |
| Grupo de atributos: | texture/enable                           |
| Valor inicial:   | GL \_ FALSE                                |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)       |



 

</dd> <dt><span id="GL_EYE_PLANE"></span><span id="gl_eye_plane"></span>GL \_ EYE \_ PLANE</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------|
| Descripción:     | Coeficientes de ecuación del plano de Texasgen   |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_OBJECT_PLANE"></span><span id="gl_object_plane"></span>PLANO \_ DE OBJETOS \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------|
| Descripción:     | Coeficientes lineales de objetos de Texgen    |
| Grupo de atributos: | textura                              |
| Valor inicial:   |                                      |
| Comando Get:     | [**glGetTexGenfv**](glgettexgen.md) |



 

</dd> <dt><span id="GL_TEXTURE_GEN_MODE"></span><span id="gl_texture_gen_mode"></span>MODO GEN \_ DE \_ TEXTURA \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------|
| Descripción:     | Función que se usa para el contrabando             |
| Grupo de atributos: | textura                              |
| Valor inicial:   | GL \_ EYE \_ LINEAR                      |
| Comando Get:     | [**glGetTexGeniv**](glgettexgen.md) |



 

</dd> </dl>

 

 




