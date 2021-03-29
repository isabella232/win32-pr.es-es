---
title: dcl_interface (SM5-ASM)
description: Declare punteros de tabla de función (interfaces). | dcl_interface (SM5-ASM)
ms.assetid: 5A4D911E-7117-409B-8FDC-9CEC2C185C15
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61435e06d0d5b88bb82ca91f758646d7911d3bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998084"
---
# <a name="dcl_interface-sm5---asm"></a>\_interfaz DCL (SM5-ASM)

Declare punteros de tabla de función (interfaces).



| DCL \_ interface FP \# \[ tamaño \] \[ numCallSites \] = {ft \# , ft \# ,...} |
|----------------------------------------------------------------------|



 



| Elemento                                                          | Descripción                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/> | \[en \] los punteros de la tabla de función.<br/> |



 

## <a name="remarks"></a>Observaciones

Cada interfaz debe estar enlazada desde la API antes de que se pueda usar el sombreador. El enlace proporciona una referencia a una de las tablas de funciones para que se puedan rellenar las ranuras de método. El compilador no generará punteros para objetos sin referencia.

Un puntero de tabla de función tiene un conjunto completo de ranuras de método para evitar el nivel de direccionamiento indirecto adicional que requeriría una representación de puntero a puntero a vtable de C++. Esto también requeriría que estos punteros sean 5-tuplas. En el modelo de inserción virtual de HLSL, siempre se sabe qué variable global/entrada se usa para una llamada, de modo que podamos configurar tablas por objeto raíz.

Las declaraciones de puntero de función indican qué tablas de función son válidas para su uso con ellas. Esto también permite la derivación de información de correlación de métodos.

La primera \[ \] de una declaración de interfaz es el tamaño de la matriz. Si se utiliza la indexación dinámica, la declaración indicará que, como se muestra. Una matriz de punteros de interfaz se puede indizar de forma estática; no es necesario que las matrices de punteros de interfaz signifiquen una indexación dinámica.

La numeración de punteros de interfaz comienza en 0 para la primera declaración y, posteriormente, tiene en cuenta el tamaño de la matriz, por lo que el primer puntero después de una matriz de cuatro entradas FP0 \[ 4 \] \[ 1 \] sería FP4 \[ \] \[ \] .

La segunda \[ \] de una declaración de interfaz es el número de sitios de llamada, que debe coincidir con el número de cuerpos de cada tabla a la que se hace referencia en la declaración.

No hay límites en el número de opciones de la tabla de funciones (ft \# ) que se pueden enumerar en una declaración de interfaz.

Una tabla de función determinada (ft \# ) puede aparecer más de una vez en una o varias declaraciones de interfaz.

### <a name="restrictions"></a>Restricciones

-   El número de sitios de objetos en un sombreador, que es la suma de todas las declaraciones *FP \#* de sus \[ \] declaraciones tamaño, no debe ser superior a 253. Este número corresponde **a cuántos punteros** pueden estar presentes. El tiempo de ejecución aplica este límite de 253 para mantener un límite en el tamaño de DDI para comunicar estos datos de puntero.
-   El número de sitios de llamada en un sombreador, que es la suma de todas las instrucciones fcall del número de posibles destinos de rama, no debe ser superior a 4096.

    Por ejemplo, un [fcall](fcall--sm5---asm-.md) que utiliza un índice estático para la primera *dimensión \[ \] \[ \] FP* cuenta como uno:

    `                       fcall fp0[0][0]         // +1`

    Un **fcall** que utiliza un índice dinámico cuenta como el número de elementos de la matriz (primero \[ \] de **la \_ interfaz DCL**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Este límite ayuda a algunas implementaciones a ajustar fácilmente las tablas de las selecciones de cuerpo de función en el almacenamiento de tipo búfer de constantes.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Esta instrucción es compatible con los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





