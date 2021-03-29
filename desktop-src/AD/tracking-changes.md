---
title: Seguimiento de cambios
description: Algunas aplicaciones deben mantener la coherencia entre los datos específicos almacenados en el servicio de directorio de Active Directory y otros datos.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, seguimiento de cambios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dc772f883b97eb4e7305b39f0a582448a8bc021
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995054"
---
# <a name="tracking-changes"></a>Seguimiento de cambios

Algunas aplicaciones deben mantener la coherencia entre los datos específicos almacenados en el servicio de directorio de Active Directory y otros datos. Los demás datos se pueden almacenar en el directorio, en una tabla de SQL Server, en un archivo o en el registro. Cuando cambian los datos almacenados en el directorio, es posible que sea necesario cambiar el resto de los datos para mantener la coherencia. Las aplicaciones que tienen este requisito incluyen:

En esta sección no se tratan los mecanismos que usan las aplicaciones de supervisión. Se trata de aplicaciones que supervisan los cambios de directorio no con el fin de mantener datos coherentes entre almacenes independientes, pero como una herramienta de administración del sistema. Aunque las aplicaciones de supervisión pueden usar los mismos mecanismos que admiten las aplicaciones de seguimiento de cambios, los siguientes mecanismos están diseñados específicamente para supervisar aplicaciones:

-   Auditoría de seguridad. Al modificar la parte de la lista de control de acceso de sistema (SACL) de un descriptor de seguridad de objeto, puede hacer que los accesos al objeto de un controlador de dominio determinado generen registros de auditoría en el registro de eventos de seguridad de ese DC. Puede auditar lecturas, escrituras o ambas cosas. puede auditar todo el objeto o atributos específicos. Para obtener más información, vea [recuperar la SACL de un objeto y la generación de](retrieving-an-objectampaposs-sacl.md) [Auditoría](/windows/desktop/SecAuthZ/audit-generation).
-   Registros de eventos. Al modificar la configuración del registro en un controlador de dominio determinado, puede cambiar los tipos de eventos registrados en el registro de eventos del servicio de directorio. En concreto, para registrar todas las modificaciones, establezca el valor **8 de acceso al directorio** en la siguiente clave del registro en 4.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Para obtener más información, vea [registro de eventos](/windows/desktop/EventLog/event-logging).

-   Seguimiento de eventos. Windows 2000 presentó una API de seguimiento de eventos para el seguimiento y el registro de eventos interesantes en software o hardware. El sistema operativo Windows, y Active Directory Domain Services en particular, admiten el uso del seguimiento de eventos para el planeamiento de la capacidad y el análisis detallado del rendimiento. Para obtener más información, vea [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) y [seguimiento de eventos en ADSI](/windows/desktop/ADSI/adsi-and-etw).

Esta sección contiene los siguientes temas:

-   [Información general sobre las técnicas de Change Tracking](overview-of-change-tracking-techniques.md)
-   [Notificaciones de cambio en Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Sondear los cambios mediante el control DirSync](polling-for-changes-using-the-dirsync-control.md)
-   [Sondeo de cambios mediante USNChanged](polling-for-changes-using-usnchanged.md)

 

 