---
description: Calcula una proyección de la iluminación directa a partir de los vectores de base de la iluminación anterior en vectores de base esférica (SH) que representan el brillo de los incidentes en ubicaciones especificadas.
ms.assetid: ccde7c59-cb82-4d61-822a-e1e9ecea0a28
title: Método ID3DXPRTEngine::ComputeVolumeSamples (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamples
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: edc13e8b6f0e5c725e957be22f1b297f825a4f3b622ced68adf19b34a0b64b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118293506"
---
# <a name="id3dxprtenginecomputevolumesamples-method"></a>Método ID3DXPRTEngine::ComputeVolumeSamples

Calcula una proyección de la iluminación directa a partir de los vectores de base de la iluminación anterior en vectores de base esférica (SH) que representan el brillo de los incidentes en ubicaciones especificadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeVolumeSamples(
  [in]            LPD3DXPRTBUFFER pSurfDataIn,
  [in]            UINT            Order,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p ResalteDataIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada que representa el objeto 3D de la luz anterior.

</dd> <dt>

*Pedido* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la evaluación de SH. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. La evaluación genera coeficientes order-to-order. El grado de la evaluación es Order - 1.

</dd> <dt>

*NumVolSamples.xml* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de ubicaciones de ejemplo.

</dd> <dt>

*pSampleLocs* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posición para cada muestra. Si pSampleLocs es **NULL,** ComputeVolumeSamples calculará las matrices de transferencia en cada vértice de malla. Sin embargo, si pSampleLocs no es **NULL,** debe muestrear en una esfera (establezca UseSphere = **TRUE** y UseCosine = **FALSE** en [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md)); De lo contrario, ComputeVolumeSamples devolverá D3DERR \_ INVALIDCALL.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que proyecta la iluminación directa de la luz anterior en vectores de base SH. Este búfer debe tener asignado el número adecuado de canales de color para la simulación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Este método calcula cómo la luz de la función de radiancia de origen se refleja fuera de la superficie que representa la escena (pSampleDataIn) y llega a cada punto del espacio especificado por pSampleLocs. Los coeficientes sh representan la asignación, en cada punto pSampleLocs, de la radiancia de origen a la radiación del incidente transferido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamplesDirectSH**](id3dxprtengine--computevolumesamplesdirectsh.md)
</dt> </dl>

 

 
