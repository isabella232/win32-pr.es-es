---
description: La cuenta NetworkService es una cuenta local predefinida utilizada por el administrador de control de servicios.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Cuenta NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668293"
---
# <a name="networkservice-account"></a>Cuenta NetworkService

La cuenta NetworkService es una cuenta local predefinida utilizada por el administrador de control de servicios. El subsistema de seguridad no reconoce esta cuenta, por lo que no puede especificar su nombre en una llamada a la función [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) . Tiene los privilegios mínimos en el equipo local y actúa como el equipo de la red.

Esta cuenta puede especificarse en una llamada a las funciones [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) y [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) . Tenga en cuenta que esta cuenta no tiene contraseña, por lo que se omite cualquier información de contraseña que proporcione en esta llamada. Aunque el subsistema de seguridad localiza este nombre de cuenta, el SCM no admite nombres localizados. Por lo tanto, recibirá un nombre traducido para esta cuenta desde la función [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , pero el nombre de la cuenta debe ser NT Authority \\ NetworkService cuando llame a **CreateService** o **ChangeServiceConfig**, independientemente de la configuración regional, o se puedan producir resultados inesperados.

Un servicio que se ejecuta en el contexto de la cuenta NetworkService presenta las credenciales del equipo a los servidores remotos. De forma predeterminada, el token remoto contiene los SID para los grupos todos y usuarios autenticados. El SID de usuario se crea a partir del valor de **RID del servicio de red de seguridad \_ \_ \_** .

La cuenta NetworkService tiene su propia subclave en la clave del registro **HKEY \_ users** . Por lo tanto, la clave del registro del **\_ \_ usuario actual HKEY** está asociada a la cuenta NetworkService.

La cuenta NetworkService tiene los siguientes privilegios:

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

 

 
