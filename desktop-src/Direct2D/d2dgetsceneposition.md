---
title: Función D2DGetScenePosition (D2d1effecthelpers. h)
description: Devuelve el valor de la posición de la escena de entrada \_ . Solo está disponible cuando \_ D2D \_ requiere \_ que la posición de la escena se declare en el archivo de código fuente.
ms.assetid: 451E4C31-D93D-44B6-81D1-AC5FD986ACBD
keywords:
- Función D2DGetScenePosition Direct2D
topic_type:
- apiref
api_name:
- D2DGetScenePosition
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace0ee4d60f8c140825e41ba47de941bca09e67c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661211"
---
# <a name="d2dgetsceneposition-function"></a>D2DGetScenePosition función)

Devuelve el valor de la posición de la escena de entrada \_ . Solo está disponible cuando \_ D2D \_ requiere \_ que la posición de la escena se declare en el archivo de código fuente.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La función devuelve una **FLOAT4** en el formato posición de la escena \_ .

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra el uso de la función para generar un patrón de resolución.

``` syntax
D2D_PS_ENTRY(BlendDissolve)  
{  
    min16float4 dest   = D2DGetInput(0);  
    min16float4 source = D2DGetInput(1);  
  
    min16float4 color = dest;  
  
    if ((source.a > 0.0) && (source.a >= Rand((min16float2)D2DGetScenePosition().xy)))  
    {  
        // TODO: perform  dissovlve math
    }  
  
    return color;  
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

 

 





