---
description: Tessellates una revisión de la superficie de orden superior rectangular en una malla de triángulo.
ms.assetid: d941d994-8a13-49ff-a0b1-b21a3f84ed78
title: Función D3DXTessellateRectPatch (D3DX9Mesh. h)
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
ms.openlocfilehash: 887f0035b50efd860149410e50dd6abff301968d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280299"
---
# <a name="d3dxtessellaterectpatch-function"></a>D3DXTessellateRectPatch función)

Tessellates una revisión de la superficie de orden superior rectangular en una malla de triángulo.

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

*pVB* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Búfer de vértices que contiene los datos de revisión.

</dd> <dt>

*pNumSegs* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntero a una matriz de cuatro valores de punto flotante que identifican el número de segmentos en los que cada borde de la revisión del rectángulo debe dividirse cuando se tesela. Vea [**\_ información de D3DRECTPATCH**](d3drectpatch-info.md).

</dd> <dt>

*pInDecl* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Estructura de declaración de vértices que define los datos de vértices. Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pRectPatchInfo* \[ de\]
</dt> <dd>

Tipo: **const [**D3DRECTPATCH \_ info**](d3drectpatch-info.md) \***

Describe una revisión rectangular. Vea [**\_ información de D3DRECTPATCH**](d3drectpatch-info.md).

</dd> <dt>

*pmesh* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a la malla creada. Vea [**ID3DXMesh**](id3dxmesh.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Use [**D3DXRectPatchSize**](d3dxrectpatchsize.md) para obtener el número de vértices y índices de salida que necesita la función de teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateTriPatch**](d3dxtessellatetripatch.md)
</dt> </dl>

 

 
