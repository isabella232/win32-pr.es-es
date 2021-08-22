---
title: store_uav_typed (sm5 - asm)
description: Escritura de acceso aleatorio de un elemento en una vista de acceso sin ordenar (UAV) con tipo.
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc190662ebab4629c92bba8fafbe75fe23704f8543c7eb9ceba53b9ab02b1029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508245"
---
# <a name="store_uav_typed-sm5---asm"></a>store \_ uav \_ con tipo (sm5 - asm)

Escritura de acceso aleatorio de un elemento en una vista de acceso sin ordenar (UAV) con tipo.



| store \_ uav \_ typed dstUAV.xyzw, dstAddress \[ .swzzle \] , src0 \[ .swzzle\] |
|-------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[en \] Contiene el resultado de la operación.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] La dirección en la que se va a escribir.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] Componentes que se escribirán.<br/>              |



 

## <a name="remarks"></a>Comentarios

Esta instrucción realiza un elemento de 4 componentes de 32 bits escrito de \* *src0* a *dstUAV* en la dirección *de dstAddress*. *dstUAV* es un UAV con tipo (u \# ).

El formato del UAV determina la conversión de formato.

El número de componentes enteros de 32 bits sin signo tomados de la dirección viene determinado por la dimensionalidad del recurso declarado en *dstUAV.* Esta dirección está en elementos .

El direccionamiento fuera de límites significa que no se escribe nada en la memoria.

*dstUAV siempre* tiene una máscara de escritura .xyzw. Se deben escribir todos los componentes.

No es válido y no está definido usar esta instrucción en un UAV que no se declara como con tipo. Es decir, hacer esto en un UAV estructurado o sin tipo no es válido.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





