---
title: Variables de estado de iluminación
description: Variables de estado de iluminación
ms.assetid: a9fb1e22-5e33-4b46-9c3b-2f64de5dd646
keywords:
- Variables de estado de iluminación OpenGL
topic_type:
- apiref
api_name:
- Lighting State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c5a2d029727f4ff4a9eee353230e0843a39f082
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909862"
---
# <a name="lighting-state-variables"></a>Variables de estado de iluminación

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>GL \_ LIGHTING</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | True si la iluminación está habilitada        |
| Grupo de atributos: | iluminación/habilitación                    |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>MATERIAL \_ DE COLOR \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | True si el seguimiento de colores está habilitado  |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>PARÁMETRO \_ DE MATERIAL DE COLOR \_ \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Propiedades de material que rastrean el color actual                                       |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | AMBIENTE \_ Y \_ DIFUSO DE GL \_                                                        |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>GL \_ COLOR \_ MATERIAL \_ FACE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Caras afectadas por el seguimiento de colores                                                 |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | GL \_ FRONT \_ Y \_ BACK                                                             |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ AMBIENT</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Color del material ambiente                   |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0.2,0.2,0.2,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFUSO</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Color de material difuso                   |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0.8,0.8,0.8,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ SPECULAR</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Color del material especular                  |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0.0,0.0,0.0,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>GL \_ EMISSION</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Color de material emisivo                  |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0.0,0.0,0.0,1.0)                        |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>GL \_ GLINESS</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------------|
| Descripción:     | Exponente especular de material            |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | 0,0                                      |
| Comando Get:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>GL \_ LIGHT \_ MODEL \_ AMBIENT</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Color de la escena ambiente                                                            |
| Grupo de atributos: | iluminación                                                                       |
| Valor inicial:   | (0.2,0.2,0.2,1.0)                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>VISOR \_ LOCAL DE GL LIGHT \_ MODEL \_ \_</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | El visor es local                                                                  |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | GL \_ FALSE                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>GL \_ LIGHT \_ MODEL \_ TWO \_ SIDE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Uso de iluminación de dos lados                                                           |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | GL \_ FALSE                                                                        |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>GL \_ AMBIENT</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Intensidad ambiental de la *luz i*     |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | (0.0,0.0,0.0,1.0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>GL \_ DIFUSO</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Intensidad difusa de *la luz i*     |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>GL \_ SPECULAR</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Intensidad especular de la *luz i*    |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   |                                    |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>POSICIÓN \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Posición de la *luz i*              |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | (0.0,0.0,1.0,0.0)                  |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>ATENUACIÓN \_ \_ CONSTANTE DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Factor de atenuación constante        |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 1.0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>ATENUACIÓN \_ LINEAL \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Factor de atenuación lineal          |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>ATENUACIÓN \_ CUADRÁTICA DE GL \_</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Factor de atenuación cuadrática       |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>DIRECCIÓN DE \_ SPOT \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Dirección del foco de luz *i*   |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | (0.0,0.0,-1.0)                     |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>EXPONENTE \_ DE SPOT \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Exponente destacado de light *i*    |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 0,0                                |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>GL \_ SPOT \_ CUTOFF</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Ángulo de foco de *luz i*       |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 180.0                              |
| Comando Get:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ LIGHT *i*</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | True si la luz *i está* habilitada          |
| Grupo de atributos: | iluminación/habilitación                    |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>ÍNDICES \_ DE COLOR \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | *C (a)*, *C (d) y* *C (s) para* la iluminación de índice de color                         |
| Grupo de atributos: | iluminación/habilitación                                                                |
| Valor inicial:   | 0,1,1                                                                          |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




