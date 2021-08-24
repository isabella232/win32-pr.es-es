---
title: Infraestructura para administrar servicios hospedados
description: Windows Administración remota 2.0 (WinRM) presenta un marco de hospedaje. Para usar el marco, se escriben complementos de WinRM que exponen los datos de administración de una aplicación dentro de la infraestructura de WinRM.
ms.assetid: 924dcc70-9a29-45a6-99a2-5681235e4574
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa41f7952867a121b8a4bd4847cb90ca42dafac346398954afbd5e4dc8bdf43e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795275"
---
# <a name="infrastructure-for-managing-hosted-services"></a>Infraestructura para administrar servicios hospedados

Windows Administración remota 2.0 (WinRM) presenta un marco de hospedaje. Para usar el marco, se escriben complementos de WinRM que exponen los datos de administración de una aplicación dentro de la infraestructura de WinRM. Se admiten dos modelos de hospedaje. Una se Internet Information Services (IIS)â€", y la otra está basada en el servicio WinRMâ€". El modelo basado en WinRM usa HTTP.sys y no depende de IIS.

En las secciones siguientes se describen los modelos de hospedaje:

-   [Modelo de hospedaje de extensiones iis de WinRM](#winrm-iis-extension-hosting-model)
    -   [Equilibrio de carga en el modelo de hospedaje de extensiones iis de WinRM](#load-balancing-in-the-winrm-iis-extension-hosting-model)
    -   [Redireccionamiento HTTP en el modelo de hospedaje de extensiones iis de WinRM](#http-redirection-in-the-winrm-iis-extension-hosting-model)
-   [Modelo de hospedaje del servicio WinRM](#winrm-service-hosting-model)

## <a name="winrm-iis-extension-hosting-model"></a>Modelo de hospedaje de extensiones iis de WinRM

El módulo de extensión de IIS de WinRM es un componente opcional que se instala mediante el **Administrador del servidor**. El módulo de extensión de IIS de WinRM se usa para crear puntos de conexión habilitados para WinRM desde el servicio IIS. Este módulo se puede habilitar en el nivel de sitio web o directorio virtual. Funciona interceptando y redirijando las solicitudes entrantes al sitio web o directorio virtual asociado. Las solicitudes se redirigen a un módulo de WinRM que analiza el contenido y, a continuación, determina qué complemento de WinRM está configurado para controlar cada solicitud. Para obtener más información, vea [Configuración del complemento de host de IIS.](iis-host-plug-in-configuration.md)

El modelo de hospedaje de extensiones de IIS de WinRM está diseñado para controlar un gran volumen de solicitudes. Si el modelo basado en IIS se usa como marco de hospedaje, están disponibles las siguientes características:

-   Módulos de autenticación estándar de IIS.
-   Proceso del grupo de aplicaciones de IIS para hospedar todos los complementos.
-   Administración de cuotas para la limitación de usuarios pesados del sistema. Para obtener más información, vea [Administración de cuotas para Shells remotos.](quotas.md)
-   Un modelo de complemento de shell. Consulte [Api de Shell de cliente de WinRM.](client-shell-api.md)
-   Un modelo de autorización flexible. Consulte [Api de complemento WinRM.](winrm-plugin-api.md)

### <a name="load-balancing-in-the-winrm-iis-extension-hosting-model"></a>Equilibrio de carga en el modelo de hospedaje de extensiones iis de WinRM

La mayoría de los equilibradores de carga (LB) admiten un modelo de stickiness basado en cookies. El lb inserta una cookie en la respuesta a la primera solicitud del cliente. Para todas las solicitudes posteriores, la cookie se transmite en la solicitud y el agente de carga usa la cookie para enrutar la solicitud al servidor adecuado.

En entornos en los que WinRM 2.0 se hospeda detrás de un LB, el lb debe configurarse para que antefija MS-WSMAN al nombre de la cookie. Además, el lb debe configurarse para permitir que la duración de la cookie sea infinita, ya que el cliente winRM debe controlar cuánto tiempo es válida la cookie.

A continuación se muestra un ejemplo de un nombre de cookie:

``` syntax
MS-WSMAN=2046820362.20480.0000; path=/
```

### <a name="http-redirection-in-the-winrm-iis-extension-hosting-model"></a>Redireccionamiento HTTP en el modelo de hospedaje de extensiones iis de WinRM

WinRM 2.0 puede controlar el redireccionamiento HTTP. Se recomienda que todos los redireccionamientos usen Capa de sockets seguros (SSL) y que todas las aplicaciones validen el URI redirigido antes de crear una nueva sesión.

## <a name="winrm-service-hosting-model"></a>Modelo de hospedaje del servicio WinRM

El modelo basado en el servicio WinRM se ejecuta sobre HTTP.sys. El servicio WinRM es un servicio orientado a la red que controla las solicitudes de los clientes de WinRM. El servicio determina si la solicitud se enruta a un complemento que se ejecuta en el servicio principal o se enruta a través de un host donde se ejecuta el complemento de terceros. Este modelo está pensado para escenarios en los que la carga en el nodo administrado es baja. Además, este modelo está pensado para escenarios en los que el hospedaje de IIS no es una opción. Para más información, consulte Configuración del complemento de [servicio winRM.](wsman-service-plug-in-configuration.md)

 

 




