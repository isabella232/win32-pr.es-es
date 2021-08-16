---
title: Marcar rutas para el estado Hold-Down estado
description: Algunos clientes, como los protocolos de vector de distancia como RIP y DVMRP, requieren que los destinos se anuncien como inaccesibles durante un momento determinado después de eliminar la última ruta al destino.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833f41da08c45d8f9bbe9419360f4d1857b2a52fb92ee0be341b56bc8362536e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790493"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Marcar rutas para el estado Hold-Down estado

Algunos clientes, como los protocolos de vector de distancia como RIP y DVMRP, requieren que los destinos se anuncien como inaccesibles durante un momento determinado después de eliminar la última ruta al destino. La última ruta que se elimina debe anunciarse como inaccesible incluso si las rutas más recientes llegan mientras tanto. La última ruta eliminada se marca como en estado *de retención.* El proceso de retención impide la formación de bucles de enrutamiento. Los bucles de enrutamiento se causan cuando un protocolo de enrutamiento anuncia información de enrutamiento obsoleta. Cuando expira la retención, estos protocolos reanudan su anuncio con la nueva mejor ruta.

Un protocolo que implementa estados de retención indica que un destino está en estado de espera mediante la función [**RtmHoldDestination.**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) El cliente llama a esta función cuando anuncia la mejor ruta a este destino. Si más adelante se eliminan todas las rutas a este destino, la última ruta que se elimina se mantiene en estado de retención durante el período de tiempo especificado en la llamada anterior a **RtmHoldDestination**.

Cuando un protocolo anuncia un destino, la información de ruta que se usa depende de si el protocolo usa estados de retención y si existe una ruta en estado de retención para el destino.

Los protocolos que no usan estados de retención pueden omitir la información de ruta relacionada con los estados de retención de un destino y anunciar siempre la mejor ruta.

Para obtener código de ejemplo que muestra cómo usar estas funciones, vea [Usar el estado de Hold-Down ruta.](use-the-route-hold-down-state.md)

 

 




