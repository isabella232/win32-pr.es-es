---
description: Crea un objeto ID3DXPRTEngine que puede generar eficazmente simulaciones de transferencia de radiancia precalutadas (PRT) de una escena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Función D3DXCreatePRTEngine (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361276"
---
# <a name="d3dxcreateprtengine-function"></a>Función D3DXCreatePRTEngine

Crea un [**objeto ID3DXPRTEngine**](id3dxprtengine.md) que puede generar eficazmente simulaciones de transferencia de radiancia precalutadas (PRT) de una escena 3D.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto de malla [**ID3DXMesh de**](id3dxmesh.md) entrada que modela la escena 3D. Esta malla debe tener una tabla de atributos en la que los vértices se encuentran en un atributo único.

</dd> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero opcional a una matriz de tres DWORD por cara que se va a rellenar con índices faciales adyacentes. El número de bytes de esta matriz debe ser al menos ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)). Puede ser **NULL.**

</dd> <dt>

*ExtractUVs* \[ En\]
</dt> <dd>

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Si **es TRUE,** se usarán texturas para almacenar vectores albedos o PRT.

</dd> <dt>

*pBlockerMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) opcional que bloquea la escena 3D. Puede ser **NULL.**

</dd> <dt>

*ppEngine* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Puntero a un objeto [**ID3DXPRTEngine de**](id3dxprtengine.md) salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para combinar varias mallas en una única interfaz de malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de transferencia de radiancia precalutadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
