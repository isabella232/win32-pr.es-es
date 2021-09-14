---
title: imm_atomic_alloc (sm5 - asm)
description: Incremente de forma atómica el contador oculto de 32 bits almacenado con una vista de acceso no ordenado (UAV) Count o Append, devolviendo el valor original.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888204"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>imm \_ atomic \_ alloc (sm5 - asm)

Incremente de forma atómica el contador oculto de 32 bits almacenado con una vista de acceso no ordenado (UAV) Count o Append, devolviendo el valor original.



| imm \_ atomic \_ alloc dst0 \[ .single component mask , \_ \_ \] dstUAV |
|-------------------------------------------------------------|



 



| Elemento                                                                                           | Descripción                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[en \] Contiene el valor de contador devuelto.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[en \] un UAV de búfer estructurado con la marca Recuento o Anexar. <br/> |



 

## <a name="remarks"></a>Observaciones

Hay un valor de contador entero de 32 bits sin signo oculto asociado a cada vista Count o Append Buffer que se inicializa cuando la vista está enlazada a la canalización, incluida la opción de mantener el valor anterior.

Esta instrucción realiza un incremento atómico del valor del contador y devuelve el original a *dst0.*

Para un UAV append, el valor devuelto solo es válido mientras dure la invocación del sombreador. Después, la implementación puede reorganizar el diseño de memoria. Cualquier direccionamiento de memoria basado en el valor devuelto debe limitarse a la invocación del sombreador.

Para un UAV Append, dentro de la invocación del sombreador, el compilador HLSL puede usar el valor devuelto como índice de estructura que se va a usar para acceder al búfer estructurado. El acceso a cualquier índice de estructura distinto de las ubicaciones [ \_](imm-atomic-consume--sm5---asm-.md) devueltas por las llamadas a la asignación atómica de **imm \_ \_** o consumo produce resultados indefinidos en que la ubicación de memoria exacta dentro del UAV es aleatoria y solo se fija durante la vigencia de la invocación del sombreador.

Para un UAV de recuento, la aplicación puede guardar el valor devuelto como una referencia a una ubicación fija dentro del UAV que sea significativa una vez que se haya terminado la invocación del sombreador. Siempre se puede acceder a cualquier ubicación de un UAV de recuento independientemente del valor de recuento.

No hay ninguna fijación del recuento, por lo que se ajusta al desbordamiento.

El mismo sombreador no puede intentar el consumo **\_ \_ atómico de imm atomic y** **imm \_ \_ en** el mismo UAV. Además, la GPU no puede permitir que varias invocaciones de sombreador mezclen la alocación atómica de **\_ \_ imm** y el consumo **\_ atómico \_** de imm en el mismo UAV.

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
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Shader Model 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Ensamblado del modelo de sombreador 5 (HLSL de DirectX)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





