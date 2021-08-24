---
title: Creación de recursos en mosaico
description: Los recursos en mosaico se crean especificando la marca MISC TILED DE RECURSOS D3D11 \_ \_ al crear un \_ recurso.
ms.assetid: DED2B70C-1E95-4A85-A818-FD32165FBF6C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657fc2cca4d5c1d8fce9efba2013d3cd04291efc7f40d44b4ed325e40f843358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752585"
---
# <a name="creating-tiled-resources"></a>Creación de recursos en mosaico

Los recursos en mosaico se crean especificando la marca [**\_ \_ MISC \_ TILED DE RECURSOS D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) al crear un recurso.

Las restricciones sobre cuándo puede usar [**D3D11 \_ RESOURCE \_ MISC \_ TILED**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) para crear un recurso se describen en Parámetros de creación [de recursos en mosaico.](tiled-resource-creation-parameters.md)

El almacenamiento de un recurso no en mosaico se asigna en el sistema de gráficos cuando se crea el recurso. Por ejemplo, cuando se llama a [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) para crear una matriz de texturas 2D, el sistema de gráficos asigna almacenamiento para esas texturas 2D. Cuando se crea un recurso en mosaico, el sistema de gráficos no asigna el almacenamiento para el contenido del recurso. En su lugar, cuando una aplicación crea un recurso en mosaico, el sistema de gráficos realiza una reserva de espacio de direcciones solo para el área de la superficie en mosaico y, a continuación, permite que la aplicación controle la asignación de los iconos. La "asignación" de un icono es simplemente la ubicación física en memoria a la que apunta un icono lógico de un recurso (o **NULL** para un icono sin asignar). No confunda este concepto con la noción de asignación de un recurso de Direct3D para el acceso a la CPU, que a pesar de usar el mismo nombre es completamente independiente. Podrá definir y cambiar la asignación de cada icono individualmente según sea necesario, sabiendo que no es necesario asignar todos los iconos de una superficie a la vez, con lo que se hace un uso eficaz de la cantidad de memoria disponible.

En esta sección se proporciona más información sobre cómo crear recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                                             | Descripción                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)<br/>                                     | Cuando se crea un recurso con la marca [**\_ \_ MISC \_ TILE de RECURSOS D3D11,**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) los iconos que lo crean proceden de apuntar a ubicaciones de un grupo de iconos. Un grupo de mosaicos es un grupo de memoria (con el respaldo de una o varias asignaciones en segundo plano, no visibles por la aplicación). <br/> |
| [Parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md)<br/>                           | Hay algunas restricciones en el tipo de recursos de Direct3D que puede crear con la marca [**\_ \_ MISC \_ TILED DE RECURSOS D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) En esta sección se proporcionan los parámetros válidos para crear recursos en mosaico.<br/>                                                |
| [Espacio de direcciones disponible para recursos en mosaico](address-space-available-for-tiled-resources.md)<br/>         | En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico. <br/>                                                                                                                                                                                                                           |
| [Parámetros de creación de grupos de iconos](tile-pool-creation-parameters.md)<br/>                                     | Use los parámetros de esta sección para definir grupos de mosaicos a través de la API [**ID3D11Device::CreateBuffer.**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) <br/>                                                                                                                                                                              |
| [Uso compartido de dispositivos y procesos en mosaico](tiled-resource-cross-process-and-device-sharing.md)<br/> | Los grupos de mosaicos se pueden compartir con otros procesos como los recursos tradicionales. Los recursos en mosaico que hacen referencia a grupos de mosaicos no se pueden compartir entre dispositivos y procesos. Pero los procesos independientes pueden crear sus propios recursos en mosaico que se asignan a grupos de mosaicos que se comparten entre esos recursos en mosaico. <br/>          |
| [Operaciones disponibles en recursos en mosaico](operations-available-on-tiled-resources.md)<br/>                 | En esta sección se enumeran las operaciones que puede realizar en recursos en mosaico.<br/>                                                                                                                                                                                                                                             |
| [Operaciones disponibles en grupos de iconos](operations-available-on-tile-pools.md)<br/>                           | En esta sección se enumeran las operaciones que puede realizar en grupos de mosaicos.<br/>                                                                                                                                                                                                                                                  |
| [Cómo se en mosaico el área de un recurso en mosaico](how-a-tiled-resource-s-area-is-tiled.md)<br/>                       | Al crear un recurso en mosaico, las dimensiones, el tamaño del elemento de formato y el número de mipmaps o segmentos de matriz (si procede) determinan el número de mosaicos necesarios para realizar una copia de seguridad de toda la superficie. <br/>                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos en mosaico](tiled-resources.md)
</dt> </dl>

 

 





