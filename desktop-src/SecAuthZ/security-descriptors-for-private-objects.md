---
description: Para crear un descriptor de seguridad, un servidor protegido puede usar el mismo procedimiento que usaría una aplicación para crear un descriptor de seguridad para un objeto protegible.
ms.assetid: f40c4b62-a3f0-4e66-875e-2ef904d052e5
title: Descriptores de seguridad para objetos privados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97c40dc5c4e9f0a3d0e641874153d2862d038a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001279"
---
# <a name="security-descriptors-for-private-objects"></a>Descriptores de seguridad para objetos privados

Para crear un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly), un servidor protegido puede usar el mismo procedimiento que usaría una aplicación para crear un descriptor de seguridad para un objeto protegible. Para obtener código de ejemplo, vea [crear un descriptor de seguridad para un nuevo objeto en C++](creating-a-security-descriptor-for-a-new-object-in-c--.md). Como alternativa, una aplicación de servidor protegido puede llamar a la función [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) para hacerlo. Si se proporciona un puntero a un [*descriptor de seguridad autorelativo*](/windows/desktop/SecGloss/s-gly) existente a **BuildSecurityDescriptor**, se generará el nuevo descriptor de seguridad con la información tomada de ese descriptor de seguridad combinada con la nueva información de control de acceso pasada como parámetros en la llamada de función. El propietario y el grupo se especifican opcionalmente mediante las estructuras de [**confianza**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) que se pasan a la función. El descriptor de seguridad creado por **BuildSecurityDescriptor** está en formato *autorelativo* .

Además, la API de Windows proporciona un conjunto de funciones para combinar información de seguridad del cliente con la información heredada del descriptor de seguridad de un objeto primario o de un descriptor de seguridad predeterminado. Las funciones [**CreatePrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-createprivateobjectsecurity), [**GetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getprivateobjectsecurity), [**SetPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setprivateobjectsecurity)y [**DestroyPrivateObjectSecurity**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-destroyprivateobjectsecurity) proporcionan la capacidad de recuperar información predeterminada de un [*token de acceso*](/windows/desktop/SecGloss/a-gly), admitir la herencia y manipular partes específicas del descriptor de seguridad. Esto puede ser útil cuando un cliente crea un objeto privado en una jerarquía de objetos protegidos. Por ejemplo, puede usar la función **CreatePrivateObjectSecurity** para crear un descriptor de seguridad que contenía las ACE especificadas por el cliente, las ACE heredadas de un objeto primario y el propietario predeterminado del token de acceso del cliente de creación. Aunque [**BuildSecurityDescriptor**](/windows/desktop/api/Aclapi/nf-aclapi-buildsecuritydescriptora) crea descriptores de seguridad de la información de control de acceso que se pasa a la llamada de función o de un descriptor de seguridad existente, **CreatePrivateObjectSecurity** crea un descriptor de seguridad únicamente a partir de la información de los descriptores de seguridad existentes.

La función [**LookupSecurityDescriptorParts**](/windows/desktop/api/Aclapi/nf-aclapi-lookupsecuritydescriptorpartsa) obtiene información del descriptor de seguridad de un [*descriptor de seguridad autorelativo*](/windows/desktop/SecGloss/s-gly)existente. Esta información incluye las especificaciones de propietario y de grupo, el número de ACE en la SACL o DACL, y la lista de ACE en la SACL o DACL.

 

 
