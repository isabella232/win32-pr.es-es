---
description: El derecho \_ de acceso ACCESS SYSTEM SECURITY controla la capacidad de obtener o establecer la \_ SACL en un descriptor de seguridad de objetos. El sistema concede este derecho de acceso si el SE security name está habilitado en el token de acceso \_ \_ del subproceso solicitante.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Derecho de acceso sacl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88256664db25c6e906f3b4ca0459217a29d0cc7c0e2dd544c1cf198bc24fff5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780520"
---
# <a name="sacl-access-right"></a>Derecho de acceso sacl

El derecho de acceso ACCESS SYSTEM SECURITY controla la capacidad de obtener \_ \_ o establecer la SACL en el descriptor de seguridad [*de un objeto*](/windows/desktop/SecGloss/s-gly). El sistema concede este derecho de acceso solo si el SE security name está habilitado en el token de acceso \_ \_ del subproceso solicitante. [](/windows/desktop/SecGloss/a-gly)

**Para acceder a la SACL de un objeto**

1.  Llame a [**la función AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para habilitar el SE \_ SECURITY \_ NAME.
2.  Solicite el derecho \_ de acceso ACCESS SYSTEM SECURITY al abrir un identificador para el objeto \_ .
3.  Obtenga o establezca la SACL del objeto mediante una función como [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).
4.  Llame [**a AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) para deshabilitar el SE \_ SECURITY \_ NAME.

Para acceder a una SACL mediante las funciones [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) o [**SetNamedSecurityInfo,**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) habilite el SE \_ SECURITY \_ NAME. La función solicita internamente el derecho de acceso.

El derecho \_ de acceso ACCESS SYSTEM SECURITY no es válido en una DACL porque las \_ DACL no controlan el acceso a una SACL. Sin embargo, puede usar el derecho de acceso ACCESS SYSTEM SECURITY en una SACL para auditar los \_ \_ intentos de uso del derecho de acceso.

 

 
