---
description: Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh:: GetOptions (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718383"
---
# <a name="id3dxbasemeshgetoptions-method"></a>ID3DXBaseMesh:: GetOptions (método)

Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Devuelve una combinación de una o varias de las marcas siguientes, que indican las opciones habilitadas para esta malla en el momento de su creación.



| Value                   | Descripción                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32 bits         | Usar índices de 32 bits.                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | Use la \_ marca de uso de D3DUSAGE DONOTCLIP para los búferes de vértices y de índices.                                                                                                                             |
| D3DXMESH \_ dinámico       | Equivale a especificar D3DXMESH \_ VB \_ Dynamic y D3DXMESH \_ IB \_ Dynamic.                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | Use la \_ marca de uso de D3DUSAGE RTPATCHES para los búferes de vértices y de índices.                                                                                                                             |
| D3DXMESH \_ NPATCHES      | Si se especifica esta marca, el vértice y el búfer de índice de la malla se crearán con la \_ marca D3DUSAGE NPATCHES. Esto es necesario si el objeto de malla se va a representar mediante la mejora de N-patch. |
| Administrado por D3DXMESH \_       | Equivale a especificar D3DXMESH \_ VB \_ administrado y D3DXMESH \_ IB \_ administrado.                                                                                                                   |
| \_Puntos D3DXMESH        | Use la \_ marca de uso de puntos D3DUSAGE para los búferes de vértices y de índices.                                                                                                                                |
| D3DXMESH \_ IB \_ Dynamic   | Use la \_ marca de uso dinámico D3DUSAGE para los búferes de índice.                                                                                                                                          |
| Administrado por D3DXMESH \_ IB \_   | Use la \_ clase de memoria administrada D3DPOOL para los búferes de índice.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Use la \_ clase de memoria D3DPOOL SYSTEMMEM para los búferes de índice.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Use la \_ marca de uso WRITEONLY de D3DUSAGE para los búferes de índice.                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | Equivale a especificar D3DXMESH \_ VB \_ SYSTEMMEM y D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ dinámico   | Use la \_ marca de uso dinámico D3DUSAGE para los búferes de vértices.                                                                                                                                         |
| D3DXMESH \_ VB \_ administrado   | Use la \_ clase de memoria administrada D3DPOOL para los búferes de vértices.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Use la \_ clase de memoria D3DPOOL SYSTEMMEM para los búferes de vértices.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Use la \_ marca de uso WRITEONLY de D3DUSAGE para los búferes de vértices.                                                                                                                                       |
| D3DXMESH \_ WRITEONLY     | Equivalente a especificar tanto D3DXMESH \_ VB \_ WRITEONLY como D3DXMESH \_ IB \_ WriteOnly.                                                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
