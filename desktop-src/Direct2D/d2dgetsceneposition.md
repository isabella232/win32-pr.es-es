---
title: Función D2DGetScenePosition (D2d1effecthelpers.h)
description: Devuelve el valor de la posición de la \_ escena de entrada. Solo está disponible cuando D2D \_ REQUIERE QUE SCENE POSITION se declare en el archivo de \_ \_ origen.
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
ms.openlocfilehash: fbcd7a1ee987cf64a92aa76b0f8910bee1c9a15465872bbd3ccfe2502629f700
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641645"
---
# <a name="d2dgetsceneposition-function"></a>Función D2DGetScenePosition

Devuelve el valor de la posición de la \_ escena de entrada. Solo está disponible cuando D2D \_ REQUIERE QUE SCENE POSITION se declare en el archivo de \_ \_ origen.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DGetScenePosition(void);
```

## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

La función devuelve un **valor float4** con el formato SCENE \_ POSITION.

## <a name="remarks"></a>Comentarios

En el ejemplo siguiente se muestra el uso de la función para generar un patrón de disolver.

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

[Asistentes hlsl](hlsl-helpers.md)
</dt> </dl>

 

 





