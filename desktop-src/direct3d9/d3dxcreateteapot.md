---
description: Usa un sistema de coordenadas a la izquierda para crear una malla que contiene una cafetera.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: Función D3DXCreateTeapot (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d016d69d1b510e504f3cf0b7ec54f69943d1b3db5f16347f8eeaadd75f3f212
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988525"
---
# <a name="d3dxcreateteapot-function"></a>Función D3DXCreateTeapot

Usa un sistema de coordenadas a la izquierda para crear una malla que contiene una cafetera.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de tépot creada.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a la forma de salida, una [**interfaz ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md) Cuando el método vuelve, este parámetro se rellena con una matriz de tres DWORD por cara que especifican los tres vecinos de cada cara de la malla. Se puede especificar **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Esta función crea una malla con la opción de creación D3DXMESH MANAGED y el formato de vértice \_ flexible NORMAL (FVF) [D3DFVF \_ XYZ \| D3DFVF. \_ ](d3dfvf.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de dibujo de formas](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
