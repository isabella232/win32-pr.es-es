---
description: ETW proporciona una manera de agrupar eventos relacionados de más de un componente.
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: Escritura de eventos relacionados en un escenario de un extremo a otro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984543"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>Escritura de eventos relacionados en un escenario de un extremo a otro

ETW proporciona una manera de agrupar eventos relacionados de más de un componente. Por ejemplo, si hay varios componentes (en el mismo equipo o en equipos diferentes) implicados en el procesamiento de los mismos datos, y cada componente registra eventos para su parte de la actividad, puede agrupar todos los eventos relacionados. Esto permitirá que un consumidor consuma todos los eventos, desde el principio del proceso hasta el final del proceso.

Para escribir eventos relacionados en un proveedor basado en [manifiestos](about-event-tracing.md) , vea [escribir eventos relacionados en un proveedor basado en manifiestos](writing-related-events-in-a-manifest-base-provider.md).

Para escribir eventos relacionados en un proveedor [clásico](about-event-tracing.md) , consulte [escribir eventos relacionados en un proveedor clásico](tracing-event-instances.md).

 

 



