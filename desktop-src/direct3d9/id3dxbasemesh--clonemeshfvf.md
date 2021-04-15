---
description: Clona una malla con un código de formato de vértice flexible (FVF).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'ID3DXBaseMesh:: CloneMeshFVF (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707853"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a>ID3DXBaseMesh:: CloneMeshFVF (método)

Clona una malla con un código de formato de vértice flexible (FVF).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas [**D3DXMESH**](./d3dxmesh.md) que especifican las opciones de creación de la malla.

</dd> <dt>

*FVF* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de códigos de FVF, que especifica el formato de vértice de los vértices de la malla de salida. Para obtener los valores de los códigos, vea [D3DFVF](d3dfvf.md).

</dd> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el objeto de dispositivo asociado a la malla.

</dd> <dt>

*ppCloneMesh* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Dirección de un puntero a una interfaz [**ID3DXMesh**](id3dxmesh.md) que representa la malla clonada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

**ID3DXBaseMesh:: CloneMeshFVF** se usa para volver a formatear y cambiar el diseño de los datos de vértices. Esto se hace creando un nuevo objeto de malla. Por ejemplo, úselo para agregar espacio para las normales, coordenadas de textura, colores, pesos, etc., que no estaban presentes antes.

[**ID3DXBaseMesh:: UpdateSemantics**](id3dxbasemesh--updatesemantics.md) actualiza la declaración de vértices con información semántica diferente sin cambiar el diseño del búfer de vértices. Este método no modifica el contenido del búfer de vértices. Por ejemplo, úselo para cambiar la etiqueta de una coordenada de textura 3D como binormal o tangente, o viceversa.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> <dt>

[**D3DXFVFFromDeclarator**](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
