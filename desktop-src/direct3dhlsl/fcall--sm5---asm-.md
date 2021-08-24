---
title: fcall (sm5 - asm)
description: Llamada a la función de interfaz.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7781fc0a2fc7bbd715084d3c0e9682a433ddf16e4492724df8fdb2e31c84689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854515"
---
# <a name="fcall-sm5---asm"></a>fcall (sm5 - asm)

Llamada a la función de interfaz.



| fcall fp \# \[ arrayIndex \] \[ callSite\] |
|--------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/>                                                  | \[en \] el puntero de función.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*<br/> | \[en \] Opcional. Especifica un desplazamiento en la matriz del puntero de función. Este parámetro debe ser un entero literal sin signo si fp \# no se declaró como indexable. De lo contrario, arrayIndex puede tener el formato literal base + desplazamiento de un registro de sombreador. Por ejemplo, fcall fp1 \[ r1.w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*callSite*<br/>     | \[en \] Opcional. Desplazamiento de entero literal sin signo en la tabla de funciones seleccionada, seleccionando un fb cuerpo de función \# para ejecutar. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Comentarios

*fp \#* \[  \] \[ arrayIndex \] se resuelve en una tabla de funciones determinada, seleccionada desde la API fuera del sombreador de las opciones de tabla de funciones enumeradas en la declaración de *fp \#*.

La suma de \# en *fp \#* y *arrayIndex* selecciona la tabla de funciones. Por ejemplo, si una interfaz se declara como fp4 4 3 (tamaño de matriz de 4), las siguientes fcall s son \[ \] \[ equivalentes: \] fcall fp4  \[ 2 \] \[ 3 \] y fp5 1 3 , porque \[ \] \[ \] 4+2 = 5+1.

### <a name="restrictions"></a>Restricciones

-   Si *arrayIndex usa* la indexación dinámica, el comportamiento no está definido si *arrayIndex* diverge en las invocaciones de sombreador adyacentes, lo que podría estar ejecutándose en lockstep. El compilador HLSL intentará no permitir este caso.

    Las invocaciones adyacentes pueden estar inactivas debido al control de flujo, ya que no interrumpirá la ejecución del paso de bloqueo.

-   Si *\# fp*  +  *arrayIndex* especifica un índice fuera de límites, el comportamiento no está definido.
-   Para los casos no definidos descritos aquí, significa que el comportamiento del dispositivo D3D actual se convierte en indefinido, incluida la posibilidad de que se pierda el dispositivo. Sin embargo, no se accederá a ninguna memoria fuera del dispositivo D3D actual o se ejecutará como código.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





