---
description: Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: Método ID3DXBaseMesh::GetOptions (D3DX9Mesh.h)
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
ms.openlocfilehash: 8b8ed6281e1418246027a05f281ef5c01d8fbe757a8bd88d2bf6f44ca41ed1d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121767"
---
# <a name="id3dxbasemeshgetoptions-method"></a>Método ID3DXBaseMesh::GetOptions

Recupera las opciones de malla habilitadas para esta malla en el momento de la creación.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Devuelve una combinación de una o varias de las marcas siguientes, que indican las opciones habilitadas para esta malla en el momento de la creación.



| Value                   | Descripción                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXMESH \_ 32 BITS         | Use índices de 32 bits.                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | Use la marca de uso D3DUSAGE DONOTCLIP para los búferes de \_ vértices e índices.                                                                                                                             |
| D3DXMESH \_ DYNAMIC       | Equivalente a especificar D3DXMESH \_ VB \_ DYNAMIC y D3DXMESH \_ IB \_ DYNAMIC.                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | Use la marca de uso D3DUSAGE \_ RTPATCHES para búferes de vértices e índices.                                                                                                                             |
| D3DXMESH \_ NPATCHES      | Al especificar esta marca, el vértice y el búfer de índice de la malla se crean con la marca D3DUSAGE \_ NPATCHES. Esto es necesario si el objeto de malla se va a representar mediante la mejora de N-Patch. |
| D3DXMESH \_ ADMINISTRADO       | Equivalente a especificar D3DXMESH \_ VB \_ MANAGED y D3DXMESH \_ IB \_ MANAGED.                                                                                                                   |
| PUNTOS D3DXMESH \_        | Use la marca de uso D3DUSAGE POINTS para búferes de \_ vértices e índices.                                                                                                                                |
| D3DXMESH \_ IB \_ DYNAMIC   | Use la marca de uso DYNAMIC de D3DUSAGE \_ para los búferes de índice.                                                                                                                                          |
| D3DXMESH \_ IB \_ ADMINISTRADO   | Use la clase de memoria administrada D3DPOOL \_ para búferes de índice.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Use la clase de memoria \_ SYSTEMMEM D3DPOOL para búferes de índice.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Use la marca de uso WRITEONLY de D3DUSAGE \_ para búferes de índice.                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | Equivalente a especificar D3DXMESH \_ VB \_ SYSTEMMEM y D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ DYNAMIC   | Use la marca de uso D3DUSAGE \_ DYNAMIC para los búferes de vértices.                                                                                                                                         |
| D3DXMESH \_ VB \_ ADMINISTRADO   | Use la clase de memoria administrada D3DPOOL \_ para búferes de vértices.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Use la clase de memoria \_ SYSTEMMEM D3DPOOL para búferes de vértices.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Use la marca de uso WRITEONLY de D3DUSAGE para \_ búferes de vértices.                                                                                                                                       |
| D3DXMESH \_ WRITEONLY     | Equivalente a especificar D3DXMESH \_ VB \_ WRITEONLY y D3DXMESH \_ IB \_ WRITEONLY.                                                                                                               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
