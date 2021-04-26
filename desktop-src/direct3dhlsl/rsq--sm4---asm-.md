---
title: rsq (sm4 - asm)
description: Raíz cuadrada mutua por componente.
ms.assetid: CDA3C2DF-2793-4CE3-87CE-4E0AA945A1BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1528e9f187ff7d4fb6074d42a1c574686f3b22f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998172"
---
# <a name="rsq-sm4---asm"></a>rsq (sm4 - asm)

Raíz cuadrada mutua por componente.



| rsq \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                      |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] Contiene los resultados de la operación.<br/> *dest* = 1.0f / sqrt(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes de la operación.<br/>                                              |



 

## <a name="remarks"></a>Comentarios

El error relativo máximo es 2-21.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.

F significa número finito-real.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | NaN      | NaN    | -inf        | -inf   | +inf   | +inf        | +F     | +0       | NaN     |



 

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
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





