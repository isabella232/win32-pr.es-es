---
title: Configuración de la sesión de servidor
description: Configuración de la sesión de servidor
ms.assetid: 1e4e9440-8d70-44df-90a7-2d5e25b2f680
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d41c1606cce397c49a15c62dae10531edfde93f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090943"
---
# <a name="configuring-the-server-session"></a>Configuración de la sesión de servidor

El identificador de sesión del servidor se crea con la [**función HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) y se usa en la llamada a [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty). El *parámetro pPropertyInformation* apunta a la estructura de configuración del tipo de propiedad que se establece. El *parámetro PropertyInformationLength* especifica el tamaño, en bytes, de la estructura de configuración. Por ejemplo, al establecer **HttpServerTimeoutsProperty,** el parámetro **pPropertyInformation** debe apuntar a un búfer que sea al menos el tamaño de la estructura [**HTTP TIMEOUT LIMIT \_ \_ \_ INFO.**](/windows/desktop/api/Http/ns-http-http_timeout_limit_info)

Normalmente, una aplicación HTTP crea una sesión de servidor único y puede establecer propiedades para toda la aplicación, como el límite de ancho de banda global o habilitar el registro centralizado en esta sesión de servidor. [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty) invalida las configuraciones de LA API del servidor HTTP para la aplicación que realiza la llamada; no afecta a las propiedades de la API del servidor HTTP. Las configuraciones de sesión del servidor se consultan mediante una llamada [**a HttpQueryServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpqueryserversessionproperty).

 

 




