---
description: Calcule las IMT por triángulo a partir de datos por vértice. Esta función permite calcular la IMT en función de cualquier valor de una malla (color, normal, etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Función D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeIMTFromPerVertexSignal
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 41d635bf436e139e4c44db75b1057cebc3a50cfee114a35bfc75a9de84abc404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299462"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>Función D3DXComputeIMTFromPerVertexSignal

Calcule las IMT por triángulo a partir de datos por vértice. Esta función permite calcular la IMT en función de cualquier valor de una malla (color, normal, etc.).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXComputeIMTFromPerVertexSignal(
  _In_        LPD3DXMESH      pMesh,
  _In_  const FLOAT           *pfVertexSignal,
  _In_        UINT            uSignalDimension,
  _In_        UINT            uSignalStride,
  _In_        DWORD           dwOptions,
              LPD3DXUVATLASCB pStatusCallback,
              LPVOID          pUserContext,
  _Out_       LPD3DXBUFFER    *ppIMTData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pMesh* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Puntero a una malla de entrada (vea [**ID3DXMesh)**](id3dxmesh.md)que contiene la geometría del objeto para calcular el IMT.

</dd> <dt>

*pfVertexSignal* \[ En\]
</dt> <dd>

Tipo: **const [**FLOAT**](../winprog/windows-data-types.md) \***

Puntero a una matriz de datos por vértice a partir de los cuales se calculará IMT. El tamaño de la matriz es uSignalStride v, donde \* v es el número de vértices de la malla.

</dd> <dt>

*uSignalDimension* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de flotantes por vértice.

</dd> <dt>

*uSignalStride* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de bytes por vértice de la matriz. Debe ser un múltiplo de sizeof(float)

</dd> <dt>

*dwOptions* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Opciones de ajuste de textura. Se trata de una combinación de una o varias [**marcas D3DXIMT.**](./d3dximt-flags.md)

</dd> <dt>

*pStatusCallback* 
</dt> <dd>

Tipo: **[LPD3DVATVATLASCB](lpd3dxuvatlascb.md)**

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

Puntero al búfer (vea [**ID3DXBuffer)**](id3dxbuffer.md)que contiene la matriz IMT devuelta. Esta matriz se puede proporcionar como entrada a las funciones [DE UVAtlas](dx9-graphics-reference-d3dx-functions-uvatlas.md) D3DX para priorizar la asignación de espacio de textura en la parametrización de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK; de lo contrario, el valor es D3DERR \_ INVALIDCALL.

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

 

 
