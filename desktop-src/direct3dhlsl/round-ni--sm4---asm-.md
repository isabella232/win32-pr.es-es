---
title: round_ni (sm4 - asm)
description: Punto flotante redondeado a float entero. | round_ni (sm4 - asm)
ms.assetid: 6DEF818B-AFF9-4B44-950E-320EACE1CAC4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2487715bbb2596653b1ca985a2e0390457feecbf
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998582"
---
# <a name="round_ni-sm4---asm"></a>round \_ ni (sm4 - asm)

Punto flotante redondeado a float entero.



| round \_ ni \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de la operación.<br/>             |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza una ronda de punto flotante por componente de los valores de *src0,* escribiendo valores enteros de punto flotante *en dest*. **round \_ ni** se redondea hacia -infinity, comúnmente conocido como floor().

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.

F significa número finito-real.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Shader Model 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





