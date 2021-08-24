---
title: Configuración del programa de instalación
description: La configuración del programa de instalación requiere privilegios de administrador y es persistente entre reinicios.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36d59065ff34e7998d9df0503f6ae7503d9d402def6053f8176ba5af5b6a9efa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996122"
---
# <a name="setup-configuration"></a>Configuración del programa de instalación

La configuración del programa de instalación requiere privilegios de administrador y es persistente entre reinicios. Normalmente, una aplicación de instalación que se ejecuta con privilegios de administrador realiza esta configuración persistente durante la instalación para que las aplicaciones puedan ejecutarse con privilegios inferiores, aunque la configuración persistente se puede realizar en cualquier momento. La configuración del programa de instalación puede incluir cualquiera de las cuatro actividades siguientes:

-   Creación de una reserva de direcciones URL. La API HTTP permite que la aplicación de instalación reserve prefijos de dirección URL para las colas de solicitudes asociadas a aplicaciones específicas. Para reservar una dirección URL, la aplicación de instalación llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en **HttpServiceConfigUrlAclInfo** y pasa un puntero en el parámetro *pConfigInformation* a una estructura [**HTTP SERVICE CONFIG \_ \_ \_ URLACL \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) que contiene la información de registro. Para obtener más información, vea Reservas, registros y enrutamiento de espacios [de nombres.](namespace-reservations-registrations-and-routing.md)
-   Configuración de SSL. Para configurar SSL, el administrador llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en **HttpServiceConfigSSLCertInfo** y pasa un puntero en el parámetro *pConfigInformation* a una estructura [**HTTP SERVICE CONFIG SSL \_ \_ \_ \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) que contiene la información del certificado SSL.
-   Establecer otras configuraciones persistentes para todo el servidor HTTP, como las direcciones IP en las que el servidor HTTP escuchará y el valor de tiempo de espera de todo el servidor. Consulte [Lista de escucha de IP](ip-listen-list.md) y HTTP SERVICE CONFIG TIMEOUT [**\_ \_ \_ \_ SET**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




