---
description: El servicio Ws232.dll proporciona facilidades para la creación de objetos de evento tanto para las aplicaciones como para los proveedores de servicios, aunque en la mayoría de los casos las aplicaciones crearán objetos \_ de evento.
ms.assetid: 86da30ad-80bc-4982-9306-bbe29b1bab19
title: Crear objetos de evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab867e6398db4b5c97303c8739431d7baaca311daf8d103f4375721e96a864b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051703"
---
# <a name="creating-event-objects"></a>Crear objetos de evento

El servicio Ws232.dll proporciona facilidades para la creación de objetos de evento tanto para las aplicaciones como para los proveedores de servicios, aunque en la mayoría de los casos las aplicaciones crearán objetos \_ de evento. Los servicios de objetos de evento están disponibles para los proveedores de servicios Windows Sockets a través de [**WPUCreateEvent**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreateevent) simplemente como un mecanismo de comodidad para cualquier procesamiento interno que pueda beneficiarse del mismo. Tenga en cuenta que el identificador del objeto de evento solo es válido en el contexto del proceso de llamada. En Windows entornos, la realización de objetos de evento se realiza a través de los servicios de eventos nativos proporcionados por el sistema operativo.

 

 



