---
description: Tipos de aplicaciones COM+
ms.assetid: 4b731f22-6837-4c03-9c8c-a76451369cf1
title: Tipos de aplicaciones COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb365863ee2b2fbe41997facdf21d84866af1f6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361598"
---
# <a name="types-of-com-applications"></a>Tipos de aplicaciones COM+

Estos son los cuatro tipos básicos de aplicaciones COM+:

-   **Aplicaciones de servidor.** Una aplicación de *servidor* COM+ se ejecuta en su propio proceso. Las aplicaciones de servidor pueden admitir todos los servicios COM+.
-   **Aplicaciones de biblioteca.** Una aplicación de *biblioteca* COM+ se ejecuta en el proceso del cliente que la crea. Más concretamente, los componentes de una aplicación de biblioteca siempre se cargan en el proceso del creador. Las aplicaciones de biblioteca no están asociadas explícitamente a un proceso de servidor. Pueden usar la seguridad basada en roles, pero no admiten el acceso remoto ni los componentes en cola.
-   **Servidores proxy de aplicación.** Un *proxy de* aplicación es un conjunto de archivos que contienen información de registro que permite a un cliente acceder de forma remota a una aplicación de servidor. Cuando se ejecuta en un equipo cliente, un archivo proxy de aplicación escribe información sobre la aplicación de servidor COM+, incluidos CLSID, ProgID, RemoteServerName e información de serialización, en el equipo cliente. A continuación, se puede acceder a la aplicación de servidor de forma remota desde el equipo cliente.
-   **Aplicaciones preinstaladas de COM+.** COM+ incluye un conjunto de aplicaciones preinstaladas que controlan funciones internas. Las aplicaciones preinstaladas se muestran en la carpeta Aplicaciones COM+ de la herramienta administrativa Servicios de componentes, pero no se pueden modificar ni eliminar. Estas aplicaciones incluyen lo siguiente:
    -   Utilidades de .NET
    -   Aplicación de control Publisher analizador
    -   Explorador de COM+
    -   Agente de escucha de cola de mensajes no enviados de COM+ QC
    -   Utilidades com+
    -   Aplicaciones In-Process IIS
    -   Aplicaciones agrupadas fuera de proceso de IIS
    -   Aplicación del sistema

## <a name="notes"></a>Notas

A partir Windows Server 2003, es posible ejecutar aplicaciones COM+ incluso si la aplicación del sistema está deshabilitada. Las aplicaciones COM+ se ejecutarán, aunque sin los servicios que normalmente proporciona la aplicación del sistema. Estos servicios incluyen el uso de la herramienta administrativa Servicios de componentes y el seguimiento de eventos del sistema.

Además, a Windows Server 2003, la funcionalidad de autenticación de la aplicación del sistema COM+ incluye el valor EOAC \_ DISABLE \_ AAA. Este valor, que deshabilita las activaciones de activación como activador (AAA), se usa con la [**función CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) al iniciar la aplicación del sistema. Establecer la funcionalidad de autenticación en EOAC DISABLE AAA permite que una aplicación que se ejecuta con una cuenta con privilegios \_ (como LocalSystem) ayude a evitar que su identidad se utilice para iniciar componentes que no son de \_ confianza.

 

 
