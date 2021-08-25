---
title: sync (sm5 - asm)
description: Sincronización de grupos de subprocesos o barrera de memoria.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5c64532669fc94d7d2109c39e501af0825e56434f66b79e20e1641c787a1a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852865"
---
# <a name="sync-sm5---asm"></a>sync (sm5 - asm)

Sincronización de grupos de subprocesos o barrera de memoria.



| sync \[ \_ uglobal\|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Comentarios

**La** sincronización tiene \_ opciones uglobal, \_ ugroup, \_ g y \_ t.

En el sombreador de píxeles, **solo se permite la sincronización de \_ uglobal.**

En el sombreador de proceso, se debe especificar ( \_ \_ uglobal o ugroup \* ) \_ y/o g. \_t es opcional además.

### <a name="_uglobal"></a>\_uglobal

Barrera de \# memoria global u (UAV).

Todas las lecturas o escrituras de memoria u anteriores realizadas por este subproceso en el orden del programa se hacen visibles para todos los subprocesos de toda la GPU antes de que este subproceso acceda a la memoria u \# \# subsiguiente. La parte completa de la GPU de la definición se reemplaza por un ámbito menor que global en un caso, que se describe a continuación.

Esto se aplica a toda la memoria UAV enlazada en la fase actual del sombreador.

\_uglobal está disponible en el sombreador de proceso o en el sombreador de píxeles.

Para cualquier UAV enlazado que no haya sido declarado por el sombreador como Coherente globalmente, la barrera de memoria uglobal u solo tiene visibilidad dentro del grupo de subprocesos del sombreador de proceso actual para ese UAV, como si fuera ugroup en lugar de \_ \# \_ \_ uglobal. Este problema solo se aplica al sombreador de proceso, ya que el sombreador de píxeles debe declarar todos los UAV como coherentes globalmente.

### <a name="_ugroup"></a>\_ugroup

Barrera de memoria \# de ámbito u (UAV) del grupo de subprocesos.

Todas las lecturas o escrituras de memoria u anteriores realizadas por este subproceso en el orden del programa se hacen visibles para todos los subprocesos del grupo de subprocesos antes de que este subproceso acceda a la memoria u \# \# subsiguiente.

Esto se aplica a toda la memoria UAV enlazada en la fase actual del sombreador.

\_ugroup solo está disponible en el sombreador de proceso.

Si \_ ugroup está expuesto, para algunas implementaciones. La ventaja de especificar \_ ugroup en lugar de \_ uglobal es que la operación **de** sincronización se puede completar más rápidamente.

Otras implementaciones no distinguen ugroup de uglobal, por lo que ambas operaciones son \_ \_ equivalentes y se comportan como \_ uglobal. Las aplicaciones pueden especificar su intención solicitando el ámbito de **sincronización** más limitado necesario.

Incluso si un UAV determinado se declara como coherente globalmente, una operación de sincronización de ugroup funcionará de forma más eficaz en ese UAV si no se requiere una barrera \_ global. 

### <a name="_g"></a>\_G

g \# (memoria compartida del grupo de subprocesos).

Todas las lecturas o escrituras de memoria g anteriores realizadas por este subproceso en orden de programa se hacen visibles para todos los subprocesos del grupo de subprocesos antes de que este subproceso obtenga acceso a la memoria \# g \# subsiguiente.

Esto se aplica a toda la memoria compartida g del grupo \# de subprocesos actual.

\_g solo está disponible en el sombreador de proceso.

### <a name="_t"></a>\_t

Sincronización del grupo de subprocesos. Todos los subprocesos de un único grupo de subprocesos (aquellos que pueden compartir el acceso a un conjunto común de espacio de registro compartido) se ejecutarán hasta el punto en que lleguen a esta instrucción antes de que cualquier subproceso pueda continuar.

\_No se puede colocar en el control de flujo dinámico (ramas que pueden variar dentro de un grupo de subprocesos), pero puede estar presente en el control de flujo uniforme, donde todos los subprocesos del grupo seleccionan la misma ruta de acceso.

\_t solo está disponible en el sombreador de proceso.

A continuación se muestra una lista de variantes de "sincronización" del sombreador de proceso.

-   sync \_ g
-   sync \_ ugroup\*
-   sync \_ uglobal
-   sync \_ g \_ t
-   sync \_ ugroup \_ t\*
-   sync \_ uglobal \_ t
-   sync \_ ugroup \_ g\*
-   sync \_ uglobal \_ g
-   sync \_ ugroup \_ g \_ t\*
-   sync \_ uglobal \_ g \_ t

\*Es posible que el compilador HLSL no tenga como destino variantes con ugroup, según la explicación anterior de \_ la \_ sección ugroup anterior.

La lista de variantes de sincronización del sombreador de píxeles incluye solo \_ sync uglobal.

Las barreras de memoria impiden que los compiladores o el hardware reordenen las instrucciones afectadas a través de la barrera.

Varias lecturas de la misma dirección mediante una invocación de sombreador que no están separadas por barreras de memoria o escrituras en la dirección se pueden contraer juntas. Lo mismo se aplica a las escrituras. Los accesos separados por una barrera no se pueden combinar ni mover a través de la barrera.

Las barreras de memoria no son necesarias para que las operaciones atómicas en una dirección determinada por subprocesos diferentes funcionen correctamente. Las barreras son necesarias cuando es necesario sincronizar las operaciones atómicas o de carga y almacenamiento con respecto a las demás, tal como aparecen en subprocesos individuales desde el punto de vista de otros subprocesos.

En el sombreador de píxeles, [las](discard--sm4---asm-.md) instrucciones de descarte implican una barrera uglobal de sincronización, ya que las instrucciones no se \_ pueden reordenar en el **descarte.** sync uglobal en píxeles del asistente (que se ejecutan solo para admitir derivados) o píxeles descartados pueden \_ o no tener ningún efecto. No se permite que el asistente o los píxeles descartados escriban en UAV si, en el caso del descarte, las escrituras se emiten después del descarte. Los valores devueltos de los UAV no pueden contribuir a cálculos derivados. Por lo tanto, se respeta o no la sincronización de u para los píxeles del asistente o cuando se emite después de \_ que un descarte sea irrelevante.

cs \_ 4 \_ 0 y cs \_ 4 \_ 1 admiten esta instrucción.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Domain | Geometría | Píxel | Proceso |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que los UAV están disponibles en todas las fases del sombreador para Direct3D 11.1, la variante **\_ sync uglobal** de esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11.1, que está disponible a partir de Windows 8.



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

 

 




