---
description: Una de las formas más comunes de recibir un evento es a través de una aplicación en ejecución, como una aplicación de administración que recopila y muestra eventos a un usuario.
ms.assetid: 380ac556-ba0a-4fae-8b76-0645d99e8583
ms.tgt_platform: multiple
title: Recepción de eventos mientras dure la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd6b9731dd662a92296a86910a6cf8cb231cca1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082396"
---
# <a name="receiving-events-for-the-duration-of-your-application"></a>Recepción de eventos mientras dure la aplicación

Una de las formas más comunes de recibir un evento es a través de una aplicación en ejecución, como una aplicación de administración que recopila y muestra eventos a un usuario. Estas aplicaciones se denominan "temporales" porque un consumidor temporal no recibe notificaciones de eventos cuando se apaga.

Un consumidor temporal llama [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md) en el script o [**IWbemServices.ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) en C++ para suscribirse a eventos en un espacio de nombres. La identidad asociada a esta suscripción es el autor de la llamada.

Un consumidor de eventos temporal puede recibir notificaciones de forma asincrónica o semisincrónica tanto en scripts como en C++.

> [!Note]  
> Por motivos de seguridad, es importante tener en cuenta que no se recomiendan las notificaciones de eventos asincrónicos. Para obtener más información, vea [establecer la seguridad en una llamada asincrónica](setting-security-on-an-asynchronous-call.md). Los consumidores de eventos tienen problemas de seguridad especiales. Para obtener más información, consulte [protección de eventos WMI](securing-wmi-events.md).

 

Para obtener más información sobre la recepción de notificaciones de eventos asincrónicos y semisincrónicos, consulte recibir notificaciones de eventos [asincrónicos](receiving-asynchronous-event-notifications.md) y [recibir notificaciones de eventos sincrónicos](receiving-synchronous-and-semisynchronous-event-notifications.md).

 

 



