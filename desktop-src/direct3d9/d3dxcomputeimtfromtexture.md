---
description: Calcula las IMT por triángulo a partir de una textura asignada a una malla, que se usará opcionalmente como entrada para las funciones D3DX UVAtlas.
ms.assetid: 6671edc4-e494-4847-ae99-b9e56651a875
title: Función D3DXComputeIMTFromTexture (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromTexture
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2fbed0411f3562e3a05ec2ec4df99dfad6d8c902
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127569324"
---
# <a name="d3dxcomputeimtfromtexture-function"></a>Función D3DXComputeIMTFromTexture

Calcula las IMT por triángulo a partir de una textura asignada a una malla, que se usará opcionalmente como entrada para las funciones [D3DX UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeIMTFromTexture(
  _In_  LPD3DXMESH         pMesh,
  _In_  LPDIRECT3DTEXTURE9 pTexture,
  _In_  DWORD              dwTextureIndex,
  _In_  DWORD              dwOptions,
        LPD3DXUVATLASCB    pStatusCallback,
        LPVOID             pUserContext,
  _Out_ LPD3DXBUFFER       *ppIMTData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada (vea [**ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el IMT.

</dd> <dt>

*pTexture* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Puntero a la textura (vea [**IDirect3DTexture9)**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)que se asigna a la malla.

</dd> <dt>

*dwTextureIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura de base cero que identifica qué conjunto de coordenadas de textura usar.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de ajuste de textura. Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DRVALLASCB](lpd3dxuvatlascb.md)**

Puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado. Normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> <dt>

*ppIMTData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta. Esta matriz se puede proporcionar como entrada a las funciones [D3DX UVAtlas para](dx9-graphics-reference-d3dx-functions-uvatlas.md) priorizar la asignación de espacio de textura en la parametrización de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Dada una textura que se asigna sobre la superficie de la malla, el algoritmo calcula el IMT para cada cara. Esto hará que los triángulos que contienen datos de señal de frecuencia inferior ocuparán menos espacio en el atlas de textura final cuando se parametrizan con las funciones UVAtlas. Se supone que la textura se interpola sobre la malla de forma bilineal.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones DE UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Uso de UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
