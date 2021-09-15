---
description: Calcula, en un punto arbitrario que no está en una malla, un vector de transferencia que asigna la radiancia de origen (representada por una aproximación de armónica esférica (SH) para salir de la luminosidad.
ms.assetid: 44790465-440d-4426-b780-ed872fbf8efb
title: Método ID3DXPRTEngine::ComputeSamplesDirectSH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSurfSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 03adb1729a8a2e771ea681ccbdd180999d3adcbf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359341"
---
# <a name="id3dxprtenginecomputesurfsamplesdirectsh-method"></a>Método ID3DXPRTEngine::ComputeSampleSamplesDirectSH

Calcula, en un punto arbitrario que no está en una malla, un vector de transferencia que asigna la radiancia de origen (representada por una aproximación de armónica esférica (SH) para salir de la luminosidad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeSurfSamplesDirectSH(
  [in]            UINT            SHOrder,
  [in]            UINT            NumSamples,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in]      const D3DXVECTOR3     *pSampleNorms,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SHOrder* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la aproximación de SH que se usará.

</dd> <dt>

*NumSamples* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de ubicaciones de ejemplo.

</dd> <dt>

*pSampleLocs* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posición para cada muestra.

</dd> <dt>

*pSampleNorms* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Vector normal para cada ubicación de muestra.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que modela la contribución de iluminación directa al punto, mediante la aproximación SH.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

No use un búfer de textura al llamar a este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeDirectLightingSH**](id3dxprtengine--computedirectlightingsh.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeSamplesBounce**](id3dxprtengine--computesurfsamplesbounce.md)
</dt> </dl>

 

 
