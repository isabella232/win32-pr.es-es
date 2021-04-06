---
description: El administrador de control de servicios (SCM) mantiene una base de datos de servicios instalados y servicios de controladores, y proporciona un medio unificado y seguro para controlarlos.
ms.assetid: a3af8340-d367-417b-9759-7282edf1d694
title: Acerca de los servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87aeec6dfcdc4e2dc0cc0ab3ef084b7927b2c3bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002331"
---
# <a name="about-services"></a>Acerca de los servicios

El [Administrador de control de servicios](service-control-manager.md) (SCM) mantiene una base de datos de servicios instalados y servicios de controladores, y proporciona un medio unificado y seguro para controlarlos. La base de datos incluye información sobre cómo se debe iniciar cada servicio o controlador. También permite a los administradores del sistema personalizar los requisitos de seguridad para cada servicio y, por tanto, controlar el acceso al servicio.

Los siguientes tipos de programas usan las funciones proporcionadas por el SCM.



| Tipo                          | Descripción                                                                                                                                                                                                                                                                                                                               |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Programa de servicio               | Programa que proporciona código ejecutable para uno o más servicios. Los programas de servicio usan funciones que se conectan al SCM y envían información de estado al SCM.                                                                                                                                                                          |
| Programa de configuración del servicio | Programa que consulta o modifica la base de datos de servicios. Los programas de configuración de servicio usan funciones que abren la base de datos, instalan o eliminan servicios en la base de datos y consultan o modifican los parámetros de configuración y seguridad para los servicios instalados. Los programas de configuración de servicio administran servicios y servicios de controladores. |
| Programa de control de servicios       | Programa que inicia y controla servicios y servicios de controladores. Los programas de control de servicios usan funciones que envían solicitudes al SCM, que lleva a cabo la solicitud.                                                                                                                                                                     |



 

En esta información general se describen los temas siguientes:

-   [Administrador de control de servicios](service-control-manager.md)
-   [Programas de servicio](service-programs.md)
-   [Programas de configuración de servicio](service-configuration-programs.md)
-   [Programas de control de servicios](service-control-programs.md)
-   [Cuentas de usuario de servicio](service-user-accounts.md)
-   [Servicios interactivos](interactive-services.md)
-   [Derechos de acceso y seguridad del servicio](service-security-and-access-rights.md)
-   [Depuración de un servicio](debugging-a-service.md)
-   [Eventos de desencadenador de servicio](service-trigger-events.md)

 

 



