---
title: Función D2DGetInput (D2d1effecthelpers.h)
description: Devuelve el color de la entrada N en la coordenada de entrada. Solo está disponible para entradas simples.
ms.assetid: 74B6F814-53C7-4C8C-B45C-3CB23B9D8BED
keywords:
- Función D2DGetInput Direct2D
topic_type:
- apiref
api_name:
- D2DGetInput
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd6ec0fe858149ee53da1f8ca8a02c12756d6a90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163466"
---
# <a name="d2dgetinput-function"></a>Función D2DGetInput

Devuelve el color de la entrada N en la coordenada de entrada. Solo está disponible para entradas simples.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ en\]
</dt> <dd>

Número de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve un **valor float4** que contiene el color RGBA con el formato INPUTN.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra la función que se usa como parte de un efecto compuesto aritmético.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Consulte también los comentarios de [D2D \_ PS \_ ENTRY](d2d-ps-entry.md) para ver otro ejemplo del uso de esta función.

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

 

 





