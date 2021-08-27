---
description: El administrador de control de servicios (SCM) mantiene una base de datos de servicios instalados y servicios de controlador, y proporciona un medio unificado y seguro de controlarlos.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Acerca de los servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58bcd2058ec8f8de5cbe56a521e2d83919a17532c00dab175d93305edd3684d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126485"
---
# <a name="about-services"></a>Acerca de los servicios

El [administrador de control de](service-control-manager.md) servicios (SCM) mantiene una base de datos de servicios instalados y servicios de controlador, y proporciona un medio unificado y seguro de controlarlos. La base de datos incluye información sobre cómo se debe iniciar cada servicio o servicio de controlador. También permite a los administradores del sistema personalizar los requisitos de seguridad de cada servicio y, por tanto, controlar el acceso al servicio.

Los siguientes tipos de programas usan las funciones proporcionadas por el SCM.



| Tipo                          | Descripción                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Programa de servicio               | Programa que proporciona código ejecutable para uno o varios servicios. Los programas de servicio usan funciones que se conectan al SCM y envían información de estado al SCM.                                                                                                                                                                          |
| Programa de configuración de servicio | Programa que consulta o modifica la base de datos de servicios. Los programas de configuración de servicio usan funciones que abren la base de datos, instalan o eliminan servicios en la base de datos, y consultan o modifican los parámetros de configuración y seguridad de los servicios instalados. Los programas de configuración de servicio administran servicios y servicios de controlador. |
| Programa de control de servicios       | Programa que inicia y controla los servicios y los servicios de controlador. Los programas de control de servicio usan funciones que envían solicitudes al SCM, que lleva a cabo la solicitud.                                                                                                                                                                     |



 

En esta introducción se tratan los temas siguientes:

-   [Administrador de control de servicios](service-control-manager.md)
-   [Programas de servicio](service-programs.md)
-   [Programas de configuración de servicio](service-configuration-programs.md)
-   [Programas de control de servicio](service-control-programs.md)
-   [Cuentas de usuario de servicio](service-user-accounts.md)
-   [Servicios interactivos](interactive-services.md)
-   [Seguridad del servicio y derechos de acceso](service-security-and-access-rights.md)
-   [Depuración de un servicio](debugging-a-service.md)
-   [Eventos de desencadenador de servicio](service-trigger-events.md)

 

 



