---
title: Espacio de direcciones disponible para los recursos en mosaico
description: En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/13/2019
ms.locfileid: "103784864"
---
# <a name="address-space-available-for-tiled-resources"></a>Espacio de direcciones disponible para los recursos en mosaico

En esta sección se especifica el espacio de direcciones virtuales que está disponible para los recursos en mosaico.

En los sistemas operativos de 64 bits, hay disponible al menos 40 bits de espacio de direcciones virtuales (1 terabyte).

En el caso de los sistemas operativos de 32 bits, el espacio de direcciones es de 32 bits (4 GB). En el caso de los sistemas ARM de 32 bits, se puede producir un error en la creación de recursos en mosaico individuales si la asignación usaría más de 27 bits de espacio de direcciones (128 MB). Esto incluye cualquier relleno oculto en el espacio de direcciones que el hardware puede usar para los mapas de caracteres, el relleno de mosaico empaquetado y, posiblemente, el relleno de las dimensiones de superficie a potencias de 2.

En los sistemas de gráficos con una tabla de páginas independiente para la unidad de procesamiento de gráficos (GPU), la mayor parte de este espacio de direcciones estará disponible para los recursos de GPU que realiza la aplicación, aunque las asignaciones de GPU realizadas por el controlador de pantalla caben en el mismo espacio.

En los sistemas futuros con una tabla de páginas compartida entre la CPU y la GPU, el espacio de direcciones disponible se comparte entre todas las asignaciones de CPU y GPU en un proceso.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Parámetros de creación de recursos en mosaico](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




