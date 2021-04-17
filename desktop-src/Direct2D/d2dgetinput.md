---
title: Función D2DGetInput (D2d1effecthelpers. h)
description: Devuelve el color de entrada N en la coordenada de entrada. Solo está disponible para entradas simples.
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661104"
---
# <a name="d2dgetinput-function"></a>D2DGetInput función)

Devuelve el color de entrada N en la coordenada de entrada. Solo está disponible para entradas simples.

## <a name="syntax"></a>Sintaxis

``` syntax
float4 WINAPI D2DGetInput(
  in uint N
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*N* \[ in\]
</dt> <dd>

Número de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

La función devuelve una **FLOAT4**, que contiene el color RGBA en el formato de entrada.

## <a name="remarks"></a>Observaciones

En el ejemplo siguiente se muestra la función que se utiliza como parte de un efecto compuesto aritmético.

``` syntax
  
D2D_PS_ENTRY(PS_NAME)  
{  
    MIN_TYPE(float4) sourceColor = D2DGetInput(0);  
    MIN_TYPE(float4) destColor   = D2DGetInput(1);  
      
    MIN_TYPE(float4) output = // TODO: add math to composite source and dest

    return output;  
}  
```

Además, consulte la entrada de comentarios [de \_ D2D \_ PS](d2d-ps-entry.md) para ver otro ejemplo del uso de esta función.

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

 

 





