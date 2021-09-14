---
description: Calcula el brillo de origen resultante de un único salto de luz interreferida, mediante el muestreo adaptable.
ms.assetid: 61f8cecd-d95a-4f02-929e-02f2bce5bde9
title: Método ID3DXPRTEngine::ComputeBounceAdaptive (D3DX9Mesh.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974766"
---
# <a name="id3dxprtenginecomputebounceadaptive-method"></a>Método ID3DXPRTEngine::ComputeBounceAdaptive

Calcula el brillo de origen resultante de un único salto de luz interreferida, mediante el muestreo adaptable. Este método genera nuevos vértices y caras en la malla para aproximar de forma más precisa la señal de transferencia de radiancia precalutada (PRT). Este método se puede usar para cualquier escena de iluminación, incluido un modelo PRT basado en armónica esférica (SH).

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

*pDataIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada que representa el objeto 3D de la luz anterior. Este búfer de entrada debe tener asignado el número adecuado de canales de color para la simulación.

</dd> <dt>

*AdaptiveThresh* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Umbral en el vector PRT que se usará para subdividir vértices y caras de malla. Si es menor que 1e-6f, se especifica un valor predeterminado de 1e-6f.

</dd> <dt>

*MinEdgeLength* \[ En\]
</dt> <dd>

Tipo: **[ **FLOAT**](../winprog/windows-data-types.md)**

Longitud mínima del borde de la cara que se generará en el muestreo adaptable. Si el método determina que el valor es demasiado pequeño, se especifica un valor dependiente del modelo. Si es cero, se especifica un valor predeterminado de 4.

</dd> <dt>

*MaxSubdiv* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Nivel máximo de subdivisión de una cara que se usará en el muestreo adaptable.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida. Este búfer de salida debe tener el número adecuado de canales de color asignados para la simulación.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) opcional que mantiene una suma en ejecución de pDataOut con cada cálculo de desenlazamiento. Puede ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
