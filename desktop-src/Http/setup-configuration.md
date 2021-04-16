---
title: Configuración de la instalación
description: La configuración del programa de instalación requiere privilegios de administrador y es persistente en todos los reinicios.
ms.assetid: 96e9c069-829b-4615-b94b-3761bc541440
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b43b543bfc81f963341d7b5f690f4b40312ee420
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104531869"
---
# <a name="setup-configuration"></a>Configuración de la instalación

La configuración del programa de instalación requiere privilegios de administrador y es persistente en todos los reinicios. Normalmente, una aplicación de instalación que se ejecuta con privilegios de administrador lleva a cabo esta configuración persistente durante la instalación para que las aplicaciones puedan ejecutarse con privilegios inferiores, aunque la configuración persistente puede realizarse en cualquier momento. La configuración de la instalación puede incluir cualquiera de las cuatro actividades siguientes:

-   Crear una reserva de direcciones URL. La API HTTP permite a la aplicación de instalación reservar prefijos de dirección URL para las colas de solicitudes asociadas a aplicaciones específicas. Para reservar una dirección URL, la aplicación de instalación llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en **HttpServiceConfigUrlAclInfo** y pasa un puntero en el parámetro *pConfigInformation* a una estructura de [**configuración del \_ servicio HTTP \_ \_ URLACL \_ set**](/windows/desktop/api/Http/ns-http-http_service_config_urlacl_set) que contiene la información de registro. Para obtener más información, vea [reservas de espacio de nombres, registros y enrutamiento](namespace-reservations-registrations-and-routing.md).
-   Configuración de SSL. Para configurar SSL, el administrador llama a la función [**HttpSetServiceConfiguration**](/windows/desktop/api/Http/nf-http-httpsetserviceconfiguration) con el parámetro *ConfigId* establecido en **HttpServiceConfigSSLCertInfo** y pasa un puntero en el parámetro *pConfigInformation* a una estructura de [**\_ \_ \_ \_ conjunto SSL de configuración del servicio http**](/windows/desktop/api/Http/ns-http-http_service_config_ssl_set) que contiene la información del certificado SSL.
-   Establecer otras configuraciones persistentes en todo el servidor HTTP, como las direcciones IP en las que el servidor HTTP escuchará y el valor de tiempo de espera para todo el servidor. Consulte [lista de escucha de IP](ip-listen-list.md) y [**tiempo de \_ \_ espera de configuración \_ \_ del servicio http**](/windows/desktop/api/Http/ns-http-http_service_config_timeout_set).

 

 




