---
description: Devuelve una malla con modificaciones resultantes del muestreo espacial adaptable. La malla devuelta solo contiene posiciones, normales y coordenadas de textura (si se definen).
ms.assetid: 21447733-b27b-4906-8c0e-7089dec71b5b
title: 'ID3DXPRTEngine:: GetAdaptedMesh (método) (D3DX9Mesh. h)'
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
ms.openlocfilehash: 3d012344a5dfbc1bc17780cb4ab9a53820fe34f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362738"
---
# <a name="id3dxprtenginegetadaptedmesh-method"></a>ID3DXPRTEngine:: GetAdaptedMesh (método)

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

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a un dispositivo [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que se usa para crear la malla de salida.

</dd> <dt>

*pFaceRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a la superficie de la malla original que se ha dividido para generar la superficie actual.

</dd> <dt>

*pVertRemap* \[ in, out\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero a una matriz de destino que contiene los tres vértices de malla originales que son los elementos primarios del vértice actual.

</dd> <dt>

*pfVertWeights* \[ in, out\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una matriz de destino que contiene factores de mezcla para los vértices de pVertRemap.

</dd> <dt>

*ppMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)\***

Puntero al objeto de malla [**ID3DXMesh**](id3dxmesh.md) de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

pVertRemap y pfVertWeights se pueden usar para interpolar cualquier valor por vértice en la malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
