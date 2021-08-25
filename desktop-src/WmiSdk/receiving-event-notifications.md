---
description: Los consumidores de eventos temporales, los consumidores de eventos permanentes y los proveedores de eventos usan las consultas de eventos. Los consumidores de eventos usan consultas de eventos para especificar eventos de interés y los proveedores de eventos usan las consultas para especificar los eventos que proporcionan.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Recepción de notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1064fd0098ac72c6ceecbb5fcbc212fb38f6b2b25d0e61d8149bdb0fad177267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996016"
---
# <a name="receiving-event-notifications"></a>Recepción de notificaciones de eventos

Los consumidores de eventos temporales, los consumidores de eventos permanentes y los proveedores de eventos usan las consultas de eventos. Los consumidores de eventos usan consultas de eventos para especificar eventos de interés y los proveedores de eventos usan las consultas para especificar los eventos que proporcionan.

[Los consumidores temporales](receiving-events-for-the-duration-of-your-application.md) aplican consultas en llamadas al método [**IWbemServices::ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) o [**IWbemServices::ExecNotificationQueryAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) [Los consumidores de eventos permanentes](receiving-events-at-all-times.md) coloca consultas en **la propiedad Query** de una instancia de la clase del sistema [**\_ \_ EventFilter.**](--eventfilter.md)

[Los proveedores de](writing-an-event-provider.md) eventos usan consultas de eventos para registrarse y admitir uno o varios tipos de eventos. Coloca consultas en la propiedad **EventQueryList** de una instancia de la clase del sistema [**\_ \_ EventProviderRegistration.**](--eventproviderregistration.md) Todos los proveedores de eventos crean **\_ \_ una instancia de EventProviderRegistration** para registrarse con Windows Management Instrumentation (WMI). Para obtener más información, [vea Registrar un proveedor de eventos.](registering-an-event-provider.md)

Los consumidores y proveedores de eventos usan la instrucción [SELECT](select-statement-for-event-queries.md) y una cláusula WHERE relacionada para las consultas de eventos, además de una variedad de extensiones específicas de la lenguaje de consulta de WMI (WQL). Las extensiones se usan para proteger a los consumidores de que se inunden con notificaciones que se producen con demasiada frecuencia para que sean útiles.

Los consumidores que no requieren notificación cada vez que se produce un evento pueden especificar las cláusulas siguientes en sus consultas:

-   [Cláusula WITHIN](within-clause.md)
-   [Cláusula GROUP](group-clause.md)
-   [Having (cláusula)](having-clause.md)

Las cláusulas WITHIN y HAVING afectan al tiempo de los eventos y la cláusula GROUP hace que se envíe un evento representativo en lugar de un evento que se produce con frecuencia.

 

 



