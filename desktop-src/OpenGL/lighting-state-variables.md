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
ms.openlocfilehash: aa7144e284b5be5abd5a6dc4e08fe2228b621465
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904101"
---
# <a name="lighting-state-variables"></a>Variables de estado de iluminación

<dl> <dt><span id="GL_LIGHTING"></span><span id="gl_lighting"></span>iluminación de GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | True si está habilitada la iluminación        |
| Grupo de atributos: | iluminación/habilitar                    |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL"></span><span id="gl_color_material"></span>\_material de color GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | True si está habilitado el seguimiento de color  |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_PARAMETER"></span><span id="gl_color_material_parameter"></span>\_parámetro de \_ material de color GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Propiedades del material seguimiento del color actual                                       |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | \_ambiente de contabilidad general \_ y \_ difuso                                                        |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_COLOR_MATERIAL_FACE"></span><span id="gl_color_material_face"></span>\_superficie del \_ material de color de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Caras afectadas por el seguimiento de color                                                 |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | \_anverso \_ y \_ atrás de GL                                                             |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiente de contabilidad general \_</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Color de material ambiente                   |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0,2, 0,2, 0,2, 1,0)                        |
| Obtener comando:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>difusión en contab. \_</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Color de material difuso                   |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0,8, 0,8, 0,8, 1,0)                        |
| Obtener comando:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_especular GL</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Color de material especular                  |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0,0, 0,0, 0,0, 1,0)                        |
| Obtener comando:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_EMISSION"></span><span id="gl_emission"></span>emisión de contabilidad \_</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Color del material de emisor                  |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | (0,0, 0,0, 0,0, 1,0)                        |
| Obtener comando:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_SHININESS"></span><span id="gl_shininess"></span>brillo de GL \_</dt> <dd> 

|                  |                                          |
|------------------|------------------------------------------|
| Descripción:     | Exponente especular de material            |
| Grupo de atributos: | iluminación                                 |
| Valor inicial:   | 0,0                                      |
| Obtener comando:     | [**glGetMaterialfv**](glgetmaterial.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_AMBIENT"></span><span id="gl_light_model_ambient"></span>\_ambiente de \_ modelo de luz de contabilidad \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Color de la escena ambiente                                                            |
| Grupo de atributos: | iluminación                                                                       |
| Valor inicial:   | (0,2, 0,2, 0,2, 1,0)                                                              |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_LOCAL_VIEWER"></span><span id="gl_light_model_local_viewer"></span>\_ \_ \_ visor local del modelo \_ de contabilidad solar</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | El visor es local                                                                  |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | CONTABILIDAD \_ falsa                                                                        |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_LIGHT_MODEL_TWO_SIDE"></span><span id="gl_light_model_two_side"></span>modelo de la luz de contabilidad \_ \_ \_ dos \_ lados</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Usar luz de dos caras                                                           |
| Grupo de atributos: | iluminación                                                                         |
| Valor inicial:   | CONTABILIDAD \_ falsa                                                                        |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AMBIENT"></span><span id="gl_ambient"></span>ambiente de contabilidad general \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Intensidad ambiental de la *luz*     |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | (0,0, 0,0, 0,0, 1,0)                  |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span>difusión en contab. \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Intensidad de *la luz difusa*     |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   |                                    |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPECULAR"></span><span id="gl_specular"></span>\_especular GL</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Intensidad especular de *i*    |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   |                                    |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_POSITION"></span><span id="gl_position"></span>posición de contabilidad \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Posición de la luz *i*              |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | (0,0, 0,0, 1,0, 0,0)                  |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_CONSTANT_ATTENUATION"></span><span id="gl_constant_attenuation"></span>\_atenuación de constantes de GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Factor de atenuación constante        |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 1,0                                |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LINEAR_ATTENUATION"></span><span id="gl_linear_attenuation"></span>\_atenuación lineal de GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Factor de atenuación lineal          |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 0,0                                |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_QUADRATIC_ATTENUATION"></span><span id="gl_quadratic_attenuation"></span>\_atenuación cuadrática de GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Factor de atenuación cuadrático       |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 0,0                                |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_DIRECTION"></span><span id="gl_spot_direction"></span>Dirección de la zona de contabilidad \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Dirección de Spotlight de *la luz*   |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | (0,0, 0.0,-1,0)                     |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_EXPONENT"></span><span id="gl_spot_exponent"></span>exponente de la zona de contabilidad \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Exponente destacado de la luz *i*    |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 0,0                                |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_SPOT_CUTOFF"></span><span id="gl_spot_cutoff"></span>límite de la zona de contabilidad \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Ángulo destacado de la *luz*       |
| Grupo de atributos: | iluminación                           |
| Valor inicial:   | 180,0                              |
| Obtener comando:     | [**glGetLightfv**](glgetlight.md) |



 

</dd> <dt><span id="GL_LIGHT_i"></span><span id="gl_light_i"></span><span id="GL_LIGHT_I"></span>GL \_ claro *i*</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | True *si está* habilitada la luz          |
| Grupo de atributos: | iluminación/habilitar                    |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span>\_índices de color de GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | *C (a)*, *c (d)* y *c (s)* para la iluminación de índice de color                         |
| Grupo de atributos: | iluminación/habilitar                                                                |
| Valor inicial:   | 0, 1, 1                                                                          |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




