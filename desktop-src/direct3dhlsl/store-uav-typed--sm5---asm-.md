---
title: store_uav_typed (SM5-ASM)
description: Escritura de acceso aleatorio de un elemento en una vista de acceso desordenado con tipo (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077082"
---
# <a name="store_uav_typed-sm5---asm"></a>almacenar \_ UAV \_ con tipo (SM5-ASM)

Escritura de acceso aleatorio de un elemento en una vista de acceso desordenado con tipo (UAV).



| almacenar \_ UAV \_ con tipo dstUAV. Xyzw, dstAddress \[ . swizzle \] , src0 \[ . swizzle\] |
|-------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[en \] contiene el resultado de la operación.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] la dirección en la que se va a escribir.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] los componentes que se van a escribir.<br/>              |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza un \* elemento de 32 bits de 4 componentes escrito de *Src0* en *dstUAV* en la dirección de *dstAddress*. *dstUAV* es un UAV (u) con tipo \# .

El formato de UAV determina la conversión de formato.

El número de componentes enteros sin signo de 32 bits tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *dstUAV*. Esta dirección está en elementos.

El direccionamiento fuera del límite significa que no se escribe nada en la memoria.

*dstUAV* siempre tiene una máscara de escritura. xyzw. Se deben escribir todos los componentes.

No es válido y no está definido para usar esta instrucción en un UAV que no se declara como con tipo. Es decir, hacer esto en un UAV estructurado o sin tipo no es válido.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





