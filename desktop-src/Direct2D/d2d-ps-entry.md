---
title: D2D_PS_ENTRY función (D2d1effecthelpers.h)
description: Macro que define un punto de entrada de sombreador de píxeles con el nombre de función especificado.
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
ms.openlocfilehash: 26369ef5be8c9dea81bf95e60c09ca0041d4275114c8892b85b6b5525f45504b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087794"
---
# <a name="d2d_ps_entry-function"></a>Función D2D \_ PS \_ ENTRY

Macro que define un punto de entrada de sombreador de píxeles con el nombre de función especificado.

## <a name="syntax"></a>Sintaxis

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*Entryname* \[ En\]
</dt> <dd>

Nombre del punto de entrada del sombreador de píxeles.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Use esta macro en lugar de especificar la firma de entrada del punto de entrada de la manera normal: todos los parámetros están implícitos y se agregan mediante Direct2D durante la compilación en función del tipo de destino de compilación (sombreador completo o función de exportación).

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

En este breve ejemplo, tenga en cuenta que no se declara ningún parámetro de función, que el número de entradas y el tipo de cada entrada se declara antes de la función de entrada, que la entrada se recupera mediante una llamada a [D2DGetInput](d2dgetinput.md)y que las directivas de preprocesador deben definirse antes de incluir el archivo auxiliar.

Un sombreador compatible con la vinculación debe proporcionar un sombreador de píxeles de un solo paso normal y una función de sombreador de exportación. La macro D2D PS ENTRY permite generar cada uno de ellos a partir del mismo código, cuando se usa junto con el script de \_ \_ compilación del sombreador.

Al compilar un sombreador completo, las macros se expanden en el código siguiente, que tiene una firma de entrada compatible con efectos D2D.

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

Tenga en cuenta que la entrada de textura, recuperada normalmente mediante el muestreo de texture2D, se ha reemplazado por una entrada input0 de función.

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

 

 





