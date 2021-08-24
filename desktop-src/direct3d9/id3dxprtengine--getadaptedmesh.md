---
description: Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable. La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: Método ID3DXPRTEngine::GetAdaptedMesh (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetAdaptedMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5e38937628bc36f49059bcb3e798a6d13e538c572c1c5fb6ef20865ed05385d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747675"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>Método ID3DXPRTEngine::GetAdaptedMesh

Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable. La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAdaptedMesh(
  [in]      LPDIRECT3DDEVICE9 pDevice,
  [in, out] UINT              *pFaceRemap,
  [in, out] UINT              *pVertRemap,
  [in, out] FLOAT             *pfVertWeights,
  [out]     LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a un [**dispositivo IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para crear la malla de salida.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a la cara de malla original que se dividió para generar la cara actual.

</dd> <dt>

*pVertRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de destino que contiene los tres vértices de malla originales que son los elementos superiores del vértice actual.

</dd> <dt>

*pfVertWeights* \[ in, out\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)\***

Puntero a una matriz de destino que contiene factores de combinación para los vértices pVertRemap.

</dd> <dt>

*ppMesh* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero al objeto de malla [**ID3DXMesh**](id3dxmesh.md) de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Comentarios

pVertRemap y pfVertWeights se pueden usar para interpolar cualquier valor por vértice sobre la malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
