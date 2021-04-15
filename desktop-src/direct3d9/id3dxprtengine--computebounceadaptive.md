---
description: Calcula el Radiance de origen resultante de un único rebote de luz interreflejada mediante el muestreo adaptable.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: 'ID3DXPRTEngine:: ComputeBounceAdaptive (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounceAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 787dee9719e0450dd39ebb19f4c06ee76013cb07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105708064"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>ID3DXPRTEngine:: ComputeBounceAdaptive (método)

Calcula el Radiance de origen resultante de un único rebote de luz interreflejada mediante el muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximar con más precisión la señal de transferencia Radiance (PRT) precalculada. Este método se puede usar para cualquier escena iluminada, incluido un modelo PRT basado en armónico (SH).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ComputeBounceAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDataIn* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada que representa el objeto 3D del rebote de luz anterior. Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*AdaptiveThresh* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Umbral del vector de PRT que se va a usar para subdividir los vértices de malla y caras. Si es menor que 1E-6F, se especifica un valor predeterminado de 1E-6F.

</dd> <dt>

*MinEdgeLength* \[ de\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Longitud mínima del borde de la superficie que se generará en el muestreo adaptable. Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo. Si es cero, se especifica un valor predeterminado de 4.

</dd> <dt>

*MaxSubdiv* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Nivel máximo de subdivisión de una esfera que se usará en el muestreo adaptable.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de salida. Este búfer de salida debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que mantiene una suma en ejecución de pDataOut con cada cálculo de rebote de luz. Puede ser **null**.

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

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
