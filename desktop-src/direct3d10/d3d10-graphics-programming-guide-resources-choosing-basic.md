---
description: Un recurso es una colección de datos que usa la canalización 3D.
ms.assetid: 802400fa-a606-4d3d-a61d-1cdb5a9f0437
title: Elegir un recurso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de635e9ad5ece322de9c34438be45db991e6700dc6192509f70b6b0f53e351b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119380325"
---
# <a name="choosing-a-resource-direct3d-10"></a>Elegir un recurso (Direct3D 10)

Un recurso es una colección de datos que usa la canalización 3D. Crear recursos y definir su comportamiento es el primer paso para programar la aplicación. En esta guía se tratan los temas básicos para elegir los recursos que requiere la aplicación.

-   [Identificar las fases de canalización que necesitan recursos](#identify-pipeline-stages-that-need-resources)
-   [Identificar cómo se usará cada recurso](#identify-how-each-resource-will-be-used)
-   [Enlazar recursos a fases de canalización](#binding-resources-to-pipeline-stages)
-   [Temas relacionados](#related-topics)

## <a name="identify-pipeline-stages-that-need-resources"></a>Identificar las fases de canalización que necesitan recursos

El primer paso consiste en elegir la fase [de canalización](d3d10-graphics-programming-guide-pipeline-stages.md) (o fases) que usará un recurso. Es decir, identifique cada fase que leerá datos de un recurso, así como las fases que escribirán datos en un recurso. Conocer las fases de canalización donde se usarán los recursos determina las API a las que se llamará para enlazar el recurso a la fase.

En esta tabla se enumeran los tipos de recursos que se pueden enlazar a cada fase de canalización. Incluye si el recurso se puede enlazar como una entrada o una salida, así como la API de enlace.



| Fase de canalización  | Entrada o salida | Resource               | Tipo de recurso                           | API de enlace                                                                                                                                                                                                |
|-----------------|--------|------------------------|-----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Ensamblador de entrada | En     | Búfer de vértices          | Buffer                                  | [**IASetVertexBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)                                                                                                                                           |
| Ensamblador de entrada | En     | Búfer de índice           | Buffer                                  | [**IASetIndexBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)                                                                                                                                               |
| Fases del sombreador   | En     | Shader-ResourceView    | Buffer, Texture1D, Texture2D, Texture3D | [**VSSetShaderResources,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetshaderresources) [**GSSetShaderResources,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetshaderresources) [**PSSetShaderResources**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetshaderresources) |
| Fases del sombreador   | En     | Shader-Constant buffer | Buffer                                  | [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers), [**GSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers) |
| Salida de flujo   | Fuera    | Buffer                 | Buffer                                  | [**SOSetTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-sosettargets)                                                                                                                                                       |
| Fusión de salida   | Fuera    | Vista de destino de representación     | Buffer, Texture1D, Texture2D, Texture3D | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |
| Fusión de salida   | Fuera    | Vista profundidad/galería de símbolos     | Texture1D, Texture2D                    | [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)                                                                                                                                           |



 

## <a name="identify-how-each-resource-will-be-used"></a>Identificar cómo se usará cada recurso

Una vez que haya elegido las fases de canalización que usará la aplicación (y, por tanto, los recursos que necesitará cada fase), el paso siguiente consiste en determinar cómo se usará cada recurso, es decir, si la CPU o la GPU pueden acceder a un recurso.

El hardware en el que se ejecuta la aplicación tendrá como mínimo una CPU y una GPU como mínimo. Para elegir un valor de uso, tenga en cuenta qué tipo de procesador debe leer o escribir en el recurso de las siguientes opciones (vea [**D3D10 \_ USAGE**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)).



| Resource Usage | Se puede actualizar mediante                    | Frecuencia de actualización |
|----------------|--------------------------------------|---------------------|
| Valor predeterminado        | GPU                                  | Infrecuentemente        |
| Dinámica        | CPU                                  | Frecuentemente          |
| Ensayo        | GPU                                  | N/D                 |
| Inmutable      | CPU (solo en el momento de la creación de recursos) | N/D                 |



 

El uso predeterminado debe usarse para un recurso que se espera que la CPU actualice con poca frecuencia (menos de una vez por fotograma). Idealmente, la CPU nunca escribiría directamente en un recurso con uso predeterminado para evitar posibles penalizaciones de rendimiento.

El uso dinámico debe usarse para un recurso que la CPU actualiza con relativa frecuencia (una o varias veces por fotograma). Un escenario típico para un recurso dinámico sería crear búferes dinámicos de vértices e índices que se rellenarían en tiempo de ejecución con datos sobre la geometría visible desde el punto de vista del usuario para cada fotograma. Estos búferes se usarían para representar solo la geometría visible para el usuario para ese marco.

El uso de almacenamiento provisional debe usarse para copiar datos hacia y desde otros recursos. Un escenario típico sería copiar datos en un recurso con uso predeterminado (al que la CPU no puede acceder) a un recurso con uso de almacenamiento provisional (al que la CPU puede acceder).

Los recursos inmutables deben usarse cuando los datos del recurso nunca cambien.

Otra manera de ver la misma idea es pensar en lo que hace una aplicación con un recurso.



| Uso del recurso por parte de la aplicación     | Resource Usage       |
|---------------------------------------|----------------------|
| Cargar una vez y nunca actualizar            | Inmutable o predeterminado |
| La aplicación rellena el recurso repetidamente | Dinámica              |
| Representación en textura                     | Valor predeterminado              |
| Acceso de CPU de datos de GPU                | Ensayo              |



 

Si no está seguro de qué uso elegir, comience con el uso predeterminado, ya que se espera que sea el caso más común. Un Shader-Constant búfer es el tipo de recurso que siempre debe tener el uso predeterminado.

## <a name="binding-resources-to-pipeline-stages"></a>Enlazar recursos a fases de canalización

Un recurso se puede enlazar a más de una fase de canalización al mismo tiempo, siempre y cuando se cumplen las restricciones especificadas cuando se creó el recurso [**(marcas**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)de [**uso,**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)marcas de enlace, marcas de acceso de [**cpu).**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cpu_access_flag) Más concretamente, un recurso se puede enlazar como una entrada y una salida simultáneamente, siempre y cuando no se pueda leer y escribir parte de un recurso al mismo tiempo.

Al enlazar un recurso, piense en cómo la GPU y la CPU accederán al recurso. Los recursos diseñados para un único propósito (no usan varias marcas de uso, enlace y acceso a la CPU) probablemente darán como resultado un mejor rendimiento.

Por ejemplo, considere el caso de un destino de representación usado como textura varias veces. Puede ser más rápido tener dos recursos: un destino de representación y una textura que se usa como recurso de sombreador. Cada recurso usaría solo una marca de enlace [**(D3D10 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag) o **D3D10 \_ BIND SHADER \_ \_ RESOURCE).** Los datos se copiarán de la textura de destino de representación a la textura del sombreador [**mediante CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) o [**CopySubresourceRegion.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) Esto puede mejorar el rendimiento mediante el aislamiento de la escritura de destino de representación de la lectura de textura del sombreador. Por supuesto, la única manera de estar seguro es implementar ambos enfoques y medir la diferencia de rendimiento en la aplicación en particular.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



