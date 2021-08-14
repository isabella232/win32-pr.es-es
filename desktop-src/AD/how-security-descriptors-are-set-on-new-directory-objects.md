---
title: Cómo se establecen los descriptores de seguridad en objetos de nuevo directorio
description: Al crear un nuevo objeto en Active Directory Domain Services, puede crear explícitamente un descriptor de seguridad y, a continuación, establecer ese descriptor de seguridad como la propiedad nTSecurityDescriptor del objeto.
ms.assetid: 07c367f8-cb5a-49ef-8e13-d31673c2ceee
ms.tgt_platform: multiple
keywords:
- objetos de AD, cómo se establecen los descriptores de seguridad en objetos de directorio nuevos
- descriptores de seguridad de AD, cómo establecer en objetos de directorio nuevos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d2009367c4d5604d359913b0154320332cd4be58e50dc5f065c574f8ea5fdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188116"
---
# <a name="how-security-descriptors-are-set-on-new-directory-objects"></a>Cómo se establecen los descriptores de seguridad en objetos de nuevo directorio

Al crear un nuevo objeto en Active Directory Domain Services, puede crear explícitamente un descriptor de seguridad y, a continuación, establecer ese descriptor de seguridad como la propiedad **nTSecurityDescriptor del** objeto. Para obtener más información, vea [Creating a Security Descriptor for a New Directory Object](creating-a-security-descriptor-for-a-new-directory-object.md).

Active Directory Domain Services las reglas siguientes para establecer la DACL en el descriptor de seguridad del nuevo objeto:

-   Si especifica explícitamente un descriptor de seguridad al crear el objeto, el sistema combina todas las ACE heredables del objeto primario en la DACL especificada, a menos que el bit **\_ DACL \_ PROTECTED** de SE esté establecido en los bits de control del descriptor de seguridad.
-   Si no especifica un descriptor de seguridad, el sistema compila la DACL del objeto combinando las ACE heredables del objeto primario en la DACL predeterminada del objeto **classSchema** para la clase del objeto .
-   Si el esquema no tiene una DACL predeterminada, la DACL del objeto es la DACL predeterminada del token principal o de suplantación del creador.
-   Si no hay ninguna DACL especificada, heredada o predeterminada, el sistema crea el objeto sin DACL, lo que permite que todos los usuarios accedan al objeto.

El sistema usa un algoritmo similar para compilar una SACL para un objeto de servicio de directorio.

El propietario y el grupo principal del descriptor de seguridad del nuevo objeto se establecen en los valores especificados en la propiedad **nTSecurityDescriptor** al crear el objeto. Si no establece estos valores, Active Directory Domain Services las reglas enumeradas en la tabla siguiente para establecerlos.



| Regla          | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Propietario         | El propietario de un descriptor de seguridad predeterminado se establece en el SID del propietario predeterminado del token principal o de suplantación del proceso de creación. Para la mayoría de los usuarios, el SID del propietario predeterminado es el mismo que el SID que identifica la cuenta del usuario. Tenga en cuenta que para los usuarios que son miembros del grupo de administradores integrado, el sistema establece automáticamente el SID de propietario predeterminado del token de acceso en el grupo de administradores. Por lo tanto, los objetos creados por un miembro del grupo de administradores suelen pertenecer al grupo de administradores. Para obtener o establecer el propietario predeterminado en un token de acceso, llame a la función [**GetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) o [**SetTokenInformation**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-settokeninformation) con la [**estructura TOKEN \_**](/windows/desktop/api/winnt/ns-winnt-token_owner) OWNER. |
| Grupo principal | El grupo principal de un descriptor de seguridad predeterminado se establece en el grupo principal predeterminado del token principal o de suplantación del creador. Tenga en cuenta que el grupo principal no se usa en el contexto de Active Directory Domain Services.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

Para obtener más información sobre la herencia ace, vea [Herencia y delegación de administración.](inheritance-and-delegation-of-administration.md)

Para obtener más información sobre los descriptores de seguridad predeterminados en el esquema, vea [Descriptor de seguridad predeterminado](default-security-descriptor.md).

Para obtener más información sobre **los objetos classSchema,** [vea Active Directory Schema](active-directory-schema.md).

 

 