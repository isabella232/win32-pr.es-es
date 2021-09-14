---
title: ftou (sm4 - asm)
description: Conversión de punto flotante a entero sin signo.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361571"
---
# <a name="ftou-sm4---asm"></a>ftou (sm4 - asm)

Conversión de punto flotante a entero sin signo.



| ftou dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|----------------------------------------------------|



 



| ftoi dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swoile\] |
|----------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El valor que se debe convertir.<br/>                        |



 

## <a name="remarks"></a>Observaciones

La conversión se realiza por componente. El redondeo siempre se realiza hacia cero, siguiendo la convención de C para las conversión de float a int.

Las aplicaciones que requieren una semántica de redondeo diferente pueden invocar las **instrucciones de redondeo** antes de convertir en entero.

Las entradas se fijan en el intervalo \[ 0,0f ... 4294967295.999f antes de la conversión y los valores NaN de entrada \] generan un resultado cero.

Los modificadores de valores absolutos y negate opcionales se aplican a los valores de origen antes de la conversión.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





