---
description: A partir de Windows 8, Microsoft comenzó a distribuir los proveedores que le permiten compartir de forma segura secretos y mensajes cifrados entre equipos.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Proveedores de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001648"
---
# <a name="protection-providers"></a>Proveedores de protección

A partir de Windows 8, Microsoft comenzó a distribuir los proveedores que le permiten compartir de forma segura secretos y mensajes cifrados entre equipos. Actualmente hay dos proveedores de protección de claves. El proveedor de protección de claves de Microsoft permite proteger el contenido en un grupo de un bosque de Active Directory. El proveedor de protección de claves de cliente de Microsoft permite proteger el contenido en un conjunto de credenciales Web.

El protector correcto que se va a usar se elige automáticamente cuando la función [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analiza la cadena de la regla del descriptor de protección que proporciona como entrada. Se elige el proveedor de protección de claves de Microsoft para las cadenas de reglas que comienzan por SID, SDDL y LOCAL. El proveedor de protección de claves de cliente de Microsoft analiza las cadenas de reglas que comienzan con las credenciales webcredentials. Para obtener más información sobre las cadenas de reglas, consulte [descriptores de protección](protection-descriptors.md).

> [!Note]  
> Los proveedores personalizados no están permitidos actualmente. [DPAPI de CNG](cng-dpapi.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DPAPI DE CNG](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Descriptores de protección](protection-descriptors.md)
</dt> </dl>

 

 



