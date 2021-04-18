---
description: Calcular los IMT por triángulo desde datos por vértices. Esta función permite calcular el IMT basándose en cualquier valor de una malla (color, normal, etc.).
ms.assetid: a417a8ad-77b1-49ae-aea0-6a32a154499f
title: Función D3DXComputeIMTFromPerVertexSignal (D3DX9Mesh. h)
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
ms.openlocfilehash: 7b12ea3f15f1a185125da46f575d37ad97dd5622
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718265"
---
# <a name="d3dxcomputeimtfrompervertexsignal-function"></a>D3DXComputeIMTFromPerVertexSignal función)

Calcular los IMT por triángulo desde datos por vértices. Esta función permite calcular el IMT basándose en cualquier valor de una malla (color, normal, etc.).

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

*pmesh* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXMESH**](id3dxmesh.md)**

Un puntero a una malla de entrada (vea [**ID3DXMesh**](id3dxmesh.md)) que contiene la geometría del objeto para calcular el IMT.

</dd> <dt>

*pfVertexSignal* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Un puntero a una matriz de datos por vértice a partir de la cual se calculará IMT. El tamaño de la matriz es uSignalStride \* v, donde v es el número de vértices de la malla.

</dd> <dt>

*uSignalDimension* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de flotantes por vértice.

</dd> <dt>

*uSignalStride* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de bytes por vértice de la matriz. Debe ser un múltiplo de sizeof (float)

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

 

 
