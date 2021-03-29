---
description: Un recurso es una colección de datos utilizada por la canalización 3D.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Elegir un recurso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be887fb94f04783b01f8873fb61812bca20faa5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807874"
---
# <a name="choosing-a-resource-direct3d-10"></a>Elegir un recurso (Direct3D 10)

Un recurso es una colección de datos utilizada por la canalización 3D. La creación de recursos y la definición de su comportamiento es el primer paso para programar la aplicación. En esta guía se tratan los temas básicos para elegir los recursos necesarios para la aplicación.

-   [Identificación de las fases de canalización que necesitan recursos](#identify-pipeline-stages-that-need-resources)
-   [Identificar cómo se utilizará cada recurso](#identify-how-each-resource-will-be-used)
-   [Enlazar recursos a fases de canalización](#binding-resources-to-pipeline-stages)
-   [Temas relacionados](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identificación de las fases de canalización que necesitan recursos

El primer paso es elegir la [fase de canalización](d3d10-graphics-programming-guide-pipeline-stages.md) (o fases) que usará un recurso. Es decir, identifique cada fase que va a leer los datos de un recurso, así como las fases que escribirán los datos en un recurso. Conocer las fases de canalización en las que se usarán los recursos determina las API a las que se llamará para enlazar el recurso a la fase.

En esta tabla se enumeran los tipos de recursos que se pueden enlazar a cada fase de canalización. Incluye si el recurso se puede enlazar como entrada o salida, así como la API de enlace.



| Fase de canalización  | Entrada o salida | Recurso               | Tipo de recurso                           | Enlazar API                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ensamblador de entrada | En     | Búfer de vértices          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Ensamblador de entrada | En     | Búfer de índice           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Fases del sombreador   | En     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources), [**GSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources), [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Fases del sombreador   | En     | Búfer de Shader-Constant | Buffer                                  | [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers), [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Salida de flujo   | Fuera    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Fusión de salida   | Fuera    | Representación: vista de destino     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Fusión de salida   | Fuera    | Vista de profundidad/estarcido     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Identificar cómo se utilizará cada recurso

Una vez que haya elegido las fases de canalización que va a usar la aplicación (y, por lo tanto, los recursos que necesitará cada fase), el siguiente paso es determinar cómo se usará cada recurso, es decir, si se puede tener acceso a un recurso mediante la CPU o la GPU.

El hardware en el que se ejecuta la aplicación tendrá como mínimo una CPU y una GPU. Para elegir un valor de uso, tenga en cuenta qué tipo de procesador debe leer o escribir en el recurso de las siguientes opciones (consulte [**\_ uso de D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Resource Usage | Se puede actualizar mediante                    | Frecuencia de actualización |
|----------------|--------------------------------------|---------------------|
| Valor predeterminado        | GPU                                  | con poca frecuencia        |
| Dinámica        | CPU                                  | mayor          |
| Ensayo        | GPU                                  | N/D                 |
| Inmutable      | CPU (solo en el momento de creación de recursos) | N/D                 |



 

El uso predeterminado se debe usar para un recurso que se espera que la CPU actualice con poca frecuencia (menos de una vez por fotograma). Idealmente, la CPU nunca escribiría directamente en un recurso con uso predeterminado para evitar posibles penalizaciones de rendimiento.

El uso dinámico debe usarse en un recurso que la CPU actualice con relativa frecuencia (una o más por fotograma). Un escenario típico de un recurso dinámico sería crear búferes dinámicos de vértices y de índices que se rellenarían en tiempo de ejecución con datos sobre la geometría visible desde el punto de vista del usuario para cada fotograma. Estos búferes se utilizarían para representar solo la geometría visible para el usuario para ese marco.

El uso del almacenamiento provisional debe usarse para copiar datos en otros recursos y desde ellos. Un escenario típico sería copiar los datos de un recurso con uso predeterminado (al que la CPU no puede acceder) a un recurso con uso de almacenamiento provisional (al que la CPU puede tener acceso).

Los recursos inmutables deben usarse cuando los datos del recurso nunca cambien.

Otra forma de ver la misma idea es pensar en lo que hace una aplicación con un recurso.



| Cómo usa la aplicación el recurso     | Resource Usage       |
|---------------------------------------|----------------------|
| Cargar una vez y no actualizar nunca            | Inmutable o predeterminado |
| La aplicación rellena recursos repetidamente | Dinámica              |
| Representar en textura                     | Valor predeterminado              |
| Acceso de CPU de los datos de GPU                | Ensayo              |



 

Si no está seguro de qué uso elegir, empiece con el uso predeterminado, ya que se espera que sea el caso más común. Un búfer Shader-Constant es el tipo de recurso que siempre debería tener el uso predeterminado.

## <a name="binding-resources-to-pipeline-stages"></a>Enlazar recursos a fases de canalización

Un recurso se puede enlazar a más de una fase de canalización al mismo tiempo, siempre y cuando se cumplan las restricciones especificadas cuando se creó el recurso ([**marcas de uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage), marcas de [**enlace**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag), marcas de [**acceso de CPU**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag)). Más concretamente, un recurso se puede enlazar como una entrada y una salida simultáneamente siempre y cuando no se pueda realizar la lectura y la escritura de una parte de un recurso al mismo tiempo.

Al enlazar un recurso, piense en cómo la GPU y la CPU tendrán acceso al recurso. Los recursos que están diseñados para un solo propósito (no se usan varias marcas de acceso de uso, enlace y CPU) serán más que probablemente resulten un mejor rendimiento.

Por ejemplo, considere el caso de un destino de representación que se usa como textura varias veces. Es posible que sea más rápido tener dos recursos: un destino de representación y una textura utilizada como un recurso de sombreador. Cada recurso usaría solo una marca de enlace ([**\_ destino de \_ representación \_ de enlace D3D10**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) o **\_ \_ \_ recurso de sombreador de enlace D3D10**). Los datos se copiarán de la textura de representación-destino a la textura del sombreador mediante [**CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Esto puede mejorar el rendimiento al aislar la escritura de destino de representación de la lectura del sombreador-textura. Por supuesto, la única manera de asegurarse es implementar ambos enfoques y medir la diferencia de rendimiento en una aplicación concreta.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



