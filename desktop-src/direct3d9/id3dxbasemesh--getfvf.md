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
ms.openlocfilehash: 814f14645e5e7f0aa883f04e689f0774441482b86223bf485fa1fc8a395618c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987625"
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

Este método puede devolver 0 si el formato de vértice no se puede asignar directamente a un código FVF. Esto ocurrirá para una malla creada a partir de una declaración de vértice que no tenga el mismo orden y los elementos admitidos por los códigos FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
