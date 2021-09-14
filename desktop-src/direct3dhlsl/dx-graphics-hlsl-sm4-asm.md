---
title: Ensamblado del modelo de sombreador 4
description: Ensamblado del modelo de sombreador 4
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974722"
---
# <a name="shader-model-4-assembly"></a>Ensamblado del modelo de sombreador 4

El modelo de sombreador 4 requiere que programe sombreadores en HLSL. Sin embargo, el compilador del sombreador compila el código HLSL en un ensamblado que se ejecuta en el dispositivo. Si usa LAV para Windows para depurar los sombreadores, puede optar por mostrar el código del sombreador en HLSL o ensamblado. En esta sección se enumeran las instrucciones de ensamblado Shader Model 4 y Shader Model 4.1 que puede encontrar al depurar un sombreador.

<dl>

[Modificadores de instrucción](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continue](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[Cortar](cut--sm4---asm-.md)  
[dcl \_ constantBuffer](dcl-constantbuffer.md)  
[dcl \_ globalFlags](dcl-globalflags.md)  
[dcl \_ immediateConstantBuffer](dcl-immediateconstantbuffer.md)  
[dcl \_ indexableTemp](dcl-indexabletemp.md)  
[dcl \_ indexRange](dcl-indexrange.md)  
[dcl \_ input](dcl-input.md)  
[dcl \_ input \_ sv](dcl-input-sv.md)  
[dcl \_ input vPrim](dcl-input-vprim.md)  
[dcl \_ maxOutputVertexCount](dcl-maxoutputvertexcount.md)  
[Salida \_ de dcl](dcl-output.md)  
[dcl \_ output \_ oDepth](dcl-output-odepth.md)  
[dcl \_ output \_ sgv](dcl-output-sgv.md)  
[siv \_ de salida de \_ dcl](dcl-output-siv.md)  
[dcl \_ outputTopology](dcl-outputtopology.md)  
[dcl \_ resource](dcl-resource.md)  
[dcl \_ sampler](dcl-sampler.md)  
[dcl \_ temps](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[deriv \_ rtx](deriv-rtx--sm4---asm-.md)  
[deriv \_ rty](deriv-rty--sm4---asm-.md)  
[Deseche](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[Emitir](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[endloop](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[Frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[iadd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[Ige](ige--sm4---asm-.md)  
[Ilt](ilt--sm4---asm-.md)  
[Imad](imad--sm4---asm-.md)  
[Imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[Ine](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[Ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[ld](ld--sm4---asm-.md)  
[Registro](log--sm4---asm-.md)  
[Bucle](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[Enojado](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[Mov](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[Nop](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[resinfo](resinfo--sm4---asm-.md)  
[Ret](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[round \_ ne](round-ne--sm4---asm-.md)  
[round \_ ni](round-ni--sm4---asm-.md)  
[round \_ pi](round-pi--sm4---asm-.md)  
[round \_ z](round-z--sm4---asm-.md)  
[Lrq](rsq--sm4---asm-.md)  
[Muestra](sample--sm4---asm-.md)  
[ejemplo \_ b](sample-b--sm4---asm-.md)  
[ejemplo \_ c](sample-c--sm4---asm-.md)  
[ejemplo \_ de c \_ lz](sample-c-lz--sm4---asm-.md)  
[ejemplo \_ d](sample-d--sm4---asm-.md)  
[ejemplo \_ l](sample-l--sm4---asm-.md)  
[sincos](sincos--sm4---asm-.md)  
[Sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[udiv](udiv--sm4---asm-.md)  
[Uge](uge--sm4---asm-.md)  
[Ult](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[Umax](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[Xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Ensamblado del modelo de sombreador 4.1

El modelo de sombreador 4.1 admite todas las instrucciones del modelo de sombreador 4.0 y las siguientes instrucciones adicionales:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[Lod](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de sombreador de Asm](dx9-graphics-reference-asm.md)
</dt> <dt>

[Shader Model 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




