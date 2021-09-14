---
title: Función D2DSampleInputAtPosition (D2d1effecthelpers.h)
description: Muestrea la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para entradas complejas.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163449"
---
# <a name="d2dsampleinputatposition-function"></a>Función D2DSampleInputAtPosition

Muestrea la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para entradas complejas.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DSampleInputAtPosition(
  in uint N,
  in float2 uv
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ en\]
</dt> <dd>

Número de entrada.

</dd> <dt>

*uv* \[ En\]
</dt> <dd>

Posición uv.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve **un valor float4**, con el formato TEXCOORDN.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra la función utilizada en un ajuste circular.

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



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Vinculación del sombreador de efectos](effect-shader-linking.md)
</dt> <dt>

[Asistentes hlsl](hlsl-helpers.md)
</dt> </dl>

 

 





