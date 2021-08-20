---
title: Seguimiento de cambios
description: Algunas aplicaciones deben mantener la coherencia entre datos específicos almacenados en Active Directory servicio de directorio y otros datos.
ms.assetid: f4539482-1170-4c0c-b817-b39e58049d39
ms.tgt_platform: multiple
keywords:
- Active Directory,using,tracking changes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3d8521fbd7b04d2c317246d81e0b9af7bce888bcc8e78b7bc9fcbbdd05b0c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024573"
---
# <a name="tracking-changes"></a>Seguimiento de cambios

Algunas aplicaciones deben mantener la coherencia entre datos específicos almacenados en Active Directory servicio de directorio y otros datos. Los demás datos se pueden almacenar en el directorio, en una SQL Server, en un archivo o en el Registro. Cuando cambian los datos almacenados en el directorio, es posible que los demás datos deban cambiar para mantener la coherencia. Las aplicaciones que tienen este requisito incluyen:

En esta sección no se cubren los mecanismos usados por las aplicaciones de supervisión. Se trata de aplicaciones que supervisan los cambios de directorio no con el fin de mantener datos coherentes entre almacenes independientes, sino como una herramienta de administración del sistema. Aunque las aplicaciones de supervisión pueden usar los mismos mecanismos que admiten aplicaciones de seguimiento de cambios, los siguientes mecanismos están diseñados específicamente para supervisar aplicaciones:

-   Auditoría de seguridad. Al modificar la parte de la lista de control de acceso del sistema (SACL) de un descriptor de seguridad de objetos, puede hacer que los accesos al objeto en un controlador de dominio determinado generen registros de auditoría en el registro de eventos de seguridad en ese controlador de dominio. Puede auditar lecturas, escrituras o ambas cosas; puede auditar todo el objeto o atributos específicos. Para obtener más información, [vea Recuperar la SACL](retrieving-an-objectampaposs-sacl.md) y la generación [de auditoría de un objeto](/windows/desktop/SecAuthZ/audit-generation).
-   Registros de eventos. Al modificar la configuración del Registro en un controlador de dominio determinado, puede cambiar los tipos de eventos registrados en el registro de eventos del servicio de directorio. En concreto, para registrar todas las modificaciones, establezca el valor **8 de Acceso a directorios** en la siguiente clave del Registro en 4.

    ```
    HKEY_LOCAL_MACHINE
       SYSTEM
          CurrentControlSet
             Services
                NTDS
                   Diagnostics
    ```

    Para obtener más información, vea [Registro de eventos.](/windows/desktop/EventLog/event-logging)

-   Seguimiento de eventos. Windows 2000 introdujo una API de seguimiento de eventos para el seguimiento y el registro de eventos interesantes en software o hardware. El Windows operativo y, en Active Directory Domain Services, admiten el uso del seguimiento de eventos para el planeamiento de la capacidad y el análisis detallado del rendimiento. Para obtener más información, vea [Seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) y Seguimiento de eventos en [ADSI.](/windows/desktop/ADSI/adsi-and-etw)

Esta sección contiene los siguientes temas:

-   [Introducción a Change Tracking técnicas](overview-of-change-tracking-techniques.md)
-   [Notificaciones de cambio en Active Directory Domain Services](change-notifications-in-active-directory-domain-services.md)
-   [Sondeo de cambios mediante el control DirSync](polling-for-changes-using-the-dirsync-control.md)
-   [Sondeo de cambios mediante USNChanged](polling-for-changes-using-usnchanged.md)

 

 