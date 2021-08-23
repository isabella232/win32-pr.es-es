---
title: Configuración del grupo de direcciones URL
description: Configuración del grupo de direcciones URL
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d335af063eb8cadc557db3f01da850b468099866e292bcd5ea2a3af314de8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014913"
---
# <a name="configuring-the-url-group"></a>Configuración del grupo de direcciones URL

El identificador del grupo de direcciones URL se crea con la [**función HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) y se usa en la llamada a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). El *parámetro pPropertyInformation* apunta a la estructura de configuración del tipo de propiedad que se establece. El **parámetro PropertyInformationLength** especifica el tamaño, en bytes, de la estructura de configuración. Por ejemplo, al establecer **HttpServerTimeoutsProperty,** el parámetro *pPropertyInformation* debe apuntar a un búfer que no puede ser menor que la estructura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) Las configuraciones del grupo de direcciones URL se consultan mediante una [**llamada a HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Una vez creado el grupo de direcciones URL, las direcciones URL se agregan al grupo [**con HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). El grupo de direcciones URL debe estar asociado a una cola de solicitudes de la versión 2.0 para recibir solicitudes. Para asociar el grupo de direcciones URL a una cola de solicitudes, la aplicación llama a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) y especifica **HttpServerBindingProperty** en el *parámetro Property.* Si no se establece esta propiedad, las solicitudes correspondientes para el grupo de direcciones URL no se entregan a una cola de solicitudes y la API del servidor HTTP genera una respuesta 503. La aplicación solo puede agregar direcciones URL reservadas previamente con el servicio a un grupo de direcciones URL cuando se ejecuta con pocos privilegios. Para obtener más información, vea el tema [Reservas, registros y](namespace-reservations-registrations-and-routing.md) enrutamiento de espacios de nombres.

 

 




