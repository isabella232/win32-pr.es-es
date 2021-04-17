---
description: Tipos de aplicaciones COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Tipos de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686442"
---
# <a name="types-of-com-applications"></a>Tipos de aplicaciones COM+

A continuación se muestran los cuatro tipos básicos de aplicaciones COM+:

-   **Aplicaciones de servidor.** Una *aplicación de servidor* com+ se ejecuta en su propio proceso. Las aplicaciones de servidor pueden admitir todos los servicios COM+.
-   **Aplicaciones de biblioteca.** Una *aplicación de biblioteca* com+ se ejecuta en el proceso del cliente que la crea. Más concretamente, los componentes de una aplicación de biblioteca siempre se cargan en el proceso del creador. Las aplicaciones de biblioteca no están asociadas explícitamente a un proceso de servidor. Pueden utilizar la seguridad basada en roles pero no admiten el acceso remoto o los componentes en cola.
-   **Proxies de aplicación.** Un *proxy de aplicación* es un conjunto de archivos que contiene información de registro que permite a un cliente acceder de forma remota a una aplicación de servidor. Cuando se ejecuta en un equipo cliente, un archivo de proxy de aplicación escribe información acerca de la aplicación de servidor COM+, incluidos los CLSID, ProgID, RemoteServerName e información de serialización, en el equipo cliente. A continuación, se puede tener acceso a la aplicación de servidor de forma remota desde el equipo cliente.
-   **Aplicaciones com+ preinstaladas**. COM+ incluye un conjunto de aplicaciones preinstaladas que controlan las funciones internas. Las aplicaciones preinstaladas se muestran en la carpeta aplicaciones COM+ de la herramienta administrativa Servicios de componentes, pero no se pueden modificar ni eliminar. Entre estas aplicaciones se incluyen las siguientes:
    -   Utilidades de .NET
    -   Aplicación de publicador de control de analizador
    -   Explorador COM+
    -   Agente de escucha de cola de mensajes con problemas de entrega COM+
    -   Utilidades COM+
    -   Aplicaciones de In-Process IIS
    -   Aplicaciones agrupadas fuera de proceso de IIS
    -   Aplicación del sistema

## <a name="notes"></a>Notas

A partir de Windows Server 2003, es posible ejecutar aplicaciones COM+ aunque la aplicación del sistema esté deshabilitada. Las aplicaciones COM+ se ejecutarán, pero sin los servicios que normalmente proporciona la aplicación del sistema. Estos servicios incluyen el uso de la herramienta administrativa Servicios de componentes y el seguimiento de eventos del sistema.

También a partir de Windows Server 2003, la capacidad de autenticación para la aplicación del sistema COM+ incluye el valor EOAC \_ Disable \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se usa con la función [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la capacidad de autenticación en EOAC \_ deshabilitar \_ AAA permite que una aplicación que se ejecuta en una cuenta con privilegios (como LocalSystem) ayude a evitar que se use su identidad para iniciar componentes que no son de confianza.

 

 
