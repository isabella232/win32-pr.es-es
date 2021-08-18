---
description: Para crear un descriptor de seguridad, un servidor protegido puede usar el mismo procedimiento que usaría una aplicación para crear un descriptor de seguridad para un objeto protegible.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descriptores de seguridad para objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bae6615f309e572dc2e22f76310ccdf84bbbf5fff504aef0331d7d8e6b60ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413735"
---
# <a name="security-descriptors-for-private-objects"></a>Descriptores de seguridad para objetos privados

Para crear un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly), un servidor protegido puede usar el mismo procedimiento que una aplicación usaría para crear un descriptor de seguridad para un objeto protegible. Para obtener código de ejemplo, [vea Crear un descriptor de seguridad para un nuevo objeto en C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md) Como alternativa, una aplicación de servidor protegido puede llamar a [**la función BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) para hacerlo. Si se proporciona un puntero a un descriptor de seguridad auto-relativo existente a **BuildSecurityDescriptor**, se compilará el nuevo [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad con información procedente de ese descriptor de seguridad combinado con la nueva información de control de acceso pasada como parámetros en la llamada de función. Opcionalmente, las estructuras TRUSTEE pasan a la función para especificar [**el**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) propietario y el grupo. El descriptor de seguridad creado **por BuildSecurityDescriptor** está en *formato auto relativo.*

Además, la API Windows proporciona un conjunto de funciones para combinar información de seguridad de cliente con información heredada del descriptor de seguridad para un objeto primario o de un descriptor de seguridad predeterminado. Las funciones [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity), [**GetPrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity) [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)y [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) proporcionan la capacidad de recuperar información predeterminada de un [*token*](/windows/desktop/SecGloss/a-gly)de acceso, admitir la herencia y manipular partes específicas del descriptor de seguridad. Esto puede ser útil cuando un cliente crea un objeto privado en una jerarquía de objetos protegidos. Por ejemplo, podría usar la función **CreatePrivateObjectSecurity** para crear un descriptor de seguridad que contenga las ACE especificadas por el cliente, las ACE heredadas de un objeto primario y el propietario predeterminado del token de acceso del cliente de creación. Aunque [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crea descriptores de seguridad a partir de la información de control de acceso que se pasa a la llamada de función o de un descriptor de seguridad existente, **CreatePrivateObjectSecurity** crea un descriptor de seguridad únicamente a partir de la información de los descriptores de seguridad existentes.

[**La función LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) obtiene información del descriptor de seguridad de un descriptor de seguridad [*auto-relativo existente.*](/windows/desktop/SecGloss/s-gly) Esta información incluye la especificación de propietario y grupo, el número de AEE en SACL o DACL y la lista de AEE en sacl o DACL.

 

 
