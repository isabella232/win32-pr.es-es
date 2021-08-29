---
title: Destinations
description: Un destino de la tabla de enrutamiento es una entrada de red representada por una dirección de red y una máscara de red.
ms.assetid: 115d86e3-f933-4601-af10-abaab287b509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88195bb0bffab46495693f79a5e4329ec0e83c801c8ee4cf50d8d8bbe39b9ac0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961135"
---
# <a name="destinations"></a>Destinations

Un destino de la tabla de enrutamiento es una entrada de red representada por una dirección de red y una máscara de red.

Una entrada de destino en la tabla de enrutamiento incluye:

-   La dirección, expresada como una dirección de red y una máscara de red.
-   Lista de rutas al destino.
-   Lista de ranuras de puntero opacos.
-   Vistas en las que este destino es válido. El destino contiene una estructura para cada vista que contiene la siguiente información:
    -   Identificador de la vista.
    -   Puntero a la mejor ruta al destino en esta vista.
    -   Propietario de la mejor ruta en esta vista.
    -   Marcas asociadas a la mejor ruta en esta vista.
    -   Controlar las rutas que se encuentran en un estado de retención en esta vista.

 

 




