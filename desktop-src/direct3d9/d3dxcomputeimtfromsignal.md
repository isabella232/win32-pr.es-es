---
description: Calcula las IMT por triángulo a partir de una señal personalizada especificada por la aplicación que varía en función de la superficie de la malla (generalmente con una frecuencia mayor que los datos de vértice). La señal se evalúa a través de una función de devolución de llamada especificada por el usuario.
ms.assetid: f1d96021-0b7d-43e6-b51b-71a90d2f5ad8
title: Función D3DXComputeIMTFromSignal (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d645e12f7159963f9b9bc5abeb960aee0bac2282537c482465be3ea08690181
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299417"
---
# <a name="d3dxcomputeimtfromsignal-function"></a>Función D3DXComputeIMTFromSignal

Calcula las IMT por triángulo a partir de una señal personalizada especificada por la aplicación que varía en función de la superficie de la malla (generalmente con una frecuencia mayor que los datos de vértice). La señal se evalúa a través de una función de devolución de llamada especificada por el usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeIMTFromSignal(
  _In_  LPD3DXMESH              pMesh,
  _In_  DWORD                   dwTextureIndex,
  _In_  UINT                    uSignalDimension,
  _In_  FLOAT                   fMaxUVDistance,
  _In_  DWORD                   dwOptions,
  _In_  LPD3DXIMTSIGNALCALLBACK pSignalCallback,
  _In_  VOID                    *pUserData,
        LPD3DXUVATLASCB         pStatusCallback,
        LPVOID                  pUserContext,
  _Out_ LPD3DXBUFFER            *ppIMTData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada (vea [**ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el IMT.

</dd> <dt>

*dwTextureIndex* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura de base cero que identifica qué conjunto de coordenadas de textura usar.

</dd> <dt>

*uSignalDimension* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de componentes de cada punto de datos de la señal.

</dd> <dt>

*fMaxUVDistance* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Distancia máxima entre vértices; El algoritmo continúa subdividiendo hasta que la distancia entre todos los vértices es menor o igual que fMaxUVDistance.

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de ajuste de textura. Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pSignalCallback* \[ En\]
</dt> <dd>

Tipo: **[LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md)**

Puntero a una función de evaluador proporcionada por el usuario, que se usará para calcular el valor de señal en coordenadas U,V arbitrarias. La función sigue el prototipo de [LPD3DXIMTSIGNALCALLBACK](lpd3dximtsignalcallback.md).

</dd> <dt>

*pUserData* \[ En\]
</dt> <dd>

Tipo: **\* VOID**

Puntero a un valor definido por el usuario que se pasa a la función de devolución de llamada de señal. Normalmente lo usa una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

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

## <a name="remarks"></a>Comentarios

Esta función requiere que la malla de entrada contenga una asignación de textura de señal a malla (es decir, coordenadas de textura). Permite al usuario definir una señal arbitrariamente sobre la superficie de la malla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Uso de UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
