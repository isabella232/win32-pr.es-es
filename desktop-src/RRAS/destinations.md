---
title: Destinations
description: Un destino de la tabla de enrutamiento es una entrada de red representada por una dirección de red y una máscara de red.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c0c758720824284147c2f35be004622157edb3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903541"
---
# <a name="destinations"></a>Destinations

Un destino de la tabla de enrutamiento es una entrada de red representada por una dirección de red y una máscara de red.

Una entrada de destino en la tabla de enrutamiento incluye:

-   La dirección, expresada como una dirección de red y una máscara de red.
-   Una lista de rutas al destino.
-   Una lista de ranuras de puntero opacas.
-   Vistas en las que este destino es válido. El destino contiene una estructura para cada vista que contiene la información siguiente:
    -   Identificador de la vista.
    -   Puntero a la mejor ruta al destino en esta vista.
    -   Propietario de la mejor ruta de esta vista.
    -   Marcas asociadas a la mejor ruta en esta vista.
    -   Identificador de las rutas que están en estado de suspensión en esta vista.

 

 




