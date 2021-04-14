---
description: Los consumidores de eventos temporales, los consumidores de eventos permanentes y los proveedores de eventos usan las consultas de eventos. Los consumidores de eventos usan consultas de eventos para especificar los eventos de interés y los proveedores de eventos usan las consultas para especificar los eventos que proporcionan.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Recibir notificaciones de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648282"
---
# <a name="receiving-event-notifications"></a>Recibir notificaciones de eventos

Los consumidores de eventos temporales, los consumidores de eventos permanentes y los proveedores de eventos usan las consultas de eventos. Los consumidores de eventos usan consultas de eventos para especificar los eventos de interés y los proveedores de eventos usan las consultas para especificar los eventos que proporcionan.

Los [consumidores temporales](receiving-events-for-the-duration-of-your-application.md) colocan consultas en llamadas al método [**IWbemServices:: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) o [**IWbemServices:: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) . Los [consumidores de eventos permanentes](receiving-events-at-all-times.md) colocan consultas en la propiedad de **consulta** de una instancia de la clase del sistema [**\_ \_ EventFilter**](--eventfilter.md) .

Los [proveedores de eventos](writing-an-event-provider.md) usan consultas de eventos para registrarse para admitir uno o varios tipos de eventos. Las consultas se colocan en la propiedad **EventQueryList** de una instancia de la clase del sistema [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Todos los proveedores de eventos crean una instancia de **\_ \_ EventProviderRegistration** para registrarse con instrumental de administración de Windows (WMI). Para obtener más información, vea [registrar un proveedor de eventos](registering-an-event-provider.md).

Los consumidores y proveedores de eventos usan la [instrucción SELECT](select-statement-for-event-queries.md) y una cláusula WHERE relacionada para las consultas de eventos, además de una variedad de extensiones específicas del lenguaje de consulta de WMI (WQL). Las extensiones se utilizan para proteger a los consumidores de la saturación con notificaciones que se producen con demasiada frecuencia para ser útiles.

Los consumidores que no requieren notificación cada vez que se produce un evento pueden especificar las siguientes cláusulas en sus consultas:

-   Cláusula [Within](within-clause.md)
-   [Group](group-clause.md) (cláusula)
-   Cláusula [having](having-clause.md)

Las cláusulas dentro de y HAVING afectan al tiempo de los eventos, y la cláusula GROUP hace que se envíe un evento representativo en lugar de un evento que se produce con frecuencia.

 

 



