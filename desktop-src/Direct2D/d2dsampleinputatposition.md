---
title: Función D2DSampleInputAtPosition (D2d1effecthelpers. h)
description: Muestra la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para las entradas complejas.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Función D2DSampleInputAtPosition Direct2D
topic_type:
- apiref
api_name:
- D2DSampleInputAtPosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e12bba2b83f3956cf4b654c00b0650a6a0ce9a54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681078"
---
# <a name="d2dsampleinputatposition-function"></a>D2DSampleInputAtPosition función)

Muestra la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para las entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Número de entrada.

</dd> <dt>

*UV* \[ de\]
</dt> <dd>

Posición UV.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve una **FLOAT4**, en el formato TEXCOORDN.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra la función utilizada en un ceñido circular.

``` syntax
  
D2D_PS_ENTRY(CircularWrapPS)  
{  
    // TODO: perform math to calculate a circular wrap
  
    // Find the input scene position.  
    float2 inputScenePosition = float2( TODO: add math parameters );  
  
    return D2DSampleInputAtPosition(0, inputScenePosition);  
}
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|----------------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D2d1effecthelpers.hlsli</dt> </dl> |
| Archivo DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Vinculación del sombreador de efectos](effect-shader-linking.md)
</dt> <dt>

[Aplicaciones auxiliares de HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





