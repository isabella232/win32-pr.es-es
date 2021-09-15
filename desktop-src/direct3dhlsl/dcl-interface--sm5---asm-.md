---
title: dcl_interface (sm5 - asm)
description: Declare punteros de tabla de función (interfaces). | dcl_interface (sm5 - asm)
ms.assetid: 5A4D911E-7117-409B-8FDC-9CEC2C185C15
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61435e06d0d5b88bb82ca91f758646d7911d3bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573920"
---
# <a name="dcl_interface-sm5---asm"></a>Interfaz dcl \_ (sm5 - asm)

Declare punteros de tabla de función (interfaces).



| dcl \_ interface fp \# \[ arraySize \] \[ numCallSites \] = {ft , ft , \# \# ...} |
|----------------------------------------------------------------------|



 



| Elemento                                                          | Descripción                                    |
|---------------------------------------------------------------|------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*Fp\#*<br/> | \[en \] Los punteros de la tabla de funciones.<br/> |



 

## <a name="remarks"></a>Observaciones

Cada interfaz debe enlazarse desde la API antes de que se pueda usar el sombreador. El enlace proporciona una referencia a una de las tablas de función para que se puedan rellenar las ranuras de método. El compilador no generará punteros para objetos sin referencia.

Un puntero de tabla de función tiene un conjunto completo de ranuras de método para evitar el nivel adicional de direccionamiento indirecto que requeriría una representación de puntero a vtable de C++. Esto también requeriría que estos punteros sean de 5 tuplas. En el modelo de inlineación virtual HLSL, siempre se sabe qué variable o entrada global se usa para una llamada, por lo que podemos configurar tablas por objeto raíz.

Las declaraciones de puntero de función indican qué tablas de funciones son legales para usarlas con ellas. Esto también permite la derivación de información de correlación de métodos.

La primera \[ \] de una declaración de interfaz es el tamaño de la matriz. Si se usa la indexación dinámica, la declaración lo indicará como se muestra. Una matriz de punteros de interfaz también se puede indexar estáticamente, no es necesario que las matrices de punteros de interfaz se refieren a la indexación dinámica.

La numeración de punteros de interfaz comienza en 0 para la primera declaración y, posteriormente, tiene en cuenta el tamaño de la matriz, por lo que el primer puntero después de una matriz de cuatro entradas fp0 \[ \] \[ 4 1 sería \] \[ \] \[ \] fp4.

La segunda de una declaración de interfaz es el número de sitios de llamada, que deben coincidir con el número de cuerpos de cada tabla a la que se hace \[ \] referencia en la declaración.

No hay límites en el número de opciones de tabla de función \# (ft) que se pueden enumerar en una declaración de interfaz.

Una tabla de función determinada (ft \# ) puede aparecer más de una vez en una o varias declaraciones de interfaz.

### <a name="restrictions"></a>Restricciones

-   El número de sitios de objeto de un sombreador, que es la suma en todas las declaraciones *fp \#* de sus declaraciones arraySize, no debe ser superior a \[ \] 253. Este número corresponde al número de **punteros** que pueden estar presentes. El tiempo de ejecución aplica este límite 253 para mantener un límite en el tamaño del DDI para comunicar estos datos de puntero.
-   El número de sitios de llamada de un sombreador, que es la suma en todas las instrucciones fcall del número de posibles destinos de rama, no debe ser superior a 4096.

    Por ejemplo, una [llamada fcall](fcall--sm5---asm-.md) que usa un índice estático para la primera *dimensión fp \[ \] \[ \]* cuenta como uno:

    `                       fcall fp0[0][0]         // +1`

    Una **llamada fcall** que usa un índice dinámico cuenta como el número de elementos de la matriz (primero \[ \] de la interfaz **dcl \_**):

    `                    dcl_interface_dynamicindexed fp1[2][1] = {ft2, ft3, ft4}                      ...                     `

    `fcall fp1[r0.z + 0][1]  // +2`

    Este límite ayuda a algunas implementaciones a ajustar fácilmente las tablas de las selecciones del cuerpo de la función en el almacenamiento constante de tipo búfer.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción para UAV y SRV.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





