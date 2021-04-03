---
description: Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un polígono de una cara.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: Función D3DXCreatePolygon (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104083728"
---
# <a name="d3dxcreatepolygon-function"></a>D3DXCreatePolygon función)

Utiliza un sistema de coordenadas de la mano izquierda para crear una malla que contenga un polígono de una cara.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de polígono creada.

</dd> <dt>

*Longitud* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Longitud de cada lado.

</dd> <dt>

*Lados* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de lados del polígono. El valor debe ser mayor o igual que 3.

</dd> <dt>

*ppMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a la forma de salida, una interfaz [**ID3DXMesh**](id3dxmesh.md) .

</dd> <dt>

*ppAdjacency* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una interfaz [**ID3DXBuffer**](id3dxbuffer.md) . Cuando el método devuelve un valor, este parámetro se rellena con una matriz de tres DWORD por cada tipo que especifica los tres vecinos para cada una de las caras de la malla. Se puede especificar **null** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

El polígono creado se centra en el origen.

Esta función crea una malla con la \_ opción de creación administrada D3DXMESH y el formato de vértice flexible [normal de D3DFVF \_ XYZ \| D3DFVF \_ ](d3dfvf.md) (FVF).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9shape. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de dibujo de forma](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
