---
description: Usa un sistema de coordenadas a la izquierda para crear una malla que contiene un cilindro.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: Función D3DXCreateCylinder (D3dx9shape.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970903"
---
# <a name="d3dxcreatecylinder-function"></a>Función D3DXCreateCylinder

Usa un sistema de coordenadas a la izquierda para crear una malla que contiene un cilindro.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la malla de cilindros creada.

</dd> <dt>

*Radius1* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radio en el extremo Z negativo. El valor debe ser mayor o igual que 0,0f.

</dd> <dt>

*Radius2* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Radio en el extremo Z positivo. El valor debe ser mayor o igual que 0,0f.

</dd> <dt>

*Longitud* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud del cilindro a lo largo del eje Z.

</dd> <dt>

*Segmentos* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de segmentos sobre el eje principal.

</dd> <dt>

*Pilas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de pilas a lo largo del eje principal.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a la forma de salida, una [**interfaz ID3DXMesh.**](id3dxmesh.md)

</dd> <dt>

*ppAdjacency* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero a una [**interfaz ID3DXBuffer.**](id3dxbuffer.md) Cuando el método devuelve un resultado, este parámetro se rellena con una matriz de tres DWORD por cara que especifican los tres vecinos para cada cara de la malla. Se puede especificar **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

El cilindro creado se centra en el origen y su eje se alinea con el eje Z.

Esta función crea una malla con la opción de creación D3DXMESH MANAGED y el formato flexible de vértice \_ flexible (FVF) [D3DFVF \_ XYZ \| D3DFVF \_ NORMAL.](d3dfvf.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9shape.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de dibujo de formas](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
