---
description: La cuenta LocalService es una cuenta local predefinida utilizada por el administrador de control de servicios.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Cuenta LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546515"
---
# <a name="localservice-account"></a>Cuenta LocalService

La cuenta LocalService es una cuenta local predefinida utilizada por el administrador de control de servicios. Tiene privilegios mínimos en el equipo local y presenta credenciales anónimas en la red.

Esta cuenta puede especificarse en una llamada a las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Tenga en cuenta que esta cuenta no tiene contraseña, por lo que se omite cualquier información de contraseña que proporcione en esta llamada. Aunque el subsistema de seguridad localiza este nombre de cuenta, el SCM no admite nombres localizados. Por lo tanto, recibirá un nombre traducido para esta cuenta desde la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , pero el nombre de la cuenta debe ser NT Authority \\ LocalService cuando llame a **CreateService** o **ChangeServiceConfig**, independientemente de la configuración regional, o se puedan producir resultados inesperados.

El SID de usuario se crea a partir del valor de **\_ \_ \_ RID del servicio local de seguridad** .

La cuenta LocalService tiene su propia subclave en la clave del registro **HKEY \_ users** . Por lo tanto, la clave del registro del **\_ \_ usuario actual HKEY** está asociada a la cuenta LocalService.

La cuenta LocalService tiene los siguientes privilegios:

-   **Se \_ \_Nombre de ASSIGNPRIMARYTOKEN** (deshabilitado)
-   **Se \_ \_Nombre de auditoría** (deshabilitado)
-   **Se \_ CAMBIAR \_ \_ el nombre** de la notificación (habilitado)
-   **Se \_ CREAR \_ \_ nombre global** (habilitado)
-   **Se \_ \_Nombre de SUplantación** (habilitado)
-   **Se \_ AUMENTAR \_ \_ el nombre** de la cuota (deshabilitado)
-   **Se \_ \_Nombre de apagado** (deshabilitado)
-   **Se \_ \_Nombre de desacoplamiento** (deshabilitado)
-   Cualquier privilegio asignado a usuarios y usuarios autenticados

Para obtener más información, consulte [seguridad del servicio y derechos de acceso](service-security-and-access-rights.md).

 

 
