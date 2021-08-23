---
title: Montones de descriptores visibles por el sombreador
description: Los montones de descriptores visibles del sombreador son montones de descriptores a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96fbbb37f3337912780e5882918c0fcbc146c41f8dc60ddf3ba5d2a35c82c1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045402"
---
# <a name="shader-visible-descriptor-heaps"></a>Montones de descriptores visibles por el sombreador

Los montones de descriptores visibles del sombreador son montones de descriptores a los que pueden hacer referencia los sombreadores a través de tablas de descriptores.

-   [Información general](#overview)
-   [Un ejemplo](#an-example)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

Los montones de descriptor a los que pueden hacer referencia los sombreadores a través de tablas de descriptores vienen en un par de tipos: un tipo de montón, D3D12 \_ SRV UAV CBV DESCRIPTOR HEAP, puede contener vistas de recursos de sombreador, vistas de acceso desordenadas y vistas de búfer constante, todas \_ \_ \_ \_ entremezcladas. Cualquier ubicación determinada del montón puede ser cualquiera de los tipos de descriptores enumerados. Otro tipo de montón, D3D12 DESCRIPTOR HEAP TYPE SAMPLER, solo almacena muestreadores, lo que refleja el hecho de que, para la mayoría de hardware, los muestreadores se administran por separado de los SRV, LOS UAV y los \_ \_ \_ \_ CBV.

Se puede solicitar que los montones de descriptores de estos tipos sean visibles o no cuando se crea el montón (este último , que no es visible para el sombreador, puede ser útil para los descriptores de almacenamiento provisional en la CPU). Cuando se solicita que sea visible el sombreador, cada uno de los tipos de montón anteriores puede tener un límite de tamaño de hardware para cualquier asignación de montón de descriptor individual.

Las aplicaciones pueden crear cualquier número de montones de descriptores y los montones de descriptores visibles que no son de sombreador no están restringidos en el tamaño. Si un montón de descriptores visibles del sombreador creado por la aplicación es menor que el límite de tamaño de hardware, el controlador puede optar por asignar el montón de descriptores fuera de un montón de descriptor subyacente más grande para que quepa varios montones de descriptores de API dentro de un montón de descriptores de hardware. La razón por la que esto puede ocurrir es que, para algún hardware, cambiar entre montones de descriptores de hardware durante la ejecución requiere una espera de GPU para que esté inactiva (para asegurarse de que las referencias de GPU al montón de descriptores anteriores han finalizado). Si todos los montones de descriptores que crea una aplicación se ajustan a las capacidades máximas del montón de hardware aplicable, no se producirán tales esperas al cambiar los montones de descriptores de API durante la representación. Sin embargo, las aplicaciones deben permitir la posibilidad de que cambiar el montón del descriptor actual pueda provocar una espera de inactividad.

Para evitar ser afectadas por esta posible espera de inactividad en el conmutador del montón de descriptores, las aplicaciones pueden aprovechar las interrupciones en la representación que harían que la GPU se inactivara por otros motivos, como el tiempo para realizar modificadores del montón de descriptores, ya que de todos modos se está produciendo una espera de inactividad.

El mecanismo y la semántica para identificar montones de descriptores a sombreadores durante la grabación de la lista de comandos o agrupación se describen en la referencia de API.

## <a name="an-example"></a>Un ejemplo

En la imagen siguiente se muestran dos montones de descriptores que hacen referencia a dos texturas 2D independientes que se almacenan en dos ranuras de un montón predeterminado grande. La canalización de gráficos (incluidos los sombreadores) puede acceder al montón de descriptores visible y, por tanto, la textura 2D está disponible para la canalización.

![montones de descriptor visibles y no visibles](images/descriptor-heaps.png)

> [!Note]  
> A menudo hay un límite en el hardware de GPU de la cantidad de memoria local de GPU que puede escribir la CPU (denominada memoria combinada de escritura) para los montones de descriptores. Normalmente, este límite es de alrededor de 96 MB para todos los procesos. Un montón de un millón de descriptores de miembros, con descriptores de 32bytes, usaría hasta 32 MB, por ejemplo. El controlador se retendrán en la memoria del sistema si es necesario, aunque es una buena práctica no crear grandes cantidades de montones de descriptores grandes.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Montones de descriptores](descriptor-heaps.md)
</dt> </dl>

 

 




