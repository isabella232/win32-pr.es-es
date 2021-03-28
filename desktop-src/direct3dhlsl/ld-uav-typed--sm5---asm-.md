---
title: ld_uav_typed (SM5-ASM)
description: Lectura de acceso aleatorio de un elemento a partir de una vista de acceso desordenado con tipo (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358487"
---
# <a name="ld_uav_typed-sm5---asm"></a>LD \_ UAV \_ con tipo (SM5-ASM)

Lectura de acceso aleatorio de un elemento a partir de una vista de acceso desordenado con tipo (UAV).



| LD \_ UAV \_ con tipo dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . swizzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[en \] la dirección de los resultados de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[en \] especifica la dirección de la que se va a leer.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[en \] el origen del que se va a leer. <br/>                    |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una lectura de un elemento de 4 componentes de *srcUAV* en la dirección de entero sin signo de *srcAddress*, convertido a 32 bits por componente basado en el formato y, a continuación, se escribe en *dst0* en el sombreador.

*srcUAV* es un UAV (u \# ) declarado como con tipo. Sin embargo, el tipo de recurso enlazado debe ser R32 \_ uint/Sint/float.

El número de componentes enteros sin signo de 32 bits tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *srcUAV*. El direccionamiento es el mismo que el de la instrucción [LD](ld--sm4---asm-.md) .

El direccionamiento fuera de los límites es igual que la instrucción **LD** .

El comportamiento de esta instrucción es idéntico a la instrucción **LD** si se llama como **LD dst0 \[ . Mask \] , srcAddress \[ . swizzle \] , srcUAV \[ . \] swizzle**

No es válido y no está definido para usar esta instrucción en un UAV que no se declara como con tipo. Hacer esto en un UAV estructurado o sin tipo no es válido.

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



 

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción para UAV, SRV y TGSM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblador modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





