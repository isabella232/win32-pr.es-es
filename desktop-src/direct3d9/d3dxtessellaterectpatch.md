---
description: Tesola una revisión rectangular de superficie de orden superior en una malla de triángulo.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Función D3DXTessellateRectPatch (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateRectPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b7fb3ab1c47ded6fe6ca6548ca6c90b3027e30280acf819d5d024fd0bd554d58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119055"
---
# <a name="d3dxtessellaterectpatch-function"></a>Función D3DXTessellateRectPatch

Tesola una revisión rectangular de superficie de orden superior en una malla de triángulo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXTessellateRectPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3DRECTPATCH_INFO       *pRectPatchInfo,
  _Inout_       LPD3DXMESH              pMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVB* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Búfer de vértices que contiene los datos de revisión.

</dd> <dt>

*pNumSegs* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero a una matriz de cuatro valores de punto flotante que identifican el número de segmentos en los que se debe dividir cada borde de la revisión del rectángulo cuando se tesela. Vea [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).

</dd> <dt>

*pInDecl* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Estructura de declaración de vértice que define los datos del vértice. Vea [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> <dt>

*pRectPatchInfo* \[ En\]
</dt> <dd>

Tipo: **const [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md) \***

Describe una revisión rectangular. Vea [**D3DRECTPATCH \_ INFO**](d3drectpatch-info.md).

</dd> <dt>

*pMesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a la malla creada. Vea [**ID3DXMesh.**](id3dxmesh.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Use [**D3DXRectPatchSize para**](d3dxrectpatchsize.md) obtener el número de vértices de salida e índices que necesita la función de teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
