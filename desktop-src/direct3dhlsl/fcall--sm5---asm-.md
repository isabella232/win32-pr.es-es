---
title: fcall (SM5-ASM)
description: Llamada de función de interfaz.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c57ea40fec51cf4155b0932f6ce4a7b80d3180dd
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419979"
---
# <a name="fcall-sm5---asm"></a>fcall (SM5-ASM)

Llamada de función de interfaz.



| fcall FP \# \[ arrayIndex \] \[ llamada\] |
|--------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/>                                                  | \[en \] el puntero de función.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*<br/> | \[en \] opcional. Especifica un desplazamiento en la matriz de puntero de función. Este parámetro debe ser un entero sin signo literal si FP \# no se declaró como indexable. De lo contrario, arrayIndex puede tener el formato literal base + offset de un registro del sombreador. Por ejemplo, fcall FP1 \[ R1. w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*llamada*<br/>     | \[en \] opcional. Un desplazamiento de entero sin signo literal en la tabla de la función seleccionada, seleccionando el cuerpo de una función FB \# para ejecutarse. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Observaciones

*FP \#* \[  \] \[ arrayIndex \] se resuelve como una tabla de función determinada, seleccionada de la API fuera del sombreador de las opciones de la tabla de funciones enumeradas en la declaración de *FP \#*.

La suma de \# en *FP \#* y *arrayIndex* selecciona la tabla de funciones. Por ejemplo, si una interfaz se declara como FP4 \[ 4 \] \[ 3 \] (tamaño de matriz de 4), los siguientes **fcall** s son equivalentes: fcall FP4 \[ 2 \] \[ 3 \] y FP5 \[ 1 \] \[ 3 \] , porque 4 + 2 = 5 + 1.

### <a name="restrictions"></a>Restricciones

-   Si *arrayIndex* utiliza la indexación dinámica, el comportamiento es indefinido si *arrayIndex* difiere en las invocaciones de sombreador adyacentes, que podrían ejecutarse en lógico. El compilador de HLSL intentará no permitir este caso.

    Las invocaciones adyacentes pueden estar inactivas debido al control de flujo, ya que no interrumpe la ejecución de lógico.

-   Si *FP \#*  +  *arrayIndex* especifica un índice fuera del límite, el comportamiento es indefinido.
-   En el caso de los casos no definidos que se describen aquí, el comportamiento del dispositivo D3D actual queda indefinido, lo que incluye la posibilidad de que se pierda el dispositivo. Sin embargo, no se tendrá acceso a la memoria fuera del dispositivo D3D actual ni se ejecutará como código.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





