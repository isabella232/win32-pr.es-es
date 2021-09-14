---
description: El administrador de control de servicios (SCM) se inicia en el arranque del sistema. Se trata de un servidor de llamada a procedimiento remoto (RPC), por lo que los programas de configuración de servicio y control de servicios pueden manipular servicios en máquinas remotas.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Administrador de control de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168893"
---
# <a name="service-control-manager"></a>Administrador de control de servicios

El administrador de control de servicios (SCM) se inicia en el arranque del sistema. Se trata de un servidor de llamada a procedimiento remoto (RPC), por lo que los programas de configuración de servicio y control de servicios pueden manipular servicios en máquinas remotas.

Las funciones de servicio proporcionan una interfaz para las siguientes tareas realizadas por el SCM:

-   Mantener la base de datos de los servicios instalados.
-   Iniciar servicios y servicios de controlador al iniciar el sistema o a petición.
-   Enumerar los servicios instalados y los servicios de controlador.
-   Mantener la información de estado para los servicios en ejecución y los servicios de controlador.
-   Transmitir solicitudes de control a servicios en ejecución.
-   Bloqueo y desbloqueo de la base de datos de servicio.

En las secciones siguientes se describe el SCM con más detalle:

-   [Base de datos de servicios instalados](database-of-installed-services.md)
-   [Inicio automático de servicios](automatically-starting-services.md)
-   [Iniciar servicios a petición](starting-services-on-demand.md)
-   [Lista de registros de servicio](service-record-list.md)
-   [Identificadores de SCM](scm-handles.md)

 

 



