---
description: Divide una revisión de superficie de orden superior triangular en una malla de triángulo.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Función D3DXTessellateTriPatch (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateTriPatch
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1cae3ff9709cb74e15c176abc0e738e4f12d1417eec1d040b90269b7e3cbc6c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119122717"
---
# <a name="d3dxtessellatetripatch-function"></a>Función D3DXTessellateTriPatch

Divide una revisión de superficie de orden superior triangular en una malla de triángulo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXTessellateTriPatch(
  _In_          LPDIRECT3DVERTEXBUFFER9 pVB,
  _In_    const FLOAT                   *pNumSegs,
  _In_    const D3DVERTEXELEMENT9       *pInDecl,
  _In_    const D3TRIPATCH_INFO         *pTriPatchInfo,
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

Puntero a una matriz de tres valores de punto flotante que identifican el número de segmentos en los que se debe dividir cada borde de la revisión de triángulo al teselar. Vea [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Estructura de declaración de vértice que define los datos del vértice. Vea [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> <dt>

*pTriPatchInfo* \[ En\]
</dt> <dd>

Tipo: **const [**D3TRIPATCH \_ INFO**](d3dtripatch-info.md) \***

Describe una revisión de triángulo. Vea [**D3DTRIPATCH \_ INFO**](d3dtripatch-info.md).

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

Use [**D3DXTriPatchSize para**](d3dxtripatchsize.md) obtener el número de vértices e índices de salida que necesita la función de teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
