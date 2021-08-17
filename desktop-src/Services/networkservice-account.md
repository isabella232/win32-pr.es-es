---
description: La cuenta NetworkService es una cuenta local predefinida que usa el administrador de control de servicios.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Cuenta de NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f8256a15b43d9a9c0403067a61f9a7cbf6b9d2df0d78936c4d9c06f6dfd87c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889399"
---
# <a name="networkservice-account"></a>Cuenta de NetworkService

La cuenta NetworkService es una cuenta local predefinida que usa el administrador de control de servicios. El subsistema de seguridad no reconoce esta cuenta, por lo que no puede especificar su nombre en una llamada a la [**función LookupAccountName.**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) Tiene privilegios mínimos en el equipo local y actúa como equipo en la red.

Esta cuenta se puede especificar en una llamada a las [**funciones CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**ChangeServiceConfig.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) Tenga en cuenta que esta cuenta no tiene una contraseña, por lo que se omite cualquier información de contraseña que proporcione en esta llamada. Aunque el subsistema de seguridad localiza este nombre de cuenta, el SCM no admite nombres localizados. Por lo tanto, recibirá un nombre localizado para esta cuenta de la función [**LookupAccountSid,**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) pero el nombre de la cuenta debe ser NT AUTHORITY NetworkService al llamar a \\ **CreateService** o **ChangeServiceConfig,** independientemente de la configuración regional, o se pueden producir resultados inesperados.

Un servicio que se ejecuta en el contexto de la cuenta NetworkService presenta las credenciales del equipo a los servidores remotos. De forma predeterminada, el token remoto contiene SID para los grupos Todos y Usuarios autenticados. El SID de usuario se crea a partir del valor **DE RID DEL SERVICIO DE RED \_ \_ \_ DE** SEGURIDAD.

La cuenta NetworkService tiene su propia subclave en la clave del Registro **HKEY \_ USERS.** Por lo tanto, la clave del Registro **HKEY \_ CURRENT \_ USER** está asociada a la cuenta networkService.

La cuenta NetworkService tiene los siguientes privilegios:

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

 

 
