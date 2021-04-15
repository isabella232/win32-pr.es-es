---
description: Crea un objeto ID3DXPRTEngine que puede generar de forma eficaz simulaciones de transferencia Radiance (PRT) precalculadas de una escena 3D.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Función D3DXCreatePRTEngine (D3DX9Mesh. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547931"
---
# <a name="d3dxcreateprtengine-function"></a>D3DXCreatePRTEngine función)

Crea un objeto [**ID3DXPRTEngine**](id3dxprtengine.md) que puede generar de forma eficaz simulaciones de transferencia Radiance (PRT) precalculadas de una escena 3D.

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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) de entrada que modela la escena 3D. Esta malla debe tener una tabla de atributos en la que los vértices se encuentren en un atributo único.

</dd> <dt>

*pAdjacency* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero opcional a una matriz de tres DWORDs por cada tipo que se va a rellenar con índices de caras adyacentes. El número de bytes de esta matriz debe ser al menos ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)). Puede ser **null**.

</dd> <dt>

*ExtractUVs* \[ de\]
</dt> <dd>

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Si **es true**, las texturas se usarán para almacenar vectores ALBEDOS o PRT.

</dd> <dt>

*pBlockerMesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a un objeto de malla [**ID3DXMesh**](id3dxmesh.md) opcional que bloquea la escena 3D. Puede ser **null**.

</dd> <dt>

*ppEngine* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**

Puntero a un objeto [**ID3DXPRTEngine**](id3dxprtengine.md) de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) para combinar varias mallas en una sola interfaz de malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de transferencia Radiance precalculadas](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
