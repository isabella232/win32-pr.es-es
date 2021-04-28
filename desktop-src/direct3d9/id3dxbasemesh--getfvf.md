---
description: 'Método ID3DXBaseMesh::GetFVF: obtiene el valor fijo del vértice de la función.'
ms.assetid: ed56ff2d-0366-426c-9f9a-7d1a7c5d1a7c
title: Método ID3DXBaseMesh::GetFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4e37db51238137d67ba6e060ecfafb7d1361727e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115443"
---
# <a name="id3dxbasemeshgetfvf-method"></a>Método ID3DXBaseMesh::GetFVF

Obtiene el valor fijo del vértice de la función.

## <a name="syntax"></a>Sintaxis


```C++
DWORD GetFVF();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Devuelve los códigos de formato de vértice flexible (FVF).

## <a name="remarks"></a>Comentarios

Este método puede devolver 0 si el formato de vértice no se puede asignar directamente a un código FVF. Esto ocurrirá para una malla creada a partir de una declaración de vértice que no tenga el mismo orden y elementos admitidos por los códigos FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
