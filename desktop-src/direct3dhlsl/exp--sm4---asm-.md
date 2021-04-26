---
title: exp (sm4 - asm)
description: 2exponent por componente.
ms.assetid: 12EB865A-BF71-4B4B-854F-9DA056B18AE0
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b24c74394a5e8ac7a6c945e2c9b63e6f242daa1
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999082"
---
# <a name="exp-sm4---asm"></a>exp (sm4 - asm)

2exponent por componente.



| exp \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle\] |
|------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/> *dest* = 2 *src0*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] El exponente.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

Esta instrucción sigue la teoría del límite. El error relativo máximo es 2-21.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzca ningún desbordamiento o subdesbordmiento. En esta tabla, F significa número finito-real.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | 0        | +F     | 1           | 1      | 1      | 1           | +F     | +inf     | NaN     |



 

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

[Ensamblado del modelo 4 del sombreador (HLSL de DirectX)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





