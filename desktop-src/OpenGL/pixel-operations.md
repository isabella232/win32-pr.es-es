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
ms.openlocfilehash: 45d36fc22ace4ee18303ce0eb16c5a10f901510f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171342"
---
# <a name="pixel-operations"></a>Operaciones de píxeles

<dl> <dt><span id="GL_SCISSOR_TEST"></span><span id="gl_scissor_test"></span>PRUEBA \_ DE RESERCIÓN \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Habilitación de la asociación                 |
| Grupo de atributos: | y habilitar                     |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_SCISSOR_BOX"></span><span id="gl_scissor_box"></span>CASILLA \_ DE RESALTE \_ DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Cuadro de verificación                                                                      |
| Grupo de atributos: | Tijera                                                                          |
| Valor inicial:   |                                                                                  |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_TEST"></span><span id="gl_stencil_test"></span>GL \_ STENCIL \_ TEST</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Galería de símbolos habilitada                 |
| Grupo de atributos: | stencil-buffer/enable              |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_STENCIL_FUNC"></span><span id="gl_stencil_func"></span>FUNC \_ de GL STENCIL \_</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de galería de símbolos                                                                 |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | GL \_ ALWAYS                                                                       |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_VALUE_MASK"></span><span id="gl_stencil_value_mask"></span>GL \_ STENCIL \_ VALUE \_ MASK</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Máscara de galería de símbolos                                                                     |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | 1                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_REF"></span><span id="gl_stencil_ref"></span>GL \_ STENCIL \_ REF</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor de referencia de galería de símbolos                                                          |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_FAIL"></span><span id="gl_stencil_fail"></span>ERROR \_ DE GALERÍA DE SÍMBOLOS DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Acción de error de galería de símbolos                                                              |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | GL \_ KEEP                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_FAIL"></span><span id="gl_stencil_pass_depth_fail"></span>ERROR DE PROFUNDIDAD DE PASO DE GALERÍA \_ \_ DE SÍMBOLOS DE \_ \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Acción de error de búfer de profundidad de galería de símbolos                                                 |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | GL \_ KEEP                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_STENCIL_PASS_DEPTH_PASS"></span><span id="gl_stencil_pass_depth_pass"></span>PASO DE PROFUNDIDAD DE PASO DE GALERÍA \_ \_ DE SÍMBOLOS DE \_ \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Acción de paso de búfer de profundidad de galería de símbolos                                                 |
| Grupo de atributos: | stencil-buffer                                                                   |
| Valor inicial:   | GL \_ KEEP                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST"></span><span id="gl_alpha_test"></span>GL \_ ALPHA \_ TEST</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Prueba alfa habilitada                 |
| Grupo de atributos: | color-buffer/enable                |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_FUNC"></span><span id="gl_alpha_test_func"></span>GL \_ ALPHA \_ TEST \_ FUNC</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de prueba alfa                                                              |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ ALWAYS                                                                       |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_ALPHA_TEST_REF"></span><span id="gl_alpha_test_ref"></span>GL \_ ALPHA \_ TEST \_ REF</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Valor de referencia de prueba alfa                                                       |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | 0                                                                                |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DEPTH_TEST"></span><span id="gl_depth_test"></span>PRUEBA \_ DE PROFUNDIDAD DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Búfer de profundidad habilitado               |
| Grupo de atributos: | depth-buffer/enable                |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_DEPTH_FUNC"></span><span id="gl_depth_func"></span>GL \_ DEPTH \_ FUNC</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de prueba de búfer de profundidad                                                       |
| Grupo de atributos: | depth-buffer                                                                     |
| Valor inicial:   | GL \_ LESS                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND"></span><span id="gl_blend"></span>GL \_ BLEND</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Blending enabled                   |
| Grupo de atributos: | color-buffer/enable                |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_BLENC_SRC"></span><span id="gl_blenc_src"></span>GL \_ BLENC \_ SRC</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de origen de combinación                                                         |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ ONE                                                                          |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_BLEND_DST"></span><span id="gl_blend_dst"></span>GL \_ BLEND \_ DST</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de destino de mezcla                                                    |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ ZERO                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_DITHER"></span><span id="gl_dither"></span>GL \_ DITHER</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Dithering enabled                  |
| Grupo de atributos: | color-buffer/enable                |
| Valor inicial:   | GL \_ TRUE                           |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP"></span><span id="gl_logic_op"></span>GL \_ LOGIC \_ OP</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Operación lógica habilitada          |
| Grupo de atributos: | color-buffer/enable                |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_LOGIC_OP_MODE"></span><span id="gl_logic_op_mode"></span>GL \_ LOGIC \_ OP \_ MODE</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Función de operación lógica                                                       |
| Grupo de atributos: | búfer de color                                                                     |
| Valor inicial:   | GL \_ COPY                                                                         |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




