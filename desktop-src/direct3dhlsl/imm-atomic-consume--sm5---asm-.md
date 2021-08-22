---
title: imm_atomic_consume (sm5 - asm)
description: Decremento atómico del contador oculto de 32 bits almacenado con una vista de acceso sin ordenar (UAV) Count o Append, que devuelve el nuevo valor.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0244b885d9d2c46b734994d5e101f79147839d0cf76e2bab5669e52700cf59e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119319"
---
# <a name="imm_atomic_consume-sm5---asm"></a>Consumo \_ atómico de imm \_ (sm5 - asm)

Decremento atómico del contador oculto de 32 bits almacenado con una vista de acceso sin ordenar (UAV) Count o Append, que devuelve el nuevo valor.



| imm \_ atomic \_ consume dst0 \[ .single component mask , \_ \_ \] dstUAV |
|---------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[en \] Contiene el valor de contador original devuelto.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] un UAV de búfer estructurado con la marca Recuento o Anexar. <br/> |



 

## <a name="remarks"></a>Comentarios

Vea [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) para obtener una explicación sobre la validez del valor de recuento devuelto en función de si el UAV es Count o Append. Lo mismo se aplica a **imm \_ atomic \_ consume**.

**El consumo \_ \_ atómico** de imm realiza un decremento atómico del valor del contador y devuelve el nuevo valor *a dst0.*

No hay ninguna fijación del recuento, por lo que se ajusta en subdesbordado.

El mismo sombreador no puede intentar tanto el consumo **\_ \_ atómico de imm como** el consumo **\_ \_ atómico** de imm en el mismo UAV. Además, la GPU no puede permitir que varias invocaciones de sombreador mezclen **imm \_ atomic \_ alloc** y **imm \_ atomic \_ consumen** en el mismo UAV.

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



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





