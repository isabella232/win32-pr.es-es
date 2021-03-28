---
title: sincos ((SM4-ASM)
description: Sin componentes (Theta) y cos (Theta) para Theta en radianes.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2dd8fc3b011758f071cdcd273e34eb8a7f6421f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996864"
---
# <a name="sincos-sm4---asm"></a>sincos ((SM4-ASM)

Sin componentes (Theta) y cos (Theta) para Theta en radianes.



| sincos ( \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------------------------------|



 



| Elemento                                                                                               | Descripción                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[en \] la dirección de sin (*src0*), se calcula por componente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[en \] la dirección de cos (*src0*), calculada por componente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[en \] los componentes para los que se van a calcular Sen y cos.<br/>    |



 

## <a name="remarks"></a>Observaciones

Si el resultado no es necesario, puede especificar *destSIN* y *destCOS* como null en lugar de especificar un registro.

Los valores de Theta pueden ser cualquier valor de punto flotante de IEEE 32 bits.

El error absoluto máximo es 0,0008 en el intervalo de-100 \* PI a + 100 \* PI.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.

F significa número finito-real.



|             |          |              |             |        |        |             |              |          |         |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **src**     | **-INF** | **-F**       | **-denormalización** | **-0** | **+0** | **+ denormalización** | **+ F**       | **+ INF** | **NaN** |
| **destSIN** | NaN      | \[de-1 a + 1\] | -0          | -0     | +0     | +0          | \[de-1 a + 1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[de-1 a + 1\] | +1          | +1     | +1     | +1          | \[de-1 a + 1\] | NaN      | NaN     |



 

Esta instrucción se aplica a las siguientes fases del sombreador:



| Sombreador de vértices | Sombreador de geometría | Sombreador de píxeles |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta función se admite en los siguientes modelos de sombreador.



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sí       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sí       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





