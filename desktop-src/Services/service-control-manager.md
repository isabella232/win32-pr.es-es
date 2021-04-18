---
description: El administrador de control de servicios (SCM) se inicia en el arranque del sistema. Es un servidor de llamada a procedimiento remoto (RPC), por lo que los programas de configuración de servicio y de control de servicio pueden manipular servicios en equipos remotos.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Administrador de control de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666447"
---
# <a name="service-control-manager"></a>Administrador de control de servicios

El administrador de control de servicios (SCM) se inicia en el arranque del sistema. Es un servidor de llamada a procedimiento remoto (RPC), por lo que los programas de configuración de servicio y de control de servicio pueden manipular servicios en equipos remotos.

Las funciones de servicio proporcionan una interfaz para las siguientes tareas realizadas por el SCM:

-   Mantenimiento de la base de datos de servicios instalados.
-   Iniciar servicios y servicios de controladores al iniciar el sistema o a petición.
-   Enumerar servicios instalados y servicios de controladores.
-   Mantenimiento de la información de estado para la ejecución de servicios y servicios de controladores.
-   Transmisión de solicitudes de control a servicios en ejecución.
-   Bloqueo y desbloqueo de la base de datos de servicio.

En las secciones siguientes se describe con más detalle el SCM:

-   [Base de datos de servicios instalados](database-of-installed-services.md)
-   [Inicio automático de servicios](automatically-starting-services.md)
-   [Inicio de servicios a petición](starting-services-on-demand.md)
-   [Lista de registros de servicio](service-record-list.md)
-   [Identificadores de SCM](scm-handles.md)

 

 



