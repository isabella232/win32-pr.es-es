---
description: Una de las formas más comunes de recibir un evento es a través de una aplicación en ejecución, como una aplicación de administración que recopila y muestra eventos a un usuario.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Recepción de eventos durante la duración de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6815c2ddd7725ccd12dd65b0047874ddce1038b2a2c07f90a40d6f87e6af3a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554223"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Recepción de eventos durante la duración de la aplicación

Una de las formas más comunes de recibir un evento es a través de una aplicación en ejecución, como una aplicación de administración que recopila y muestra eventos a un usuario. Estas aplicaciones se denominan "temporales" porque un consumidor temporal no recibe notificaciones de eventos cuando se apaga.

Un consumidor temporal llama [**aSWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) en script o [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en C++ para suscribirse a eventos en un espacio de nombres. La identidad asociada a esta suscripción es el autor de la llamada.

Un consumidor de eventos temporal puede recibir notificaciones de forma asincrónica o semisincronosa tanto en scripts como en C++.

> [!Note]  
> Por motivos de seguridad, es importante tener en cuenta que no se recomiendan las notificaciones de eventos asincrónicas. Para obtener más información, vea [Establecer la seguridad en una llamada asincrónica.](setting-security-on-an-asynchronous-call.md) Los consumidores de eventos tienen problemas de seguridad especiales. Para obtener más información, [vea Securing WMI Events](securing-wmi-events.md).

 

Para obtener más información sobre cómo recibir notificaciones de eventos asincrónicas y semisincrónicas, vea Recepción de notificaciones de eventos [asincrónicas](receiving-asynchronous-event-notifications.md) y Recepción de notificaciones de eventos semisincronosas. [](receiving-synchronous-and-semisynchronous-event-notifications.md)

 

 



