---
title: Crear recursos en mosaico
description: Los recursos en mosaico se crean mediante la especificación de \_ la \_ marca de mosaico varios de recursos D3D11 \_ cuando se crea un recurso.
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd6e2c0e457bfd8534d3a42c6f658095b3349572
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/13/2019
ms.locfileid: "104419872"
---
# <a name="creating-tiled-resources"></a>Crear recursos en mosaico

Los recursos en mosaico se crean mediante la especificación de la marca de [**\_ \_ \_ mosaico varios de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) cuando se crea un recurso.

Las restricciones en cuanto al uso de los [**recursos de D3D11 en \_ \_ \_ mosaico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) para crear un recurso se describen en [parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md).

El almacenamiento de un recurso no en mosaico se asigna en el sistema de gráficos cuando se crea el recurso. Por ejemplo, al llamar a [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) para crear una matriz de texturas 2D, el sistema de gráficos asigna almacenamiento para esas texturas 2D. Cuando se crea un recurso en mosaico, el sistema de gráficos no asigna el almacenamiento para el contenido del recurso. En su lugar, cuando una aplicación crea un recurso en mosaico, el sistema de gráficos realiza una reserva de espacio de direcciones solo para el área de la superficie en mosaico y, a continuación, permite que la aplicación controle la asignación de los mosaicos. La "asignación" de un icono es simplemente la ubicación física en memoria a la que apunta un icono lógico en un recurso (o **null** para un mosaico sin asignar). No confunda este concepto con la noción de asignar un recurso de Direct3D para el acceso a la CPU, que a pesar de usar el mismo nombre es completamente independiente. Podrá definir y cambiar la asignación de cada mosaico individualmente según sea necesario, sabiendo que no es necesario asignar todos los mosaicos de una superficie a la vez, con lo que se consigue un uso eficaz de la cantidad de memoria disponible.

En esta sección se proporciona más información sobre cómo crear recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)<br/>                                     | Cuando un recurso se crea con la marca [**D3D11 de \_ recursos varios en \_ \_ mosaico**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) , los mosaicos que componen el recurso provienen de apuntar a ubicaciones de un grupo de mosaicos. Un grupo de mosaicos es un grupo de memoria (respaldado por una o varias asignaciones en segundo plano, no detectadas por la aplicación). <br/> |
| [Parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md)<br/>                           | Existen algunas restricciones en el tipo de recursos de Direct3D que se pueden crear con la marca de [**\_ mosaico de \_ varios \_ recursos de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) . En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.<br/>                                                |
| [Espacio de direcciones disponible para los recursos en mosaico](address-space-available-for-tiled-resources.md)<br/>         | En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico. <br/>                                                                                                                                                                                                                           |
| [Parámetros de creación de grupos de iconos](tile-pool-creation-parameters.md)<br/>                                     | Use los parámetros de esta sección para definir grupos de mosaicos a través de la API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) . <br/>                                                                                                                                                                              |
| [Proceso cruzado y uso compartido de dispositivos entre recursos en mosaico](tiled-resource-cross-process-and-device-sharing.md)<br/> | Los grupos de mosaicos se pueden compartir con otros procesos, al igual que los recursos tradicionales. Los recursos en mosaico que hacen referencia a los grupos de mosaicos no se pueden compartir entre dispositivos y procesos. Sin embargo, los procesos independientes pueden crear sus propios recursos en mosaico que se asignan a los grupos de mosaicos que se comparten entre esos recursos en mosaico. <br/>          |
| [Operaciones disponibles en los recursos en mosaico](operations-available-on-tiled-resources.md)<br/>                 | En esta sección se enumeran las operaciones que se pueden realizar en los recursos en mosaico.<br/>                                                                                                                                                                                                                                             |
| [Operaciones disponibles en grupos de iconos](operations-available-on-tile-pools.md)<br/>                           | En esta sección se enumeran las operaciones que se pueden realizar en grupos de mosaicos.<br/>                                                                                                                                                                                                                                                  |
| [Cómo se organiza en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Cuando se crea un recurso en mosaico, las dimensiones, el tamaño de los elementos de formato y el número de mapas MIP y/o segmentos de matriz (si procede) determinan el número de mosaicos necesarios para respaldar todo el área expuesta. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 





