---
title: Variables de estado del evaluador
description: Variables de estado del evaluador
ms.assetid: e7d710be-de17-46a0-8ad8-0f65b943ece8
keywords:
- Variables de estado del evaluador OpenGL
topic_type:
- apiref
api_name:
- Evaluator State Variables
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 615e7cde4a8f82c3f4a9a95791912c5dc3f77ff3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103994718"
---
# <a name="evaluator-state-variables"></a>Variables de estado del evaluador

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>orden de contabilidad \_</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descripción:     | orden de mapa 1-D                  |
| Grupo de atributos: |                                |
| Valor inicial:   | 1                              |
| Obtener comando:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>orden de contabilidad \_</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descripción:     | pedidos de asignación 2D                 |
| Grupo de atributos: |                                |
| Valor inicial:   | 1,1                            |
| Obtener comando:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descripción:     | puntos de control 1D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Obtener comando:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descripción:     | puntos de control 2D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Obtener comando:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>dominio de contabilidad general \_</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descripción:     | extremos de dominio 1-D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Obtener comando:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>dominio de contabilidad general \_</dt> <dd> 

|                  |                                |
|------------------|--------------------------------|
| Descripción:     | extremos de dominio 2D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Obtener comando:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | la asignación 1-D habilita: *x* es el tipo de asignación   |
| Grupo de atributos: | eval/habilitar                        |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ MAP2 ( \_ x</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | la asignación 2D habilita: *x* es el tipo de asignación   |
| Grupo de atributos: | eval/habilitar                        |
| Valor inicial:   | CONTABILIDAD \_ falsa                          |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>Dominio de la cuadrícula de GL \_ MAP1 \_ \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | extremos de cuadrícula 1D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0, 1                                                                            |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>Dominio de la cuadrícula de GL \_ MAP2 ( \_ \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | extremos de cuadrícula 2D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0, 1; 0, 1                                                                     |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>Segmentos de cuadrícula de GL \_ MAP1 \_ \_</dt> <dd> 

|                  |                                    |
|------------------|------------------------------------|
| Descripción:     | divisiones de cuadrícula 1D                 |
| Grupo de atributos: | eval                               |
| Valor inicial:   | 1                                  |
| Obtener comando:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>Segmentos de cuadrícula de GL \_ MAP1 \_ \_</dt> <dd> 

|                  |                                                                                |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | segmentos de cuadrícula 2D                                                              |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 1,1                                                                           |
| Obtener comando:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>libro de contabilidad \_ automática \_ normal</dt> <dd> 

|                  |                                             |
|------------------|---------------------------------------------|
| Descripción:     | True si la generación automática normal está habilitada |
| Grupo de atributos: | eval                                        |
| Valor inicial:   | CONTABILIDAD \_ falsa                                   |
| Obtener comando:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




