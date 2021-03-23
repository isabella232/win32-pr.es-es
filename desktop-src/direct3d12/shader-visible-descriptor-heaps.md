---
title: Montones de descriptor visibles del sombreador
description: Los montones de descriptor visibles del sombreador, son montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104280"
---
# <a name="shader-visible-descriptor-heaps"></a>Montones de descriptor visibles del sombreador

Los montones de descriptor visibles del sombreador, son montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.

-   [Información general](#overview)
-   [Un ejemplo](#an-example)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Los montones de descriptor a los que pueden hacer referencia los sombreadores a través de las tablas de descriptores tienen un par de tipos: un tipo de montón, D3D12 \_ SRV \_ UAV \_ CBV de \_ descriptor \_ , puede contener vistas de recursos del sombreador, vistas de acceso desordenado y vistas de búfer de constantes, todo entremezclado. Cualquier ubicación determinada en el montón puede ser cualquiera de los tipos de descriptores enumerados. Otro tipo de montón, \_ \_ \_ la muestra de tipo de montón del descriptor de D3D12 \_ , solo almacena los muestreadores, que reflejan el hecho de que, para la mayoría del hardware, los muestreadores se administran de forma independiente de SRVs, UAVs, CBVs.

Es posible que se solicite a los montones de descriptores de estos tipos que sean visibles para el sombreador o no cuando se cree el montón (el último, que no es un sombreador visible, puede ser útil para descriptores de ensayo en la CPU). Cuando se solicita que el sombreador sea visible, cada uno de los tipos de montones anteriores puede tener un límite de tamaño de hardware para cualquier asignación de montón de descriptor individual.

Las aplicaciones pueden crear cualquier número de montones de descriptor y los montones de descriptores no visibles de sombreador no tienen restricciones de tamaño. Si un montón de descriptor visible del sombreador creado por la aplicación es menor que el límite de tamaño del hardware, el controlador puede optar por subasignar el montón del descriptor de un montón de descriptor subyacente más grande para que varios montones de descriptor de la API se ajusten a un montón de descriptores de hardware. La razón por la que esto puede ocurrir es que, para un determinado hardware, el cambio entre los montones de descriptores de hardware durante la ejecución requiere un tiempo de espera de GPU para inactivo (para asegurarse de que las referencias de GPU al montón de descriptor anterior se han completado) Si todos los montones de descriptor que crea una aplicación caben en las capacidades máximas del montón de hardware aplicable, entonces no se producirá ninguna espera al cambiar los montones del descriptor de la API durante la representación. Las aplicaciones deben permitir, sin embargo, que el cambio de la pila de descriptores actual pueda incurrir en una espera de inactividad.

Para evitar que esto se vea afectado por esta posible espera de inactividad en el modificador del montón del descriptor, las aplicaciones pueden aprovechar las ventajas de los saltos en la representación que harían que la GPU estuviera inactiva por otras razones como el tiempo para realizar los cambios del montón de descriptor, ya que se produce una espera de inactividad.

El mecanismo y la semántica para identificar montones de descriptores en sombreadores durante la grabación de la lista de comandos o el lote se describen en la referencia de la API.

## <a name="an-example"></a>Un ejemplo

En la imagen siguiente se muestran dos montones de descriptor que hacen referencia a dos texturas 2D independientes que se almacenan en dos ranuras de un montón predeterminado de gran tamaño. La canalización de gráficos (incluidos los sombreadores) puede tener acceso al montón de descriptor que es visible para el sombreador y, por lo tanto, la textura 2D está disponible para la canalización.

![montones de descriptores visibles y no visibles](images/descriptor-heaps.png)

> [!Note]  
> A menudo hay un límite en el hardware de GPU de la cantidad de memoria local de GPU que se pueda escribir en la CPU (denominada memoria combinada) para los montones de descriptor. Normalmente, este límite está alrededor de 96MB para todos los procesos. Un montón de descriptores de miembro 1 millón, con descriptores de 32byte, usaría 32 MB, por ejemplo. Si es necesario, el controlador revertirá la memoria del sistema, aunque es recomendable no crear un gran número de montones de descriptores grandes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




