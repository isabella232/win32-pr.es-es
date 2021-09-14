---
title: 'ftoi (sm4 - asm) '
description: Conversión de punto flotante a entero con signo.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361572"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 - asm) 

Conversión de punto flotante a entero con signo.

| ftoi dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swoile\] |
|-|

| Elemento | Descripción |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección del resultado de la operación.<br/> *dest*  =  [round \_ z](round-z--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El componente que se debe convertir.<br/> |

## <a name="remarks"></a>Observaciones

La conversión se realiza por componente. El redondeo siempre se realiza hacia cero, siguiendo la convención de C para las conversión de float a int. Las aplicaciones que requieren una semántica de redondeo diferente pueden invocar las **instrucciones de redondeo** antes de convertir en entero.

Las entradas se fijan en el \[ intervalo -2147483648.999f ... 2147483647.999f antes de la conversión y los valores NaN de entrada \] generan un resultado cero.

Los modificadores de valores absolutos y negate opcionales se aplican a los valores de origen antes de la conversión.

Esta instrucción se aplica a las siguientes fases del sombreador:

| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.

| Modelo de sombreador | Compatible |
|-|-|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) | sí |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md) | sí |
| [Shader Model 4](dx-graphics-hlsl-sm4.md) | sí |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No |

## <a name="related-topics"></a>Temas relacionados

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
