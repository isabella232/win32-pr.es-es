---
title: imm_atomic_iadd (sm5 - asm)
description: Entero atómico inmediato que se agrega a la memoria. Devuelve el valor en memoria antes de la adición.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2695e23707fb61cd576748e2e83829cd7dc65259
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072706"
---
# <a name="imm_atomic_iadd-sm5---asm"></a>imm \_ atomic \_ iadd (sm5 - asm)

Entero atómico inmediato que se agrega a la memoria. Devuelve el valor en memoria antes de la adición.



| imm \_ atomic \_ iadd dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swzzle \] , src0 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Elemento                                                                                                           | Descripción                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[en \] Contiene el valor de *dst1 antes* de la escritura. <br/>                                                                           |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | Este valor debe ser una vista de acceso no ordenado (UAV) (u \# ). En el sombreador de proceso también puede ser memoria compartida de grupo de subprocesos (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[en \] la dirección naddress de memoria.<br/>                                                                                                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[en \] El valor que se agregará a *dst1.*<br/>                                                                                               |



 

## <a name="remarks"></a>Observaciones

Esta instrucción realiza una única adición de entero de 32 bits de componente de operando *src0* con *dst1* a 32 bits por dirección de componente *dstAddress*. No es importante firmar.

Si *dst1* es una u , es posible que se haya declarado como \# sin formato, con tipo o estructurado. Si se escribe, se debe declarar como UINT/SINT con el formato de recurso enlazado R32 \_ \_ UINT/SINT.

Si *dst1* es g \# , debe declararse como sin formato o estructurado.

El valor de *la memoria dst1* antes de la adición se devuelve *a dst0.*

El número de componentes tomados de la dirección viene determinado por la dimensionalidad de *dst1.*

Toda la operación se realiza de forma atómica.

Si la invocación del sombreador está inactiva, por ejemplo, si el píxel se ha descartado anteriormente en su ejecución, o si solo existe una invocación de píxel o muestra para servir como asistente de un píxel o muestra real para los derivados, esta instrucción no modifica la memoria *dst1* en absoluto y el valor devuelto no está definido.

El direccionamiento fuera de los límites en u hace que no se escriba nada en la memoria, excepto si la u está estructurada y el desplazamiento de bytes en la estructura (segundo componente de la dirección) está causando el acceso fuera de límites, todo el contenido del UAV se queda \# \# sin definir.

El direccionamiento fuera de límites en u o g hace que se devuelva un resultado no definido al \# \# sombreador en *dst0.*

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, esta instrucción se aplica a todas las fases del sombreador para el entorno de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



| Vértice | Casco | Domain | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo mínimo de sombreador

Esta instrucción se admite en los siguientes modelos de sombreador:



| Modelo de sombreador                                              | Compatible |
|-----------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md)        | sí       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | No        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | No        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | No        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | No        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | No        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





