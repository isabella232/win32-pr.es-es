---
title: 'ftoi (sm4 - asm) '
description: Punto flotante a conversión de enteros con signo.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "104359485"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 - asm) 

Punto flotante a conversión de enteros con signo.

| ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|-|

| Elemento | Descripción |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[en \] la dirección del resultado de la operación.<br/> *dest*  =  [Round \_ z](round-z--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] el componente que se va a convertir.<br/> |

## <a name="remarks"></a>Observaciones

La conversión se realiza por componente. El redondeo siempre se realiza hacia cero, siguiendo la Convención de C para las conversiones de Float a int. Las aplicaciones que requieren una semántica de redondeo diferente pueden invocar las instrucciones **Round** antes de la conversión a un entero.

Las entradas se fijan en el intervalo \[ -2147483648.999 f... 2147483647.999 f \] antes de la conversión y los valores Nan de entrada producen un resultado cero.

Los modificadores de valor absoluto y de negación opcionales se aplican a los valores de origen antes de la conversión.

Esta instrucción se aplica a las siguientes fases del sombreador:

| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.

| Modelo de sombreador | Compatible |
|-|-|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) | sí |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md) | sí |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) | sí |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no |

## <a name="related-topics"></a>Temas relacionados

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
