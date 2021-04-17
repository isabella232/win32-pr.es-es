---
title: D2D_PS_ENTRY función (D2d1effecthelpers. h)
description: Macro que define un punto de entrada del sombreador de píxeles con el nombre de función especificado.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY función Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7525416eed7700709d02d2ec17823cd57a8c12ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670376"
---
# <a name="d2d_ps_entry-function"></a>D2D \_ \_ función de entrada PS

Macro que define un punto de entrada del sombreador de píxeles con el nombre de función especificado.

## <a name="syntax"></a>Sintaxis

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombreentrada* \[ de\]
</dt> <dd>

Nombre del punto de entrada del sombreador de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use esta macro en lugar de especificar la firma de entrada de punto de entrada de la manera normal: todos los parámetros son implícitos y se agregan mediante Direct2D durante la compilación según el tipo de destino de compilación (sombreador completo o función de exportación).

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

En este breve ejemplo, observe que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes que la función de entrada, la entrada se recupera llamando a [D2DGetInput](d2dgetinput.md)y que se deben definir las directivas de preprocesador antes de que se incluya el archivo auxiliar.

Un sombreador compatible con vinculación debe proporcionar un sombreador de píxeles de paso único normal y una función de sombreador de exportación. La \_ macro D2D PS \_ entry permite que cada una de ellas se genere a partir del mismo código, cuando se usa junto con el script de compilación del sombreador.

Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos de D2D.

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

Al compilar una versión de función de exportación del mismo código, se genera el código siguiente:

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

Tenga en cuenta que la entrada de textura, que normalmente se recupera mediante el muestreo de un Texture2D, se ha reemplazado por una entrada de función input0.

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

 

 





