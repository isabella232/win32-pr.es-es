---
title: Variables de estado para los valores actuales y los datos asociados
description: Variables de estado para los valores actuales y los datos asociados
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- Variables de estado para valores actuales y datos asociados OpenGL
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d99a9504a673d23d6923d5faf0e99770f20fe55e1cdd6b63d9adcbe68282584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553715"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>Variables de estado para los valores actuales y los datos asociados

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>COLOR \_ ACTUAL DE \_ GL</dt> <dd> 

| Propiedad | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Color actual                                                                                                        |
| Grupo de atributos: | actuales                                                                                                              |
| Valor inicial:   | 1, 1, 1, 1                                                                                                           |
| Comando Get:     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>GL \_ CURRENT \_ INDEX</dt> <dd> 

| Propiedad | Valor |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Índice de color actual                                                                                                                                            |
| Grupo de atributos: | actuales                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>\_ \_ COORDS DE TEXTURA \_ ACTUALES DE GL</dt> <dd> 

| Propiedad | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Coordenadas de textura actuales                                                    |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>GL \_ CURRENT \_ NORMAL</dt> <dd> 

| Propiedad | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Normal actual                                                                 |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 1                                                                        |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>POSICIÓN \_ DE TRAMA ACTUAL DE \_ GL</dt> <dd> 

| Propiedad | Valor |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Posición de trama actual                                                        |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>GL \_ CURRENT \_ RASTER \_ DISTANCE</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Distancia de trama actual                                                        |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0                                                                              |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>COLOR \_ DE TRAMA ACTUAL DE \_ \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Color asociado a la posición de trama                                                                                                                          |
| Grupo de atributos: | actuales                                                                                                                                                        |
| Valor inicial:   | 1, 1, 1, 1                                                                                                                                                     |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>ÍNDICE \_ DE TRAMA ACTUAL DE \_ \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Índice de color asociado a la posición de trama                                                                                                                    |
| Grupo de atributos: | actuales                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Comando Get:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>\_ \_ \_ COORDS ACTUALES DE TEXTURA DE \_ TRAMA DE GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Coordenadas de textura asociadas a la posición de trama                            |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>POSICIÓN DE TRAMA ACTUAL DE GL \_ \_ \_ \_ VÁLIDA</dt> <dd> 

| Propiedad | Valor |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Bit válido de posición de trama                                                        |
| Grupo de atributos: | actuales                                                                          |
| Valor inicial:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>MARCA \_ DE BORDE DE \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Marca perimetral                                                                        |
| Grupo de atributos: | actuales                                                                          |
| Valor inicial:   | GL \_ TRUE                                                                         |
| Comando Get:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




