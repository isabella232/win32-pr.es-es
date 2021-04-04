---
description: Tessellates una revisión de la superficie de orden superior triangular en una malla de triángulo.
ms.assetid: bcc9143f-fec0-491a-8d32-1df961b8dade
title: Función D3DXTessellateTriPatch (D3DX9Mesh. h)
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
ms.openlocfilehash: 61d5a426f9fe3331b85c4a881219319622283820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821047"
---
# <a name="d3dxtessellatetripatch-function"></a>D3DXTessellateTriPatch función)

Tessellates una revisión de la superficie de orden superior triangular en una malla de triángulo.

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

*pVB* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DVERTEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexbuffer9)**

Búfer de vértices que contiene los datos de revisión.

</dd> <dt>

*pNumSegs* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Puntero a una matriz de tres valores de punto flotante que identifican el número de segmentos en los que cada borde de la revisión del triángulo debe dividirse cuando se tesela. Vea [**\_ información de D3DTRIPATCH**](d3dtripatch-info.md).

</dd> <dt>

*pInDecl* \[ de\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Estructura de declaración de vértices que define los datos de vértices. Vea [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

</dd> <dt>

*pTriPatchInfo* \[ de\]
</dt> <dd>

Tipo: **const [**D3TRIPATCH \_ info**](d3dtripatch-info.md) \***

Describe una revisión de triángulo. Vea [**\_ información de D3DTRIPATCH**](d3dtripatch-info.md).

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

Use [**D3DXTriPatchSize**](d3dxtripatchsize.md) para obtener el número de vértices y índices de salida que necesita la función de teselación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXTessellateRectPatch**](d3dxtessellaterectpatch.md)
</dt> </dl>

 

 
