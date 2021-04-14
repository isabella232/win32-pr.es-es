---
description: Explica el uso de tokens de suplantación en el control de acceso.
ms.assetid: 74fcb0e3-303a-4a5e-9eb6-2aad3a4944db
title: Tokens de suplantación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f468a4c7a9c6ff04a4481ffe7347e227a447db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668399"
---
# <a name="impersonation-tokens"></a>Tokens de suplantación

Un subproceso de suplantación tiene dos [*tokens de acceso*](/windows/desktop/SecGloss/a-gly):

-   Un [*token de acceso principal*](/windows/desktop/SecGloss/p-gly) que describe el [*contexto de seguridad*](/windows/desktop/SecGloss/s-gly) del servidor. Para obtener un identificador de este token, llame a la función [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken) .
-   Token de acceso de suplantación que describe el contexto de seguridad del cliente que se va a suplantar. Para obtener un identificador de este token, llame a la función [**OpenThreadToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthreadtoken) .

Un servidor puede utilizar el [*token de suplantación*](/windows/desktop/SecGloss/i-gly) en las siguientes funciones:

-   En las funciones [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck), [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype)y [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar si un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) permite al cliente un conjunto de derechos de acceso.
-   En la función [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar o deshabilitar los privilegios del cliente.
-   En la función [**PrivilegeCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar si un conjunto de privilegios está habilitado en el token del cliente.
-   En las funciones que generan entradas en el registro de eventos de seguridad, como [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma) o [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma). Estas funciones usan un token de suplantación para obtener información sobre el cliente para la entrada de registro.

 

 
