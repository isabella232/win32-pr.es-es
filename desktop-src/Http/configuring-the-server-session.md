---
title: Configurar la sesión de servidor
description: .
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcf069b22992fa178798c7f28545e30217d0dada
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685474"
---
# <a name="configuring-the-server-session"></a>Configurar la sesión de servidor

El identificador de sesión de servidor se crea con la función [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) y se utiliza en la llamada a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). El parámetro *pPropertyInformation* apunta a la estructura de configuración para el tipo de propiedad que se establece. El parámetro *PropertyInformationLength* especifica el tamaño, en bytes, de la estructura de configuración. Por ejemplo, al establecer **HttpServerTimeoutsProperty** , el parámetro **pPropertyInformation** debe apuntar a un búfer que tenga al menos el tamaño de la estructura de [**\_ \_ \_ información de límite de tiempo de espera de http**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info) .

Normalmente, una aplicación HTTP crea una única sesión de servidor y puede establecer propiedades de toda la aplicación, como el límite de ancho de banda global o habilitar el registro centralizado en esta sesión de servidor. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) invalida las configuraciones de la API del servidor http para la aplicación que realiza la llamada. no afecta a las propiedades para toda la API del servidor HTTP. Las configuraciones de sesión de servidor se consultan llamando a [**HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




