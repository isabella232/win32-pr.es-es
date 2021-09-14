---
title: Creación de grupos de iconos
description: Un grupo de mosaicos se crea a través de la API ID3D11Device CreateBuffer pasando la marca GRUPO DE MOSAICOS MISC DE RECURSOS de D3D11 en el miembro MiscFlags de la estructura \_ \_ DESC de BÚFER \_ \_ D3D11 a la que apunta el \_ parámetro \_ pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966867"
---
# <a name="tile-pool-creation"></a>Creación de grupos de iconos

Un grupo de mosaicos se crea a través de la API [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) pasando la marca GRUPO DE MOSAICOS MISC RESOURCE [**\_ \_ \_ \_ MISC de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) en el miembro **MiscFlags** de la estructura [**\_ \_ DESC de BÚFER D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a la que apunta el *parámetro pDesc.*

Las aplicaciones pueden crear uno o varios grupos de mosaicos por dispositivo Direct3D. El tamaño total de cada grupo de mosaicos está restringido al límite de tamaño de recursos de Direct3D 11, que es aproximadamente 1/4 de RAM de unidad de procesamiento gráfico (GPU).

Un grupo de mosaicos está hecho de iconos de 64 KB, pero el sistema operativo (controlador de pantalla) administra todo el grupo como una o varias asignaciones en segundo plano: el desglose no es visible para las aplicaciones. Los recursos en mosaico definen el contenido señalando los iconos dentro de un grupo de mosaicos. La desapping de un icono de un recurso en mosaico se realiza señalando el icono a **NULL.** Estos iconos no mapaeados tienen reglas sobre el comportamiento de las lecturas o escrituras. Para obtener información, consulte [Seguimiento de peligro frente a recursos del grupo de mosaicos.](hazard-tracking-versus-tile-pool-resources.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




