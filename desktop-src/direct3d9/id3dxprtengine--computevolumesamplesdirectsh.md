---
description: Calcula una proyección de iluminación distanl en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.
ms.assetid: 4d07b288-aec1-48eb-8d27-f3d7d8cfb69e
title: 'ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (método) (D3DX9Mesh. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708061"
---
# <a name="id3dxprtenginecomputevolumesamplesdirectsh-method"></a>ID3DXPRTEngine:: ComputeVolumeSamplesDirectSH (método)

Calcula una proyección de iluminación distanl en vectores de base de armónicos esféricos (SH) que representan el incidente radiance en las ubicaciones especificadas.

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

*Ordenar* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la representación SH de la iluminación Distant. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. El grado de evaluación es Orderen-1.

</dd> <dt>

*OrderOut* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Orden de la representación SH de la iluminación local. Debe estar en el intervalo de [D3DXSH \_ MINORDER](other-d3dx-constants.md) a D3DXSH \_ MAXORDER, ambos incluidos. El grado de evaluación es OrderOut-1.

</dd> <dt>

*NumVolSamples.xml* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de ubicaciones de ejemplo.

</dd> <dt>

*pSampleLocs* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR3**](d3dxvector3.md) \***

Posición de cada ejemplo.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida que proyecta la iluminación lejana en vectores de base SH. Este búfer debe tener asignado el número adecuado de canales de color para la simulación. Este método genera orderis ² \* OrderOut "² scalars per Channel en cada ubicación de ejemplo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método calcula cómo llega la luz de un origen distante en cada punto del espacio especificado por pSampleLocs. Los coeficientes SH representan la asignación, en cada punto de pSampleLocs, de Radiance de origen a Radiance de incidente transferido.

Para usar este método correctamente, debe establecer el muestreo en una esfera con UseSphere = **true** y UseCosine = **false** en [**ID3DXPRTEngine:: SetSamplingInfo**](id3dxprtengine--setsamplinginfo.md); de lo contrario, este método devolverá un error con D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeVolumeSamples**](id3dxprtengine--computevolumesamples.md)
</dt> </dl>

 

 
