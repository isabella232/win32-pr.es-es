---
title: Configuración del grupo de direcciones URL
description: .
ms.assetid: be222076-51ff-4907-924f-cc7b0d4fe767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59d9be6969b2b197d0bdcb404ad6b8965c278235
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994418"
---
# <a name="configuring-the-url-group"></a>Configuración del grupo de direcciones URL

El identificador de grupo de direcciones URL se crea con la función [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) y se usa en la llamada a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty). El parámetro *pPropertyInformation* apunta a la estructura de configuración para el tipo de propiedad que se establece. El parámetro **PropertyInformationLength** especifica el tamaño, en bytes, de la estructura de configuración. Por ejemplo, al establecer **HttpServerTimeoutsProperty** , el parámetro *pPropertyInformation* debe apuntar a un búfer que no puede ser menor que la estructura de [**\_ \_ \_ información de límite de tiempo de espera de http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) . Las configuraciones de grupo de direcciones URL se consultan llamando a [**HttpQueryUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpqueryurlgroupproperty).

Una vez creado el grupo de direcciones URL, las direcciones URL se agregan al grupo con [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup). El grupo de direcciones URL debe estar asociado a una cola de solicitudes de la versión 2,0 para recibir solicitudes. Para asociar el grupo de direcciones URL a una cola de solicitudes, la aplicación llama a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) y especifica **HttpServerBindingProperty** en el parámetro *Property* . Si no se establece esta propiedad, las solicitudes coincidentes para el grupo de direcciones URL no se entregan a una cola de solicitudes y la API del servidor HTTP genera una respuesta 503. La aplicación solo puede agregar direcciones URL que se han reservado previamente con el servicio a un grupo de direcciones URL cuando se ejecuta con privilegios bajos. Para obtener más información, vea el tema [reservas de espacio de nombres, registros y enrutamiento](namespace-reservations-registrations-and-routing.md) .

 

 




