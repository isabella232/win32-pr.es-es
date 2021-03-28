---
title: Recursos en mosaico
description: Los recursos en mosaico pueden considerarse como recursos lógicos de gran tamaño que utilizan pequeñas cantidades de memoria física.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c7e6aaf60f58f55274c9d7a135b9107933f640
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903176"
---
# <a name="tiled-resources"></a>Recursos en mosaico

Los recursos en mosaico pueden considerarse como recursos lógicos de gran tamaño que utilizan pequeñas cantidades de memoria física.

En esta sección se describe por qué se necesitan recursos en mosaico y cómo crear y usar recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [¿Por qué son necesarios los recursos en mosaico?](why-are-tiled-resources-needed-.md)<br/>       | Los recursos en mosaico son necesarios, por lo que no se podrá tener acceso a la memoria de la unidad de procesamiento de gráficos (GPU), y el hardware puede comprender cómo filtrar por los mosaicos adyacentes.<br/>     |
| [Crear recursos en mosaico](creating-tiled-resources.md)<br/>                     | Los recursos en mosaico se crean mediante la especificación de la marca de [**\_ \_ \_ mosaico varios de recursos D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) cuando se crea un recurso.<br/>                                                                                          |
| [API de recursos en mosaico](tiled-resource-apis.md)<br/>                               | Las API descritas en esta sección funcionan con los recursos en mosaico y el grupo de mosaicos.<br/>                                                                                                                                                              |
| [Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)<br/> | Los recursos en mosaico se pueden usar en las vistas de recursos del sombreador (SRV), las vistas de destino de representación (RTV), las vistas de estarcido de profundidad (DSV) y las vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como los enlaces de búfer de vértices. <br/> |
| [Niveles de características de recursos en mosaico](tiled-resources-features-tiers.md)<br/>         | Direct3D 11,2 expone la compatibilidad con los recursos en mosaico en dos niveles con los valores de [**\_ nivel de \_ recursos \_ en mosaico D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) . <br/>                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





