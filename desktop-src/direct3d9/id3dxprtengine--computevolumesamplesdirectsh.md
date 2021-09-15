---
description: Calcula una proyección de iluminación lejana en vectores de base armónicos esféricos (SH) que representan el brillo de los incidentes en ubicaciones especificadas.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: Método ID3DXPRTEngine::ComputeVolumeSamplesDirectSH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeVolumeSamplesDirectSH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 757e227907eab73848f43b2b8e2f40f9b4b1071b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127359339"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>Método ID3DXPRTEngine::ComputeVolumeSamplesDirectSH

Calcula una proyección de iluminación lejana en vectores de base armónicos esféricos (SH) que representan el brillo de los incidentes en ubicaciones especificadas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeVolumeSamplesDirectSH(
  [in]            UINT            OrderIn,
  [in]            UINT            OrderOut,
  [in]            UINT            NumVolSamples.xml,
  [in]      const D3DXVECTOR3     *pSampleLocs,
  [in, out]       LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OrderIn* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la representación SH de iluminación lejana. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. El grado de la evaluación es OrderIn - 1.

</dd> <dt>

*OrderOut* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Orden de la representación SH de la iluminación local. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos inclusive. El grado de la evaluación es OrderOut - 1.

</dd> <dt>

*NumVolSamples.xml* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de ubicaciones de ejemplo.

</dd> <dt>

*pSampleLocs* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posición para cada muestra.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida que proyecta la iluminación lejana en vectores de base SH. Este búfer debe tener asignado el número adecuado de canales de color para la simulación. Este método genera OrderInntes \* OrderOut"miento escalares por canal en cada ubicación de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método calcula cómo llega la luz de un origen lejano a cada punto del espacio especificado por pSampleLocs. Los coeficientes sh representan la asignación, en cada punto pSampleLocs, de la radiancia de origen a la radiación del incidente transferido.

Para usar este método correctamente, debe establecer el muestreo en una esfera con UseSphere = **TRUE** y UseCosine = **FALSE** en [**ID3DXPRTEngine::SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); De lo contrario, este método devolverá un error con D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
