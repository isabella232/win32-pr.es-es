---
description: Una aplicación de servidor protegido debe comprobar los derechos de acceso de los clientes antes de permitir que el cliente tenga acceso a un objeto privado protegido.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Comprobar el acceso a objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b7b3d8b2cd933b00be0be9f1f2b077f5c7a2d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001224"
---
# <a name="checking-access-to-private-objects"></a>Comprobar el acceso a objetos privados

Una aplicación de servidor protegido debe comprobar los derechos de acceso de un cliente antes de permitir que el cliente tenga acceso a un objeto privado protegido. Para ello, el servidor pasa un [*token de suplantación*](/windows/desktop/SecGloss/i-gly), un descriptor de seguridad y un conjunto de derechos de acceso solicitados a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). Las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) de la DACL [*del descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) especifican los derechos de acceso permitidos o denegados a varios confíantes. La función **AccessCheck** compara el administrador de confianza de cada ACE con los destinatarios identificados en el token de suplantación. Para obtener una descripción del algoritmo que se usa para conceder o denegar el acceso, vea [Cómo controlan el acceso a un objeto las DACL](how-dacls-control-access-to-an-object.md).

La función [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) realiza una comprobación de acceso similar. Además, genera registros de auditoría en el registro de eventos de seguridad según la SACL del descriptor de seguridad.

Las funciones [**AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) y [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) son similares a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) y [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) , salvo que permiten comprobar el acceso a los subobjetos de un objeto, como los conjuntos de propiedades o las propiedades. Las funciones [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) y [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) también son similares a **AccessCheck** , salvo que proporcionan los resultados de la comprobación de acceso para cada subobjeto en una jerarquía de las propiedades y los conjuntos de propiedades del objeto. Estas funciones usan la estructura de la [**\_ \_ lista de tipos de objeto**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) para describir la jerarquía de objetos para los que se comprueba el acceso. Las funciones que generan un mensaje de auditoría usan el tipo de enumeración de [**\_ \_ tipo de evento de auditoría**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) para indicar si el objeto que se está comprobando es un objeto de servicio de directorio. Para obtener más información acerca de la jerarquía de un objeto y sus subobjetos, vea [ACE para controlar el acceso a las propiedades de un objeto](aces-to-control-access-to-an-object-s-properties.md).

Los derechos de acceso solicitados que se pasan a las funciones [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) y [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) no deben incluir [derechos de acceso genéricos](generic-access-rights.md). El servidor puede usar la función [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) para convertir los derechos de acceso genéricos en los derechos específicos y estándar correspondientes según la asignación especificada en la estructura de [**\_ asignación genérica**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping) .

Las funciones [**AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) y [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) comparan una [*máscara de acceso*](/windows/desktop/SecGloss/a-gly) solicitada con una máscara de acceso concedida.

Para ver el código de ejemplo que usa la función [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , vea [comprobar el acceso de cliente con ACL en C++](verifying-client-access-with-acls-in-c--.md).

La función [**ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) crea y devuelve un descriptor de seguridad en un formato que permite la propagación automática de las ACE heredables. Este descriptor de seguridad contiene todas las ACE, heredadas y no heredadas, en el descriptor de seguridad actual y está en formato [*autorelativo*](/windows/desktop/SecGloss/s-gly) . La función **ConvertToAutoInheritPrivateObjectSecurity** determina si las ACE son heredadas o no heredadas comparando todas las ACE en el descriptor de seguridad actual con todas las ACE en su descriptor de seguridad primario. Es posible que no haya una correspondencia uno a uno entre los dos grupos de ACE. Por ejemplo, una ACE que permita permisos de lectura y escritura puede ser equivalente a dos ACE: una ACE que permita el permiso de lectura y una ACE que permita el permiso de escritura. No se puede proporcionar un descriptor de seguridad primario cuando el descriptor de seguridad actual es el elemento primario.

 

 
