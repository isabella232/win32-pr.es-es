---
title: Operaciones de píxeles
description: Operaciones de píxeles
ms.assetid: e60cc45b-867c-441a-b579-8c7dbd46ecd9
keywords:
- Operaciones de píxeles OpenGL
topic_type:
- apiref
api_name:
- Pixel Operations
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda15342b246ba979bdbe60184eeb632368f36b4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904039"
---
# <a name="pixel-operations"></a>Operaciones de píxeles

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>\_prueba de tijeras GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Tijera habilitada                 |
| Grupo de atributos: | tijeras/habilitación                     |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>\_cuadro de tijeras de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Cuadro de tijeras                                                                      |
| Grupo de atributos: | tijera                                                                          |
| Valor inicial:   |                                                                                  |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>\_prueba de galería de símbolos GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Estarcido habilitado                 |
| Grupo de atributos: | Galería de símbolos: búfer/habilitar              |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>la \_ Galería de símbolos GL \_ FUNC</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de estarcido                                                                 |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | GL \_ siempre                                                                       |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>\_máscara de \_ valor de estarcido GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Máscara de galería de símbolos                                                                     |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | 1                                                                              |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>\_referencia de galería de símbolos GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor de referencia de estarcido                                                          |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | 0                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>error en la \_ Galería de símbolos GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Acción de error de estarcido                                                              |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | mantenimiento de contabilidad \_                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>error de profundidad de la \_ fase de estarcido GL \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Acción de error de búfer de profundidad de estarcido                                                 |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | mantenimiento de contabilidad \_                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>\_paso de \_ \_ profundidad \_ de la galería de símbolos GL</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Acción de paso de búfer de profundidad de estarcido                                                 |
| Grupo de atributos: | cliché-búfer                                                                   |
| Valor inicial:   | mantenimiento de contabilidad \_                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>prueba de GL \_ alpha \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Prueba alfa habilitada                 |
| Grupo de atributos: | búfer de color/habilitar                |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>FUNC. de prueba de GL \_ \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de prueba alfa                                                              |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ siempre                                                                       |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>referencia de prueba de GL \_ alfa \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor de referencia de la prueba alfa                                                       |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | 0                                                                                |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>\_prueba de profundidad de GL \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Búfer de profundidad habilitado               |
| Grupo de atributos: | profundidad de búfer/habilitación                |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>\_FUNC profundidad de GL \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de prueba de búfer de profundidad                                                       |
| Grupo de atributos: | búfer de profundidad                                                                     |
| Valor inicial:   | CONTABILIDAD \_ inferior                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>fusión de contabilidad \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Combinación habilitada                   |
| Grupo de atributos: | búfer de color/habilitar                |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>\_src BLENC \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Blending (función de origen)                                                         |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ uno                                                                          |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>DST de contab. \_ \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de destino de fusión                                                    |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ cero                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>interpolación en contab. \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Interpolación habilitada                  |
| Grupo de atributos: | búfer de color/habilitar                |
| Valor inicial:   | GL \_ true                           |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>\_OP lógica de contabilidad \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | Operación lógica habilitada          |
| Grupo de atributos: | búfer de color/habilitar                |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>\_modo de \_ OP \_ lógica de contabilidad</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de operación lógica                                                       |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | copia en GL \_                                                                         |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




