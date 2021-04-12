---
title: Infraestructura para la administración de servicios hospedados
description: Administración remota de Windows 2,0 (WinRM) incorpora un marco de hospedaje. Para usar el marco de trabajo, se escriben complementos de WinRM que exponen los datos de administración de una aplicación dentro de la infraestructura de WinRM.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8439aca1f36d2d0c2cebb6ed3111aeaa2e4fcee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357696"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infraestructura para la administración de servicios hospedados

Administración remota de Windows 2,0 (WinRM) incorpora un marco de hospedaje. Para usar el marco de trabajo, se escriben complementos de WinRM que exponen los datos de administración de una aplicación dentro de la infraestructura de WinRM. Se admiten dos modelos de hospedaje. Una es Internet Information Services (IIS) â € "basada y la otra es WinRMâ €" basada en el servicio. El modelo basado en WinRM utiliza HTTP.sys y no depende de IIS.

En las secciones siguientes se describen los modelos de hospedaje:

-   [Modelo de hospedaje de la extensión IIS de WinRM](#winrm-iis-extension-hosting-model)
    -   [Equilibrio de carga en el modelo de hospedaje de la extensión IIS de WinRM](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [Redirección HTTP en el modelo de hospedaje de la extensión IIS de WinRM](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [Modelo de hospedaje del servicio WinRM](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Modelo de hospedaje de la extensión IIS de WinRM

El módulo de extensión WinRM IIS es un componente opcional que se instala mediante el **Administrador del servidor**. El módulo de extensión WinRM de IIS se usa para crear puntos de conexión habilitados para WinRMâ € desde dentro del servicio IIS. Este módulo se puede habilitar en el nivel de sitio web o directorio virtual. Funciona interceptando y redirigiendo las solicitudes entrantes al sitio web o directorio virtual asociado. Las solicitudes se redirigen a un módulo WinRM que analiza el contenido y, a continuación, determina qué complemento WinRM está configurado para controlar cada solicitud. Para obtener más información, consulte [configuración del complemento de host de IIS](iis-host-plug-in-configuration.md).

El modelo de hospedaje de la extensión IIS de WinRM está diseñado para controlar un gran volumen de solicitudes. Si se usa el modelo basado en IIS como el marco de trabajo de hospedaje, están disponibles las siguientes características:

-   Los módulos de autenticación de IIS estándar.
-   El proceso del grupo de aplicaciones de IIS para hospedar todos los complementos.
-   Administración de cuotas para la limitación de usuarios intensivos del sistema. Para obtener más información, vea [Administración de cuotas para shells remotos](quotas.md).
-   Un modelo de complemento de Shell. Vea [API del shell de cliente de WinRM](client-shell-api.md).
-   Un modelo de autorización flexible. Consulte [API de complementos de WinRM](winrm-plugin-api.md).

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Equilibrio de carga en el modelo de hospedaje de la extensión IIS de WinRM

La mayoría de los equilibradores de carga (libras) admiten un modelo de adherencia basado en cookies. Las LB insertan una cookie en la respuesta a la primera solicitud del cliente. En todas las solicitudes posteriores, la cookie se transmite en la solicitud y la LB usa la cookie para enrutar la solicitud al servidor adecuado.

En entornos en los que WinRM 2,0 se hospeda tras un LB, los LB deben configurarse para que el prefijo MS-WSMAN sea el nombre de la cookie. Además, los LB deben configurarse para permitir que la cookie sea infinita, ya que el cliente WinRM debe controlar cuánto tiempo es válida la cookie.

El siguiente es un ejemplo de un nombre de cookie:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>Redirección HTTP en el modelo de hospedaje de la extensión IIS de WinRM

WinRM 2,0 puede controlar el redireccionamiento HTTP. Se recomienda que todos los redireccionamientos utilicen Capa de sockets seguros (SSL) y que todas las aplicaciones validen el URI Redirigido antes de crear una nueva sesión.

## <a name="winrm-service-hosting-model"></a>Modelo de hospedaje del servicio WinRM

El modelo basado en el servicio WinRM se ejecuta sobre HTTP.sys. El servicio WinRM es un servicio orientado a la red que controla las solicitudes de los clientes de WinRM. El servicio determina si la solicitud se enruta a un complemento que se ejecuta en el servicio principal o se enruta a través de un host donde se ejecuta el complemento de terceros. Este modelo está pensado para escenarios en los que la carga en el nodo administrado es baja. Además, este modelo está pensado para escenarios en los que el hospedaje de IIS no es una opción. Para obtener más información, consulte [configuración del complemento de servicio WinRM](wsman-service-plug-in-configuration.md).

 

 




