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
ms.openlocfilehash: 747ed7c19817757570d6517c68a987c2c75aa340c74ecfbac9fe258b1091f00e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082515"
---
# <a name="evaluator-state-variables"></a>Variables de estado del evaluador

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ ORDER</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------|
| Descripción:     | Orden del mapa 1D                  |
| Grupo de atributos: |                                |
| Valor inicial:   | 1                              |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>GL \_ ORDER</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------|
| Descripción:     | Pedidos de mapa 2D                 |
| Grupo de atributos: |                                |
| Valor inicial:   | 1,1                            |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de control 1D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de control 2D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMINIO \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de conexión de dominio 1D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMINIO \_ GL</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de conexión de dominio 2D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Habilita el mapa 1D: *x* es el tipo de mapa   |
| Grupo de atributos: | eval/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ MAP2 \_ x</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Habilita el mapa 2D: *x* es el tipo de mapa   |
| Grupo de atributos: | eval/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>DOMINIO DE \_ CUADRÍCULA DE GL MAP1 \_ \_</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Puntos de conexión de cuadrícula 1D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0,1                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>DOMINIO DE \_ CUADRÍCULA DE GL MAP2 \_ \_</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Puntos de conexión de cuadrícula 2D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0, 1; 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>SEGMENTOS \_ DE CUADRÍCULA DE GL MAP1 \_ \_</dt> <dd> 

| Propiedad | Value |
|------------------|------------------------------------|
| Descripción:     | Divisiones de cuadrícula 1D                 |
| Grupo de atributos: | eval                               |
| Valor inicial:   | 1                                  |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>SEGMENTOS \_ DE CUADRÍCULA DE GL MAP1 \_ \_</dt> <dd> 

| Propiedad | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Segmentos de cuadrícula 2D                                                              |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ AUTO \_ NORMAL</dt> <dd> 

| Propiedad | Value |
|------------------|---------------------------------------------|
| Descripción:     | True si la generación normal automática está habilitada |
| Grupo de atributos: | eval                                        |
| Valor inicial:   | GL \_ FALSE                                   |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




