---
description: Calcular los IMT por triángulo a partir de los datos de textura. Esta función es similar a D3DXComputeIMTFromTexture, pero usa una matriz Float para pasar los datos y puede calcular valores de mayor dimensiones que 4.
ms.assetid: 4a151184-e67e-41e9-83c6-63da72f262fa
title: Función D3DXComputeIMTFromPerTexelSignal (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerTexelSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a3db71fbc931f7bdb3e73c8d949a163607e66c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721465"
---
# <a name="d3dxcomputeimtfrompertexelsignal-function"></a>D3DXComputeIMTFromPerTexelSignal función)

Calcular los IMT por triángulo a partir de los datos de textura. Esta función es similar a [**D3DXComputeIMTFromTexture**](d3dxcomputeimtfromtexture.md), pero usa una matriz Float para pasar los datos y puede calcular valores de mayor dimensiones que 4.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeIMTFromPerTexelSignal(
  _In_  LPD3DXMESH      pMesh,
  _In_  DWORD           dwTextureIndex,
  _In_  FLOAT           *pfTexelSignal,
  _In_  UINT            uWidth,
  _In_  UINT            uHeight,
  _In_  UINT            uSignalDimension,
  _In_  UINT            uComponents,
  _In_  DWORD           dwOptions,
        LPD3DXUVATLASCB pStatusCallback,
        LPVOID          pUserContext,
  _Out_ LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.

</dd> <dt>

*dwTextureIndex* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Índice de coordenadas de textura basado en cero que identifica el conjunto de coordenadas de textura que se va a usar.

</dd> <dt>

*pfTexelSignal* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)\***

Puntero a una matriz de textura de entrada de la que se calculará IMT. El tamaño de la matriz es uWidth \* uHeight \* uComponents.

</dd> <dt>

*uWidth* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Ancho de la textura en píxeles.

</dd> <dt>

*uHeight* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Alto de textura en píxeles.

</dd> <dt>

*uSignalDimension* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos flotantes por componente en cada elemento de la matriz de señal.

</dd> <dt>

*uComponents* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

El número de componentes de cada textura.

</dd> <dt>

*dwOptions* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de ajuste de textura. Se trata de una combinación de una o varias [**marcas D3DXIMT**](./d3dximt-flags.md).

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DXUVATLASCB](lpd3dxuvatlascb.md)**

Un puntero a una función de devolución de llamada para supervisar el progreso del cálculo de IMT.

</dd> <dt>

*pUserContext* 
</dt> <dd>

Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**

Puntero a una variable definida por el usuario que se pasa a la función de devolución de llamada de estado. Lo suele usar una aplicación para pasar un puntero a una estructura de datos que proporciona información de contexto para la función de devolución de llamada.

</dd> <dt>

*ppIMTData* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Un puntero al búfer (vea [**ID3DXBuffer**](id3dxbuffer.md)) que contiene la matriz IMT devuelta. Esta matriz se puede proporcionar como entrada para las [funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) de D3DX a fin de dar prioridad a la asignación de espacio de textura en la parametrización de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md)
</dt> <dt>

[Usar UVAtlas (Direct3D 9)](using-uvatlas.md)
</dt> </dl>

 

 
