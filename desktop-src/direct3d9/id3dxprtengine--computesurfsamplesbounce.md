---
description: Calcula muestras de transferencia Radiance (PRT) precalculadas para un punto arbitrario (y un vector normal).
ms.assetid: 862a9067-5c5e-4428-86f4-ebef653411b9
title: 'ID3DXPRTEngine:: ComputeSurfSamplesBounce (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 55cea3e87850273b6ea8d190422bd77afeb831f4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362810"
---
# <a name="id3dxprtenginecomputesurfsamplesbounce-method"></a>ID3DXPRTEngine:: ComputeSurfSamplesBounce (método)

Calcula muestras de transferencia Radiance (PRT) precalculadas para un punto arbitrario (y un vector normal).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeSurfSamplesBounce(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut,
  [in, out]       LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSurfDataIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el Radiance de origen del objeto 3D. Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*NumSamples* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de ubicaciones de ejemplo.

</dd> <dt>

*pSampleLocs* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posición de cada ejemplo.

</dd> <dt>

*pSampleNorms* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Vector normal para cada ubicación de ejemplo.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela la contribución de iluminación directa hasta el punto mediante la aproximación armónica esférica (SH).

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que es la suma de todas las salidas pDataOut anteriores. Puede ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSurfSamplesDirectSH**](id3dxprtengine--computesurfsamplesdirectsh.md)
</dt> </dl>

 

 
