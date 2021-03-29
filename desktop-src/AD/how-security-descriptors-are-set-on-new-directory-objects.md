---
title: Cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio
description: Al crear un nuevo objeto en Active Directory Domain Services, puede crear explícitamente un descriptor de seguridad y, a continuación, establecer ese descriptor de seguridad como la propiedad nTSecurityDescriptor del objeto.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- objetos AD, cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio
- descriptores de seguridad AD, cómo establecer en nuevos objetos de directorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7858d08944e93165b4a1a63ef7d845ee646dc648
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487431"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Cómo se establecen los descriptores de seguridad en los nuevos objetos de directorio

Al crear un nuevo objeto en Active Directory Domain Services, puede crear explícitamente un descriptor de seguridad y, a continuación, establecer ese descriptor de seguridad como la propiedad **nTSecurityDescriptor** del objeto. Para obtener más información, vea [crear un descriptor de seguridad para un nuevo objeto de directorio](creating-a-security-descriptor-for-a-new-directory-object.md).

Active Directory Domain Services usar las siguientes reglas para establecer la DACL en el descriptor de seguridad del nuevo objeto:

-   Si especifica explícitamente un descriptor de seguridad al crear el objeto, el sistema combina las ACE heredables del objeto primario en la DACL especificada, a menos que el bit **\_ \_ protegido de DACL** se establezca en los bits de control del descriptor de seguridad.
-   Si no especifica un descriptor de seguridad, el sistema crea la DACL del objeto combinando las entradas de acceso heredables del objeto primario en la DACL predeterminada del objeto **ClassSchema** para la clase del objeto.
-   Si el esquema no tiene una DACL predeterminada, la DACL del objeto es la DACL predeterminada del token de suplantación o principal del creador.
-   Si no hay ninguna DACL especificada, heredada o predeterminada, el sistema crea el objeto sin DACL, lo que permite que todos los usuarios tengan acceso total al objeto.

El sistema utiliza un algoritmo similar para crear una SACL para un objeto de servicio de directorio.

El propietario y el grupo primario del descriptor de seguridad del nuevo objeto se establecen en los valores especificados en la propiedad **nTSecurityDescriptor** al crear el objeto. Si no establece estos valores, Active Directory Domain Services usar las reglas que se muestran en la tabla siguiente para establecerlos.



| Regla          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Propietario         | El propietario de un descriptor de seguridad predeterminado se establece en el SID del propietario predeterminado del token principal o de suplantación del proceso de creación. Para la mayoría de los usuarios, el SID del propietario predeterminado es el mismo que el SID que identifica la cuenta del usuario. Tenga en cuenta que para los usuarios que son miembros del grupo de administradores integrado, el sistema establece automáticamente el SID del propietario predeterminado en el token de acceso para el grupo administradores. por lo tanto, los objetos creados por un miembro del grupo administradores suelen pertenecer al grupo administradores. Para obtener o establecer el propietario predeterminado en un token de acceso, llame a la función [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la estructura del [**\_ propietario del token**](/windows/desktop/api/winnt/ns-winnt-token_owner) . |
| Grupo primario | El grupo principal de un descriptor de seguridad predeterminado se establece en el grupo primario predeterminado del token principal o de suplantación del creador. Tenga en cuenta que el grupo principal no se utiliza en el contexto de Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Para obtener más información sobre la herencia de ACE, consulte [herencia y delegación de la administración](inheritance-and-delegation-of-administration.md).

Para obtener más información acerca de los descriptores de seguridad predeterminados del esquema, consulte [descriptor de seguridad predeterminado](default-security-descriptor.md).

Para obtener más información sobre los objetos **ClassSchema** , vea [esquema de Active Directory](active-directory-schema.md).

 

 