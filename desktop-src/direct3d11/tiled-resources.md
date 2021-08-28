---
title: Recursos en mosaico
description: Los recursos en mosaico se pueden pensar como recursos lógicos grandes que usan pequeñas cantidades de memoria física.
ms.assetid: 03083460-192b-40cb-8ee1-76df6d95f72b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73835d6603d1d8d7e708cd422e3991bb88ac1f91cebf016ccce36f2466270c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124093"
---
# <a name="tiled-resources"></a>Recursos en mosaico

Los recursos en mosaico se pueden pensar como recursos lógicos grandes que usan pequeñas cantidades de memoria física.

En esta sección se describe por qué se necesitan recursos en mosaico y cómo crear y usar recursos en mosaico.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                   | Descripción                                                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [¿Por qué se necesitan recursos en mosaico?](why-are-tiled-resources-needed-.md)<br/>       | Se necesitan recursos en mosaico, por lo que se desperdicia menos memoria de la unidad de procesamiento gráfico (GPU) almacenando regiones de superficies a las que la aplicación sabe que no se accederá y el hardware puede entender cómo filtrar entre iconos adyacentes.<br/>     |
| [Creación de recursos en mosaico](creating-tiled-resources.md)<br/>                     | Los recursos en mosaico se crean especificando la marca [**\_ \_ MISC \_ TILED DE RECURSOS D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) al crear un recurso.<br/>                                                                                          |
| [API de recursos en mosaico](tiled-resource-apis.md)<br/>                               | Las API descritas en esta sección funcionan con recursos en mosaico y un grupo de mosaicos.<br/>                                                                                                                                                              |
| [Acceso de canalización a recursos en mosaico](pipeline-access-to-tiled-resources.md)<br/> | Los recursos en mosaico se pueden usar en vistas de recursos de sombreador (SRV), vistas de destino de representación (RTV), vistas de galería de símbolos de profundidad (DSV) y vistas de acceso desordenado (UAV), así como algunos puntos de enlace donde no se usan vistas, como enlaces de búfer de vértices. <br/> |
| [Niveles de características de recursos en mosaico](tiled-resources-features-tiers.md)<br/>         | Direct3D 11.2 expone la compatibilidad con recursos en mosaico en dos niveles con los valores de NIVEL DE RECURSOS [**\_ MOSAICOS \_ \_ D3D11.**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_tiled_resources_tier) <br/>                                                                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recursos](overviews-direct3d-11-resources.md)
</dt> </dl>

 

 





