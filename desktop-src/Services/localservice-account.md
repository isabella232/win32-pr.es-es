---
description: La cuenta LocalService es una cuenta local predefinida que usa el administrador de control de servicios.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Cuenta localService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265012"
---
# <a name="localservice-account"></a>Cuenta localService

La cuenta LocalService es una cuenta local predefinida que usa el administrador de control de servicios. Tiene privilegios mínimos en el equipo local y presenta credenciales anónimas en la red.

Esta cuenta se puede especificar en una llamada a las [**funciones CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) Tenga en cuenta que esta cuenta no tiene una contraseña, por lo que se omite cualquier información de contraseña que proporcione en esta llamada. Aunque el subsistema de seguridad localiza este nombre de cuenta, el SCM no admite nombres localizados. Por lo tanto, recibirá un nombre localizado para esta cuenta de la función [**LookupAccountSid,**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) pero el nombre de la cuenta debe ser NT AUTHORITY LocalService al llamar a \\ **CreateService** o **ChangeServiceConfig,** independientemente de la configuración regional, o se pueden producir resultados inesperados.

El SID de usuario se crea a partir del valor **DE RID DEL SERVICIO LOCAL \_ \_ \_ DE** SEGURIDAD.

La cuenta LocalService tiene su propia subclave en la clave del Registro **HKEY \_ USERS.** Por lo tanto, la clave del Registro **HKEY \_ CURRENT \_ USER** está asociada a la cuenta LocalService.

La cuenta LocalService tiene los siguientes privilegios:

-   **SE \_ ASSIGNPRIMARYTOKEN \_ NAME** (deshabilitado)
-   **SE \_ AUDIT \_ NAME** (deshabilitado)
-   **SE \_ CAMBIAR \_ NOMBRE \_ DE NOTIFICACIÓN** (habilitado)
-   **SE \_ CREATE \_ GLOBAL \_ NAME** (habilitado)
-   **SE \_ IMPERSONATE \_ NAME** (habilitado)
-   **SE \_ INCREASE \_ QUOTA \_ NAME (deshabilitado)**
-   **SE \_ SHUTDOWN \_ NAME (deshabilitado)**
-   **SE \_ UNDOCK \_ NAME (deshabilitado)**
-   Privilegios asignados a usuarios y usuarios autenticados

Para obtener más información, vea [Derechos de acceso y seguridad del servicio.](service-security-and-access-rights.md)

 

 
