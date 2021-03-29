---
title: Creación de grupos de iconos
description: Un grupo de mosaicos se crea a través de la API de ID3D11Device CreateBuffer pasando la \_ marca D3D11 Resource \_ Misc del \_ \_ grupo de mosaicos en el miembro MiscFlags de la \_ estructura DESC del búfer D3D11 \_ al que apunta el parámetro pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104996733"
---
# <a name="tile-pool-creation"></a>Creación de grupos de iconos

Un grupo de mosaicos se crea a través de la API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) pasando la marca [**D3D11 \_ Resource \_ Misc del \_ \_ grupo de mosaicos**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) en el miembro **MiscFlags** de la estructura [**\_ \_ DESC del búfer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) a la que apunta el parámetro *pDesc* .

Las aplicaciones pueden crear uno o varios grupos de mosaicos por dispositivo Direct3D. El tamaño total de cada grupo de mosaicos está restringido al límite de tamaño de los recursos de Direct3D 11, que es aproximadamente 1/4 de RAM de unidad de procesamiento de gráficos (GPU).

Un grupo de mosaicos se compone de mosaicos de 64 KB, pero el sistema operativo (Mostrar controlador) administra todo el grupo como una o más asignaciones en segundo plano; el desglose no es visible para las aplicaciones. Los recursos en mosaico definen el contenido apuntando a los mosaicos de un grupo de mosaicos. La desasignación de un icono de un recurso en mosaico se realiza apuntando el icono a **null**. Estos mosaicos sin asignar tienen reglas sobre el comportamiento de las lecturas o escrituras. Para obtener información, consulte [seguimiento de peligros frente a recursos del grupo de mosaicos](hazard-tracking-versus-tile-pool-resources.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Mapas en un grupo de iconos](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




