---
title: Creación de grupos de iconos
description: Un grupo de mosaicos se crea a través de la API ID3D11Device CreateBuffer pasando la marca GRUPO DE MOSAICOS MISC DE RECURSOS D3D11 en el miembro MiscFlags de la estructura \_ \_ \_ DESC buffer de \_ D3D11 a la que apunta el parámetro \_ \_ pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec98038f2c58de0feae7fa491c45945e9e2a30d112ee45a6c3116209f126222e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124103"
---
# <a name="tile-pool-creation"></a>Creación de grupos de iconos

Un grupo de mosaicos se crea a través de la API [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) pasando la marca GRUPO DE MOSAICOS MISC DE RECURSOS de [**D3D11 \_ \_ \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) en el miembro **MiscFlags** de la estructura [**\_ \_ DESC buffer de D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a la que apunta el *parámetro pDesc.*

Las aplicaciones pueden crear uno o varios grupos de mosaicos por dispositivo Direct3D. El tamaño total de cada grupo de mosaicos está restringido al límite de tamaño de recursos de Direct3D 11, que es aproximadamente 1/4 de RAM de unidad de procesamiento gráfico (GPU).

Un grupo de mosaicos está hecho de iconos de 64 KB, pero el sistema operativo (controlador para mostrar) administra todo el grupo como una o varias asignaciones en segundo plano: el desglose no es visible para las aplicaciones. Los recursos en mosaico definen el contenido señalando los iconos dentro de un grupo de mosaicos. La desapping de un icono de un recurso en mosaico se realiza señalando el icono a **NULL.** Estos iconos no mapa tienen reglas sobre el comportamiento de las lecturas o escrituras. Para obtener información, consulte [Seguimiento de riesgos frente a recursos del grupo de mosaicos.](hazard-tracking-versus-tile-pool-resources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




