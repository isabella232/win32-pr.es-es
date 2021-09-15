---
title: Espacio de direcciones disponible para recursos en mosaico
description: En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568457"
---
# <a name="address-space-available-for-tiled-resources"></a>Espacio de direcciones disponible para recursos en mosaico

En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico.

En sistemas operativos de 64 bits, hay al menos 40 bits de espacio de direcciones virtuales (1 Terabyte) disponible.

Para los sistemas operativos de 32 bits, el espacio de direcciones es de 32 bits (4 GB). En el caso de los sistemas ARM de 32 bits, se puede producir un error en la creación de recursos en mosaico individuales si la asignación usaría más de 27 bits de espacio de direcciones (128 MB). Esto incluye cualquier relleno oculto en el espacio de direcciones que el hardware puede usar para mapas MIP, relleno de mosaico empaquetado y posiblemente dimensiones de superficie de relleno para potencias de 2.

En sistemas gráficos con una tabla de páginas independiente para la unidad de procesamiento de gráficos (GPU), la mayor parte de este espacio de direcciones estará disponible para los recursos de GPU realizados por la aplicación, aunque las asignaciones de GPU realizadas por el controlador de pantalla caben en el mismo espacio.

En sistemas futuros con una tabla de páginas compartida entre la CPU y la GPU, el espacio de direcciones disponible se comparte entre todas las asignaciones de CPU y GPU de un proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




