---
title: Descriptor de seguridad predeterminado
description: Con Active Directory Domain Services, también puede especificar la seguridad predeterminada para cada tipo de objeto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descriptor de seguridad predeterminado AD
- descriptores de seguridad ad , valor predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ed57b775196ad6981a88b5621076d76c61035c4700af25ed3f35703fc9018b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118019886"
---
# <a name="default-security-descriptor"></a>Descriptor de seguridad predeterminado

Con Active Directory Domain Services, también puede especificar la seguridad predeterminada para cada tipo de objeto. Esto se especifica en el atributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) en la definición de objeto [**classSchema**](/windows/desktop/ADSchema/c-classschema) [en el Active Directory esquema](active-directory-schema.md). Este descriptor de seguridad se usa para proporcionar protección predeterminada en el objeto si no hay ningún descriptor de seguridad especificado durante la creación del objeto.

> [!Note]  
> Las ACE de un descriptor de seguridad predeterminado se controlan como si se hubieran especificado como parte de la creación de objetos. Por lo tanto, las ACE predeterminadas se colocan antes de las ACE heredadas y las invalidan según corresponda. Para obtener más información, [vea Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) se especifica en un formato de cadena especial mediante el Lenguaje de definición de [descriptores](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de seguridad (SDDL). Se pueden usar dos funciones para convertir la forma binaria del descriptor de seguridad en formato de cadena y viceversa. Estas funciones son las siguientes:

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Para obtener más información y los descriptores de seguridad predeterminados de las clases de objeto predefinidas, vea las páginas de referencia de clase en la referencia de esquema de Active Directory de la Active Directory Domain Services [referencia](active-directory-domain-services-reference.md).

Para obtener más información y un ejemplo de código que lee o modifica la propiedad [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de una clase de objeto, vea Leer [defaultSecurityDescriptor](reading-the-defaultsecuritydescriptor-for-an-object-class.md) para una clase object y [Modificar defaultSecurityDescriptor](modifying-the-defaultsecuritydescriptor-for-an-object-class.md)para una clase object .

 

 