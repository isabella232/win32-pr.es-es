---
description: ETW proporciona una manera de agrupar eventos relacionados de más de un componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Escribir eventos relacionados en un escenario de un extremo a otro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f1ddde6fa80c0ecd5f95373b6ba4d9b7fcf25e8b3e7be878b14830a404b1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813713"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Escribir eventos relacionados en un escenario de un extremo a otro

ETW proporciona una manera de agrupar eventos relacionados de más de un componente. Por ejemplo, si varios componentes (en el mismo equipo o en equipos diferentes) están implicados en el procesamiento de los mismos datos y cada componente registra eventos para su parte de la actividad, puede agrupar todos los eventos relacionados. Esto permitirá que un consumidor consuma todos los eventos, desde el principio del proceso hasta el final del proceso.

Para escribir eventos relacionados en un [proveedor basado en](about-event-tracing.md) manifiestos, vea Escribir eventos relacionados en un proveedor basado en [manifiestos.](writing-related-events-in-a-manifest-base-provider.md)

Para escribir eventos relacionados en un [proveedor clásico,](about-event-tracing.md) vea [Escribir eventos relacionados en un proveedor clásico.](tracing-event-instances.md)

 

 



