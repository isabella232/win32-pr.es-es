---
title: min (sm4 - asm)
description: Mínimo flotante por componente.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8791589b77edc66eeab4b48f10f4a9b16b5cb2d9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993902"
---
# <a name="min-sm4---asm"></a>min (sm4 - asm)

Mínimo flotante por componente.



| min \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swzzle \] , \[ - \] src1 abs \[ \_ \] \[ .sw swle \] , |
|---------------------------------------------------------------------------------------------|



 



| Elemento                                                            | Descripción                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[en \] El resultado de la operación.<br/> *dest*  =  *src0*  <  *src1* ? *src0:* *src1*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[en \] Los componentes que se comparan con *src1*.<br/>                                                  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[en \] Los componentes que se comparan con *src0*.<br/>                                                  |



 

## <a name="remarks"></a>Comentarios

>= se usa en lugar > para que si min(x,y) = x, max(x,y) = y.

NaN tiene un control especial. Si un operando de origen es NaN, se devuelve el otro operando de origen y la elección se realiza por componente. Si ambos son NaN, se devuelve cualquier representación de NaN. Esto se ajusta a las nuevas reglas IEEE 754R.

Los desnormas se vacían, con el signo conservado, antes de la comparación. Sin embargo, el resultado escrito *en dest* puede o no vaciarse desnormado.

En la tabla siguiente se muestran los resultados obtenidos al ejecutar la instrucción con varias clases de números, suponiendo que no se produzcan desbordamientos ni subdesbordes. F significa número real finito.



| **src0 src1->** | **-inf** | **F**        | **+inf** | **NaN** |
|--------------------|----------|--------------|----------|---------|
| **-inf**           | -inf     | -inf         | -inf     | -inf    |
| **F**              | -inf     | src0 o src1 | src0     | src0    |
| **-inf**           | -inf     | src1         | +inf     | +inf    |
| **NaN**            | -inf     | src1         | +inf     | NaN     |



 

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

 

 





