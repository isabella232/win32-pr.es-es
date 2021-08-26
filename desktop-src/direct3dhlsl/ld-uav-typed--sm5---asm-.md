---
title: ld_uav_typed (sm5 - asm)
description: Lectura de acceso aleatorio de un elemento desde una vista de acceso no ordenado (UAV) con tipo.
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9685341f4a3a2e6b22bbbcc4b36f6ecccc153f17c67f38c390e6beeef94358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982075"
---
# <a name="ld_uav_typed-sm5---asm"></a>ld \_ uav \_ con tipo (sm5 - asm)

Lectura de acceso aleatorio de un elemento desde una vista de acceso no ordenado (UAV) con tipo.



| ld \_ uav \_ typed dst0 \[ .mask \] , srcAddress \[ .swzzle \] , srcUAV \[ .swzzle\] |
|--------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[en \] La dirección de los resultados de la operación.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[en \] Especifica la dirección de la que se leerá.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[en \] El origen del que se leerá. <br/>                    |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza una lectura de un elemento de 4 componentes de *srcUAV* en la dirección de entero sin signo en *srcAddress*, convertida a 32 bits por componente según el formato y, a continuación, se escribe en *dst0* en el sombreador.

*srcUAV* es un UAV \# (u) declarado como con tipo. Sin embargo, el tipo del recurso enlazado debe ser R32 \_ UINT/SINT/FLOAT.

El número de componentes enteros de 32 bits sin signo tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *srcUAV.* El direccionamiento es el mismo que el de [la instrucción ld.](ld--sm4---asm-.md)

El direccionamiento fuera de los límites es el mismo que la **instrucción ld.**

El comportamiento de esta instrucción es idéntico a la instrucción **ld** si se llama a **como ld dst0 \[ .mask , \] srcAddress \[ .swzzle \] , srcUAV \[ .swzzle \]**

No es válido y no está definido usar esta instrucción en un UAV que no se declara como con tipo. Hacer esto en un UAV estructurado o sin tipo no es válido.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | Sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

cs \_ 4 \_ 0 y cs 4 1 admiten esta instrucción para \_ \_ UAV, SRV y TGSM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





