---
description: Una aplicación de servidor protegido debe comprobar los derechos de acceso de los clientes antes de permitir que el cliente acceda a un objeto privado protegido.
ms.assetid: dce4dd10-1d5f-40a3-8a7e-ec708d3123c7
title: Comprobación del acceso a objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b7b3d8b2cd933b00be0be9f1f2b077f5c7a2d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160852"
---
# <a name="checking-access-to-private-objects"></a>Comprobación del acceso a objetos privados

Una aplicación de servidor protegido debe comprobar los derechos de acceso de un cliente antes de permitir que el cliente acceda a un objeto privado protegido. Para ello, el servidor pasa un token de [*suplantación,*](/windows/desktop/SecGloss/i-gly)un descriptor de seguridad y un conjunto de derechos de acceso solicitados a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck). Las [*entradas de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE) en la DACL del [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad especifican los derechos de acceso permitidos o denegados a varios administradores de confianza. La **función AccessCheck** compara el administrador de confianza de cada ACE con los administradores de confianza identificados en el token de suplantación. Para obtener una descripción del algoritmo utilizado para conceder o denegar el acceso, vea [How DACLs Control Access to an Object](how-dacls-control-access-to-an-object.md).

La [**función AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) realiza una comprobación de acceso similar. Además, genera registros de auditoría en el registro de eventos de seguridad en función de la SACL del descriptor de seguridad.

Las [**funciones AccessCheckByType**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) y [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma) son similares a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) y [**AccessCheckAndAuditAlarm,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) salvo que permiten comprobar el acceso a los subobjetos de un objeto, como conjuntos de propiedades o propiedades. Las funciones [**AccessCheckByTypeResultList**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) y [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) también son similares a **AccessCheck,** salvo que proporcionan los resultados de la comprobación de acceso para cada subobjeto de una jerarquía de propiedades y conjuntos de propiedades del objeto. Estas funciones usan la [**estructura OBJECT \_ TYPE \_ LIST**](/windows/desktop/api/Winnt/ns-winnt-object_type_list) para describir la jerarquía de objetos para los que se comprueba el acceso. Las funciones que generan un mensaje de auditoría usan el tipo de enumeración [**AUDIT \_ EVENT \_ TYPE**](/windows/desktop/api/Winnt/ne-winnt-audit_event_type) para indicar si el objeto que se comprueba es un objeto de servicio de directorio. Para obtener más información sobre la jerarquía de un objeto y sus subobjetos, vea ACE para controlar el acceso [a las propiedades de un objeto](aces-to-control-access-to-an-object-s-properties.md).

Los derechos de acceso solicitados pasados a las funciones [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) y [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma) no deben incluir derechos [de acceso genéricos.](generic-access-rights.md) El servidor puede usar la función [**MapGenericMask**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-mapgenericmask) para convertir los derechos de acceso genéricos a los derechos específicos y estándar correspondientes según la asignación especificada en la estructura [**GENERIC \_ MAPPING.**](/windows/desktop/api/Winnt/ns-winnt-generic_mapping)

Las [**funciones AreAllAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areallaccessesgranted) y [**AreAnyAccessesGranted**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-areanyaccessesgranted) comparan una máscara de acceso solicitada [*con*](/windows/desktop/SecGloss/a-gly) una máscara de acceso concedido.

Para obtener código de ejemplo que usa [**la función AccessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) vea [Verifying Client Access with ACLs in C++](verifying-client-access-with-acls-in-c--.md)(Comprobación del acceso de cliente con ACL en C++).

La [**función ConvertToAutoInheritPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-converttoautoinheritprivateobjectsecurity) crea y devuelve un descriptor de seguridad en un formato que permite la propagación automática de ACE heredables. Este descriptor de seguridad contiene todas las ACE, heredadas y no heredadas, en el descriptor de seguridad actual y está en formato [*auto relativo.*](/windows/desktop/SecGloss/s-gly) La **función ConvertToAutoInheritPrivateObjectSecurity** determina si las ACE se heredan o no al comparar todas las ACE del descriptor de seguridad actual con todas las ACE de su descriptor de seguridad primario. Puede que no haya una correspondencia uno a uno entre los dos grupos de ASE. Por ejemplo, una ACE que permita el permiso de lectura y escritura puede ser equivalente a dos ACE: una ACE que permite el permiso de lectura y una ACE que permite el permiso de escritura. No se puede proporcionar un descriptor de seguridad primario cuando el descriptor de seguridad actual es el primario.

 

 
