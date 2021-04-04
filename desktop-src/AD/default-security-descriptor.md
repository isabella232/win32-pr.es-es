---
title: Descriptor de seguridad predeterminado
description: Con Active Directory Domain Services, también puede especificar la seguridad predeterminada para cada tipo de objeto.
ms.assetid: 6642c966-c163-4d63-8707-62a545d15094
ms.tgt_platform: multiple
keywords:
- Descriptor de seguridad predeterminado AD
- descriptores de seguridad (AD), predeterminado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372f285c3e8c17b481811d7356c40ae07316801d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077537"
---
# <a name="default-security-descriptor"></a>Descriptor de seguridad predeterminado

Con Active Directory Domain Services, también puede especificar la seguridad predeterminada para cada tipo de objeto. Esto se especifica en el atributo [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de la definición del objeto [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) en el [esquema de Active Directory](active-directory-schema.md). Este descriptor de seguridad se usa para proporcionar protección predeterminada en el objeto si no se especifica ningún descriptor de seguridad durante la creación del objeto.

> [!Note]  
> Las ACE de un descriptor de seguridad predeterminado se administran como si se hubieran especificado como parte de la creación de objetos. Por lo tanto, las ACE predeterminadas se colocan delante de las ACE heredadas y las reemplazan según corresponda. Para obtener más información, vea [orden de las ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

[**DefaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) se especifica en un formato de cadena especial mediante el [lenguaje de definición de descriptores de seguridad](/windows/desktop/SecAuthZ/security-descriptor-definition-language) (SDDL). Se pueden usar dos funciones para convertir el formato binario del descriptor de seguridad al formato de cadena y viceversa. Estas funciones son las siguientes:

-   [ConvertSecurityDescriptorToStringSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora)
-   [ConvertStringSecurityDescriptorToSecurityDescriptor](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Para obtener más información y los descriptores de seguridad predeterminados de las clases de objeto predefinidas, vea las páginas de referencia de la clase en la Active Directory referencia de esquema de la [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md).

Para obtener más información y un ejemplo de código que lee o modifica la propiedad [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) de una clase de objeto, vea [leer el DefaultSecurityDescriptor de una clase de objeto](reading-the-defaultsecuritydescriptor-for-an-object-class.md) y [modificar DefaultSecurityDescriptor para una clase de objeto](modifying-the-defaultsecuritydescriptor-for-an-object-class.md).

 

 