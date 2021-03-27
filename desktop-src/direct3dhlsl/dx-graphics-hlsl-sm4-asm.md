---
title: Ensamblado del modelo 4 del sombreador
description: Ensamblado del modelo 4 del sombreador
ms.assetid: 2896e195-b48b-4ce9-9421-f5fa40674b5e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 20c7ff5d2a171228223d52db28d3bae6007068c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075759"
---
# <a name="shader-model-4-assembly"></a>Ensamblado del modelo 4 del sombreador

El modelo de sombreador 4 requiere la aplicación de sombreadores en HLSL. Sin embargo, el compilador del sombreador compila el código HLSL en el ensamblado que se ejecuta en el dispositivo. Si usa PIX para Windows para depurar los sombreadores, puede elegir mostrar el código del sombreador en HLSL o en el ensamblado. En esta sección se enumeran las instrucciones de ensamblado del modelo de sombreador 4 y 4,1 del modelo de sombreador que puede encontrarse al depurar un sombreador.

<dl>

[Modificadores de instrucciones](instruction-modifiers.md)  
[add](add--sm4---asm-.md)  
[and](and--sm4---asm-.md)  
[break](break--sm4---asm-.md)  
[breakc](breakc--sm4---asm-.md)  
[call](call--sm4---asm-.md)  
[callc](callc--sm4---asm-.md)  
[case](case--sm4---asm-.md)  
[continue](continue--sm4---asm-.md)  
[continuec](continuec--sm4---asm-.md)  
[límite](cut--sm4---asm-.md)  
[constantBuffer de DCL \_](dcl-constantbuffer.md)  
[DCL \_ indicadores_globales](dcl-globalflags.md)  
[immediateConstantBuffer de DCL \_](dcl-immediateconstantbuffer.md)  
[indexableTemp de DCL \_](dcl-indexabletemp.md)  
[indexRange de DCL \_](dcl-indexrange.md)  
[entrada de DCL \_](dcl-input.md)  
[\_SV de entrada de DCL \_](dcl-input-sv.md)  
[vPrim de entrada de DCL \_](dcl-input-vprim.md)  
[maxOutputVertexCount de DCL \_](dcl-maxoutputvertexcount.md)  
[salida de DCL \_](dcl-output.md)  
[\_oDepth de salida de DCL \_](dcl-output-odepth.md)  
[\_SGV de salida de DCL \_](dcl-output-sgv.md)  
[\_SIV de salida de DCL \_](dcl-output-siv.md)  
[outputTopology de DCL \_](dcl-outputtopology.md)  
[\_recurso DCL](dcl-resource.md)  
[muestra de DCL \_](dcl-sampler.md)  
[Temps de DCL \_](dcl-temps.md)  
[default](default--sm4---asm-.md)  
[derivar \_ RTX](deriv-rtx--sm4---asm-.md)  
[derivar \_ propiedad](deriv-rty--sm4---asm-.md)  
[omiti](discard--sm4---asm-.md)  
[div](div--sm4---asm-.md)  
[dp2](dp2--sm4---asm-.md)  
[dp3](dp3--sm4---asm-.md)  
[dp4](dp4--sm4---asm-.md)  
[else](else--sm4---asm-.md)  
[reflexión](emit--sm4---asm-.md)  
[emitThenCut](emitthencut--sm4---asm-.md)  
[endif](endif--sm4---asm-.md)  
[ENDLOOP](endloop--sm4---asm-.md)  
[endswitch](endswitch--sm4---asm-.md)  
[eq](eq--sm4---asm-.md)  
[exp](exp--sm4---asm-.md)  
[frc](frc--sm4---asm-.md)  
[ftoi](ftoi--sm4---asm-.md)  
[ftou](ftou--sm4---asm-.md)  
[ge](ge--sm4---asm-.md)  
[iadd](iadd--sm4---asm-.md)  
[ibfe](dne--sm5---asm-.md)  
[ieq](ieq--sm4---asm-.md)  
[if](if--sm4---asm-.md)  
[ige](ige--sm4---asm-.md)  
[ILT](ilt--sm4---asm-.md)  
[imad](imad--sm4---asm-.md)  
[imin](imin--sm4---asm-.md)  
[imul](imul--sm4---asm-.md)  
[Nea](ine--sm4---asm-.md)  
[ineg](ineg--sm4---asm-.md)  
[ishl](ishl--sm4---asm-.md)  
[ishr](ishr--sm4---asm-.md)  
[itof](itof--sm4---asm-.md)  
[label](label--sm4---asm-.md)  
[!](ld--sm4---asm-.md)  
[inicia](log--sm4---asm-.md)  
[bucle](loop--sm4---asm-.md)  
[lt](lt--sm4---asm-.md)  
[Mad](mad--sm4---asm-.md)  
[max](max--sm4---asm-.md)  
[min](min--sm4---asm-.md)  
[MOV](mov--sm4---asm-.md)  
[movc](movc--sm4---asm-.md)  
[mul](mul--sm4---asm-.md)  
[ne](ne--sm4---asm-.md)  
[instrucción](nop--sm4---asm-.md)  
[not](not--sm4---asm-.md)  
[or](or--sm4---asm-.md)  
[resinfo](resinfo--sm4---asm-.md)  
[direcc](ret--sm4---asm-.md)  
[retc](retc--sm4---asm-.md)  
[Round \_ ne](round-ne--sm4---asm-.md)  
[no redondeo \_ ni](round-ni--sm4---asm-.md)  
[redondear \_ PI](round-pi--sm4---asm-.md)  
[Round \_ z](round-z--sm4---asm-.md)  
[rsq](rsq--sm4---asm-.md)  
[AdventureWorks](sample--sm4---asm-.md)  
[ejemplo \_ b](sample-b--sm4---asm-.md)  
[ejemplo \_ c](sample-c--sm4---asm-.md)  
[ejemplo de \_ c \_ LZ](sample-c-lz--sm4---asm-.md)  
[ejemplo \_ d](sample-d--sm4---asm-.md)  
[ejemplo \_ l](sample-l--sm4---asm-.md)  
[sincos (](sincos--sm4---asm-.md)  
[sqrt](sqrt--sm4---asm-.md)  
[switch](switch--sm4---asm-.md)  
[UDIV](udiv--sm4---asm-.md)  
[uge](uge--sm4---asm-.md)  
[ULT](ult--sm4---asm-.md)  
[umad](umad--sm4---asm-.md)  
[escáner](umax--sm4---asm-.md)  
[umin](umin--sm4---asm-.md)  
[umul](umul--sm4---asm-.md)  
[ushr](ushr--sm4---asm-.md)  
[utof](utof--sm4---asm-.md)  
[xor](xor--sm4---asm-.md)  
</dl>

## <a name="shader-model-41-assembly"></a>Ensamblado modelo de sombreador 4,1

El modelo de sombreador 4,1 es compatible con todas las instrucciones del modelo de sombreador 4,0 y las siguientes instrucciones adicionales:

<dl>

[gather4](gather4--sm4-1---asm-.md)  
[ld2dms](ld2dms--sm4-1---asm-.md)  
[LOD](lod--sm4-1---asm-.md)  
[sampleinfo](sampleinfo--sm4-1---asm-.md)  
[samplepos](samplepos--sm4-1---asm-.md)  
</dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del sombreador de ASM](dx9-graphics-reference-asm.md)
</dt> <dt>

[Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




