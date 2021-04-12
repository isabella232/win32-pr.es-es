---
title: Variables de estado para los valores actuales y los datos asociados
description: Variables de estado para los valores actuales y los datos asociados
ms.assetid: 8e47b119-a065-43c5-b7f5-76deaf975ad8
keywords:
- Variables de estado para los valores actuales y datos asociados de OpenGL
topic_type:
- apiref
api_name:
- State Variables for Current Values and Associated Data
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aeab660299aa278017e12556a941353d624147d7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419444"
---
# <a name="state-variables-for-current-values-and-associated-data"></a>Variables de estado para los valores actuales y los datos asociados

<dl> <dt><span id="GL_CURRENT_COLOR"></span><span id="gl_current_color"></span>\_color actual de GL \_</dt> <dd> 

|                  |                                                                                                                      |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Color actual                                                                                                        |
| Grupo de atributos: | actuales                                                                                                              |
| Valor inicial:   | 1, 1, 1, 1                                                                                                           |
| Obtener comando:     | [**glGetIntegerv**](glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_INDEX"></span><span id="gl_current_index"></span>\_índice actual de contabilidad \_</dt> <dd> 

|                  |                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Índice de color actual                                                                                                                                            |
| Grupo de atributos: | actuales                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_TEXTURE_COORDS"></span><span id="gl_current_texture_coords"></span>\_coordenadas de \_ textura \_ actual de GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Coordenadas de textura actuales                                                    |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_NORMAL"></span><span id="gl_current_normal"></span>libro de contabilidad \_ \_ normal actual</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Normal actual                                                                 |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 1                                                                        |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION"></span><span id="gl_current_raster_position"></span>\_posición de \_ rasterización actual de GL</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Posición de la trama actual                                                        |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_DISTANCE"></span><span id="gl_current_raster_distance"></span>\_distancia de \_ rasterizado actual de GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Distancia de la trama actual                                                        |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0                                                                              |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_COLOR"></span><span id="gl_current_raster_color"></span>\_color de \_ rasterizado actual de GL \_</dt> <dd> 

|                  |                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Color asociado a la posición de la trama                                                                                                                          |
| Grupo de atributos: | actuales                                                                                                                                                        |
| Valor inicial:   | 1, 1, 1, 1                                                                                                                                                     |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_INDEX"></span><span id="gl_current_raster_index"></span>\_Índice de \_ rasterizado actual de GL \_</dt> <dd> 

|                  |                                                                                                                                                                |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Descripción:     | Índice de color asociado a la posición de la trama                                                                                                                    |
| Grupo de atributos: | actuales                                                                                                                                                        |
| Valor inicial:   | 1                                                                                                                                                              |
| Obtener comando:     | [**glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)[**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_TEXTURE_COORDS"></span><span id="gl_current_raster_texture_coords"></span>\_coordenadas de \_ textura de rasterizado actual de \_ GL \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Coordenadas de textura asociadas a la posición de la trama                            |
| Grupo de atributos: | actuales                                                                        |
| Valor inicial:   | 0, 0, 0, 1                                                                     |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_CURRENT_RASTER_POSITION_VALID"></span><span id="gl_current_raster_position_valid"></span>\_posición de \_ rasterizado actual de GL \_ \_ válida</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Bit válido de posición de la trama                                                        |
| Grupo de atributos: | actuales                                                                          |
| Valor inicial:   | GL \_ true                                                                         |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_EDGE_FLAG"></span><span id="gl_edge_flag"></span>\_marca de borde de contabilidad \_</dt> <dd> 

|                  |                                                                                  |
|------------------|----------------------------------------------------------------------------------|
| Descripción:     | Marca perimetral                                                                        |
| Grupo de atributos: | actuales                                                                          |
| Valor inicial:   | GL \_ true                                                                         |
| Obtener comando:     | [**glGetBooleanv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> </dl>

 

 




