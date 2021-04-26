---
title: sincos (sm4 - asm)
description: Sin(theta) por componente y cos(theta) para theta en radianes.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997022"
---
# <a name="sincos-sm4---asm"></a>sincos (sm4 - asm)

Sin(theta) por componente y cos(theta) para theta en radianes.



| sincos \[ \_ sat \] destSIN \[ .mask \] , destCOS \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|------------------------------------------------------------------------------------|



 



| Elemento                                                                                               | Descripción                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[en \] La dirección de sin(*src0*), calculada por componente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[en \] La dirección de cos(*src0*), calculada por componente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[en \] Los componentes para los que se va a calcular sin y cos.<br/>    |



 

## <a name="remarks"></a>Comentarios

Si el resultado no es necesario, puede especificar *destSIN* y *destCOS* como NULL en lugar de especificar un registro.

Los valores de Theta pueden ser cualquier valor de punto flotante ieee de 32 bits.

El error absoluto máximo es 0,0008 en el intervalo de -100 \* Pi a +100 \* Pi.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números.

F significa número finito-real.



| **src**     | **-inf** | **-F**       | **-denorm** | **-0** | **+0** | **+denorm** | **+F**       | **+inf** | **NaN** |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **destSIN** | NaN      | \[-1 a +1\] | -0          | -0     | +0     | +0          | \[-1 a +1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[-1 a +1\] | +1          | +1     | +1     | +1          | \[-1 a +1\] | NaN      | NaN     |



 

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

 

 





