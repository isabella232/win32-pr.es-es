---
title: Función D2DSampleInputAtPosition (D2d1effecthelpers.h)
description: Muestra la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para entradas complejas.
ms.assetid: E839287F-91D1-4591-8DE7-1DFC3001A23D
keywords:
- Función Direct2DSampleInputAtPosition de D2D
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
ms.openlocfilehash: c19a455444459e78e2a98fde6386e733c9aa7f1848ed3bb7d2cd6bc22c3062cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698205"
---
# <a name="d2dsampleinputatposition-function"></a>Función D2DSampleInputAtPosition

Muestra la entrada N en una posición de escena absoluta, en lugar de una posición relativa de entrada. Solo está disponible para entradas complejas.

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

La función devuelve **float4**, con el formato TEXCOORDN.

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Vinculación del sombreador de efectos](effect-shader-linking.md)
</dt> <dt>

[Asistentes hlsl](hlsl-helpers.md)
</dt> </dl>

 

 





