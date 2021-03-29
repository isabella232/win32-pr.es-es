---
title: Marcar rutas para el estado Hold-Down
description: Algunos clientes, como los protocolos de vector de distancia como RIP y DVMRP, requieren que los destinos se anuncien como inaccesibles durante un tiempo determinado después de que se elimine la última ruta al destino.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994321"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Marcar rutas para el estado Hold-Down

Algunos clientes, como los protocolos de vector de distancia como RIP y DVMRP, requieren que los destinos se anuncien como inaccesibles durante un tiempo determinado después de que se elimine la última ruta al destino. La última ruta que se elimine debe anunciarse como inaccesible aunque lleguen las rutas más recientes. La última ruta eliminada se marca como en *Estado de suspensión*. El proceso de suspensión impide la formación de bucles de enrutamiento. Los bucles de enrutamiento se producen cuando un protocolo de enrutamiento anuncia información de enrutamiento obsoleta. Cuando expire el tiempo de espera, estos protocolos reanudarán su anuncio con la nueva ruta más adecuada.

Un protocolo que implementa Estados de suspensión indica que un destino está en estado de suspensión mediante la función [**RtmHoldDestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) . El cliente llama a esta función cuando anuncia la mejor ruta a este destino. Si posteriormente se eliminan todas las rutas a este destino, la última ruta que se elimina se mantiene en estado de suspensión durante el período de tiempo especificado en la llamada anterior a **RtmHoldDestination**.

Cuando un protocolo anuncia un destino, la información de ruta que se usa depende de si el protocolo utiliza Estados de retención y si existe una ruta en el estado de retención para el destino.

Los protocolos que no utilizan Estados de suspensión pueden omitir la información de ruta relacionada con los Estados de retención de un destino y siempre anuncian la mejor ruta.

Para ver el código de ejemplo que muestra cómo usar estas funciones, consulte [usar el estado Hold-Down de la ruta](use-the-route-hold-down-state.md).

 

 




