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
ms.openlocfilehash: f2895f773721f7c900003cbaa0f070c277a0e260
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473683"
---
# <a name="evaluator-state-variables"></a>Variables de estado del evaluador

<dl> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>PEDIDO \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------|
| Descripción:     | Orden de mapa 1D                  |
| Grupo de atributos: |                                |
| Valor inicial:   | 1                              |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_ORDER"></span><span id="gl_order"></span>PEDIDO \_ DE GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------|
| Descripción:     | Pedidos de mapas 2D                 |
| Grupo de atributos: |                                |
| Valor inicial:   | 1,1                            |
| Comando Get:     | [**glGetMapiv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de control 1D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_COEFF"></span><span id="gl_coeff"></span>GL \_ COEFF</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de control 2D             |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMINIO \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de conexión de dominio 1D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_DOMAIN"></span><span id="gl_domain"></span>DOMINIO \_ GL</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------|
| Descripción:     | Puntos de conexión de dominio 2D           |
| Grupo de atributos: |                                |
| Valor inicial:   |                                |
| Comando Get:     | [**glGetMapfv**](glgetmap.md) |



 

</dd> <dt><span id="GL_MAP1_x"></span><span id="gl_map1_x"></span><span id="GL_MAP1_X"></span>GL \_ MAP1 \_ x</dt> <dd> 

| Propiedad. | Value |
|------------------|------------------------------------|
| Descripción:     | Asignación 1D habilita: *x* es tipo de mapa   |
| Grupo de atributos: | eval/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP2_x"></span><span id="gl_map2_x"></span><span id="GL_MAP2_X"></span>GL \_ MAP2 \_ x</dt> <dd> 

| Propiedad. | Value |
|------------------|------------------------------------|
| Descripción:     | Asignación 2D habilita: *x* es tipo de mapa   |
| Grupo de atributos: | eval/enable                        |
| Valor inicial:   | GL \_ FALSE                          |
| Comando Get:     | [**glIsEnabled**](glisenabled.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_DOMAIN"></span><span id="gl_map1_grid_domain"></span>DOMINIO DE CUADRÍCULA DE GL \_ MAP1 \_ \_</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Puntos de conexión de cuadrícula 1D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0,1                                                                            |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP2_GRID_DOMAIN"></span><span id="gl_map2_grid_domain"></span>DOMINIO DE \_ CUADRÍCULA DE GL MAP2 \_ \_</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Puntos de conexión de cuadrícula 2D                                                             |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 0, 1; 0, 1                                                                     |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>SEGMENTOS \_ DE CUADRÍCULA DE GL MAP1 \_ \_</dt> <dd> 

| Propiedad. | Value |
|------------------|------------------------------------|
| Descripción:     | Divisiones de cuadrícula 1D                 |
| Grupo de atributos: | eval                               |
| Valor inicial:   | 1                                  |
| Comando Get:     | [**glGetFloatv**](glgetfloatv.md) |



 

</dd> <dt><span id="GL_MAP1_GRID_SEGMENTS"></span><span id="gl_map1_grid_segments"></span>SEGMENTOS \_ DE CUADRÍCULA DE GL MAP1 \_ \_</dt> <dd> 

| Propiedad. | Value |
|------------------|--------------------------------------------------------------------------------|
| Descripción:     | Segmentos de cuadrícula 2D                                                              |
| Grupo de atributos: | eval                                                                           |
| Valor inicial:   | 1, 1                                                                           |
| Comando Get:     | [**glGetFloatv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) |



 

</dd> <dt><span id="GL_AUTO_NORMAL"></span><span id="gl_auto_normal"></span>GL \_ AUTO \_ NORMAL</dt> <dd> 

| Propiedad. | Value |
|------------------|---------------------------------------------|
| Descripción:     | True si la generación normal automática está habilitada |
| Grupo de atributos: | eval                                        |
| Valor inicial:   | GL \_ FALSE                                   |
| Comando Get:     | [**glIsEnabled**](glisenabled.md)          |



 

</dd> </dl>

 

 




