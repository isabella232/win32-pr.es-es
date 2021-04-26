---
title: mul (sm4 - asm)
description: Multiplicación por componentes.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a020666c3ce59cb368271aaf09f958d8a40af56c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998262"
---
# <a name="mul-sm4---asm"></a>mul (sm4 - asm)

Multiplicación por componentes.



| mul \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw swzzle\] |
|--------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                        |
|-----------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación. dest = src0 \* src1<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Multiplicando.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] El multiplicador.<br/>                                  |



 

## <a name="remarks"></a>Comentarios

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento.

F significa número finito-real.



| **src0 src1 ->** | **-inf** | **-F** | **-1.0** | **-denorm** | **-0** | **+0** | **desnorma** | **+1.0** | **+F** | **+inf** | **NaN** |
|---------------------|----------|--------|----------|-------------|--------|--------|------------|----------|--------|----------|---------|
| **-inf**            | +inf     | +inf   | +inf     | NaN         | NaN    | NaN    | NaN        | -inf     | -inf   | -inf     | NaN     |
| **-F**              | +inf     | +F     | -src0    | +0          | +0     | -0     | -0         | src0     | -F     | -inf     | NaN     |
| **-1**              | +inf     | -src1  | +1.0     | +0          | +0     | -0     | -0         | -1.0     | -src1  | -inf     | NaN     |
| **-denorm**         | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **-0**              | NaN      | +0     | +0       | +0          | +0     | -0     | -0         | -0       | -0     | NaN      | NaN     |
| **+0**              | Inan     | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+denorm**         | NaN      | -0     | -0       | -0          | -0     | +0     | +0         | +0       | +0     | NaN      | NaN     |
| **+1.0**            | -inf     | src1   | -1.0     | -0          | -0     | +0     | +0         | +1.0     | src1   | +inf     | NaN     |
| **+F**              | -inf     | -F     | -src0    | -0          | -0     | +0     | +0         | src0     | +F     | +inf     | NaN     |
| **+inf**            | -inf     | -inf   | -inf     | NaN         | NaN    | NaN    | NaN        | +inf     | +inf   | +inf     | NaN     |
| **NaN**             | NaN      | NaN    | NaN      | NaN         | NaN    | NaN    | NaN        | NaN      | NaN    | NaN      | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 4 (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





