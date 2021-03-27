---
title: sincronización (SM5-ASM)
description: Sincronización de grupo de subprocesos o barrera de memoria.
ms.assetid: DCA637FE-8F5C-41D0-8B5E-F913463BA387
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be072b51b4a18d9f1408df0907ec0a55131c18d2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104997000"
---
# <a name="sync-sm5---asm"></a>sincronización (SM5-ASM)

Sincronización de grupo de subprocesos o barrera de memoria.



| sincronizar \[ \_ uglobal \|\_ugroup \] \[ \_ g \] \[ \_ t\] |
|-------------------------------------------|



 

## <a name="remarks"></a>Observaciones

**Sync** tiene las opciones \_ uglobal, \_ ugroup, \_ g y \_ t.

En el sombreador de píxeles, solo se permite la **sincronización de \_ uglobal** .

En el sombreador de cálculo, \_ \_ se deben especificar (uglobal o ugroup \* ) y/o \_ g. \_t es opcional además.

### <a name="_uglobal"></a>\_uglobal

Barrera de \# memoria global u (UAV).

Todas las \# lecturas/escrituras de memoria de u anteriores por este subproceso en el orden del programa se hacen visibles a todos los subprocesos de toda la GPU antes de cualquier \# acceso a la memoria u posterior por este subproceso. Toda la parte de la GPU de la definición se sustituye por un ámbito menos que global en un caso, que se describe a continuación.

Esto se aplica a toda la memoria UAV enlazada en la fase del sombreador actual.

\_uglobal está disponible en el sombreador de cálculo o en el sombreador de píxeles.

En el caso de cualquier UAV enlazado que el sombreador no haya declarado como coherente globalmente, la \_ barrera de memoria de uglobal u \# solo tiene visibilidad dentro del grupo de subprocesos del sombreador de cálculo actual para ese UAV, como si estuviera \_ ugroup en lugar de \_ uglobal. Este problema solo se aplica al sombreador de cálculo, ya que el sombreador de píxeles debe declarar todos los UAVs como coherentes globalmente.

### <a name="_ugroup"></a>\_ugroup

Límite de memoria del ámbito del grupo de subprocesos u \# (UAV).

Todas las \# lecturas o escrituras de memoria de u anteriores por este subproceso en el orden del programa se hacen visibles a todos los subprocesos del grupo de subprocesos antes de cualquier \# acceso a la memoria u posterior por parte de este subproceso.

Esto se aplica a toda la memoria UAV enlazada en la fase del sombreador actual.

\_ugroup solo está disponible en el sombreador de cálculo.

Si \_ se expone ugroup, para algunas implementaciones. La ventaja de especificar \_ ugroup en lugar de \_ uglobal es que la operación de **sincronización** se puede completar con mayor rapidez.

Otras implementaciones no distinguen \_ ugroup de \_ uglobal, por lo que ambas operaciones son equivalentes y se comportan como \_ uglobal. Las aplicaciones pueden especificar su intención solicitando el ámbito más restringido necesario para la **sincronización** .

Aunque un UAV determinado se declare como coherente globalmente, una \_ operación de **sincronización** de ugroup funcionará de manera más eficaz en ese UAV si no se requiere una barrera global.

### <a name="_g"></a>\_i

\#barrera g (memoria compartida del grupo de subprocesos).

Todas las \# lecturas o escrituras anteriores de la memoria de g realizadas por este subproceso en el orden del programa se hacen visibles a todos los subprocesos del grupo de subprocesos antes de cualquier \# acceso posterior a la memoria de g por este subproceso.

Esto se aplica a toda la memoria compartida de g del grupo de subprocesos actual \# .

\_g solo está disponible en el sombreador de cálculo.

### <a name="_t"></a>\_t

Sincronización de grupo de subprocesos. Todos los subprocesos dentro de un único grupo de subprocesos (aquellos que pueden compartir el acceso a un conjunto común de espacio de registro compartido) se ejecutarán hasta el punto en el que lleguen a esta instrucción antes de que cualquier subproceso pueda continuar.

\_no se puede colocar en el control de flujo dinámico (ramas que podrían variar dentro de un grupo de subprocesos), pero pueden estar presentes en el control de flujo uniforme, donde todos los subprocesos del grupo seleccionan la misma ruta de acceso.

\_t solo está disponible en el sombreador de cálculo.

A continuación se muestra una lista de variantes del sombreador de cálculo ' Sync '.

-   sincronizar \_ g
-   sincronizar \_ ugroup\*
-   sincronizar \_ uglobal
-   sincronizar \_ g \_ t
-   sincronizar \_ ugroup \_ t\*
-   sincronizar \_ uglobal \_ t
-   sincronizar \_ ugroup \_ g\*
-   sincronizar \_ uglobal \_ g
-   sincronizar \_ ugroup \_ g \_ t\*
-   sincronizar \_ uglobal \_ g \_ t

\*\_Es posible que las variantes con ugroup no sean el destino del compilador de HLSL, según la explicación anterior en la \_ sección ugroup anterior.

La lista de variantes de sincronización del sombreador de píxeles incluye \_ solo uglobal de sincronización.

Las barreras de memoria impiden que las instrucciones afectadas se reordenen mediante compiladores o hardware a través de la barrera.

Varias lecturas de la misma dirección mediante una invocación del sombreador que no están separadas por barreras de memoria o las escrituras en la dirección se pueden contraer juntas. Lo mismo se aplica a las escrituras. Los accesos separados por una barrera no se pueden combinar ni pasar por la barrera.

Las barreras de memoria no son necesarias para que los distintos subprocesos funcionen correctamente las operaciones atómicas en una dirección determinada. Las barreras son necesarias cuando es necesario sincronizar las operaciones atómicas o de carga y almacenamiento con respecto a las demás, tal como aparecen en subprocesos individuales desde el punto de vista de otros subprocesos.

En el sombreador de píxeles, las instrucciones [descartadas](discard--sm4---asm-.md) implican una \_ barrera uglobal de sincronización, en las instrucciones no se pueden reordenar en la **descartar**. \_la sincronización de uglobal en píxeles auxiliares (que solo se ejecutan para admitir derivados) o los píxeles descartados puede o no tener ningún efecto. No se permite que los píxeles auxiliares o descartados escriban en UAVs si, en el caso de discard, las escrituras se emiten después de la descarte. Los valores devueltos de UAVs no pueden contribuir a cálculos derivados. Por lo tanto, tanto si se cumple la sincronización u como si no \_ para los píxeles del ayudante o cuando se emite después de un descarte, se Moot.

CS \_ 4 \_ 0 y CS \_ 4 \_ 1 admiten esta instrucción.

Esta instrucción se aplica a las siguientes fases del sombreador:



| Vértice | Casco | Dominio | Geometría | Píxel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Dado que UAVs están disponibles en todas las fases del sombreador para Direct3D 11,1, la variante **Sync \_ uglobal** de esta instrucción se aplica a todas las fases del sombreador para el tiempo de ejecución de Direct3D 11,1, que está disponible a partir de Windows 8.



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

 

 




