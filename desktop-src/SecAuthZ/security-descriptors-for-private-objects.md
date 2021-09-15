---
description: Para crear un descriptor de seguridad, un servidor protegido puede usar el mismo procedimiento que una aplicación usaría para crear un descriptor de seguridad para un objeto protegible.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descriptores de seguridad para objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473470"
---
# <a name="security-descriptors-for-private-objects"></a>Descriptores de seguridad para objetos privados

Para crear un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly), un servidor protegido puede usar el mismo procedimiento que una aplicación usaría para crear un descriptor de seguridad para un objeto protegible. Para obtener código de ejemplo, [vea Crear un descriptor de seguridad para un nuevo objeto en C++.](creating-a-security-descriptor-for-a-new-object-in-c--.md) Como alternativa, una aplicación de servidor protegido puede llamar a [**la función BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) para hacerlo. Si se proporciona un puntero a un descriptor de seguridad auto relativo existente a **BuildSecurityDescriptor**, se compilará el nuevo [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad con la información tomada de ese descriptor de seguridad combinada con la nueva información de control de acceso pasada como parámetros en la llamada de función. El propietario y el grupo se especifican opcionalmente mediante estructuras [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) que se pasan a la función. El descriptor de seguridad creado **por BuildSecurityDescriptor** está en *formato auto relativo.*

Además, la API Windows proporciona un conjunto de funciones para combinar información de seguridad de cliente con información heredada del descriptor de seguridad para un objeto primario o de un descriptor de seguridad predeterminado. Las funciones [**CreatePrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity) [**GetPrivateObjectSecurity,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity) [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)y [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) proporcionan la capacidad de recuperar información predeterminada de un [*token*](/windows/desktop/SecGloss/a-gly)de acceso, admitir la herencia y manipular partes específicas del descriptor de seguridad. Esto puede ser útil cuando un cliente crea un objeto privado en una jerarquía de objetos protegidos. Por ejemplo, puede usar la función **CreatePrivateObjectSecurity** para crear un descriptor de seguridad que contenga las ACE especificadas por el cliente, las ACE heredadas de un objeto primario y el propietario predeterminado del token de acceso del cliente de creación. Aunque [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crea descriptores de seguridad a partir de la información de control de acceso que se pasa a la llamada de función o de un descriptor de seguridad existente, **CreatePrivateObjectSecurity** crea un descriptor de seguridad únicamente a partir de la información de los descriptores de seguridad existentes.

[**La función LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) obtiene información del descriptor de seguridad de un descriptor de seguridad [*auto relativo existente.*](/windows/desktop/SecGloss/s-gly) Esta información incluye la especificación de propietario y grupo, el número de ACE en sacl o DACL y la lista de ASE en sacl o DACL.

 

 
