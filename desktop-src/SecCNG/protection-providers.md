---
description: A partir Windows 8, Microsoft comenzó a distribuir los proveedores que le permiten compartir de forma segura secretos y mensajes cifrados entre equipos.
ms.assetid: C2E62DD2-8316-407B-B879-2617873F8409
title: Proveedores de protección
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c262fcfbfa5ab0842f103849af3d67b20f8e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073652"
---
# <a name="protection-providers"></a>Proveedores de protección

A partir Windows 8, Microsoft comenzó a distribuir los proveedores que le permiten compartir de forma segura secretos y mensajes cifrados entre equipos. Actualmente hay dos proveedores de protección clave. El proveedor de Microsoft Key Protection permite proteger el contenido de un grupo en un Active Directory de claves. El proveedor de Protección de claves de cliente de Microsoft permite proteger el contenido de un conjunto de credenciales web.

El protector correcto que se va a usar se elige automáticamente cuando la función [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor) analiza la cadena de regla del descriptor de protección que proporciona como entrada. El proveedor de Microsoft Key Protection se elige para las cadenas de reglas que comienzan por SID, SDDL y LOCAL. El proveedor de Microsoft Client Key Protection analiza las cadenas de regla que comienzan por WEBCREDENTIALS. Para obtener más información sobre las cadenas de reglas, vea [Descriptores de protección](protection-descriptors.md).

> [!Note]  
> Actualmente no se permiten proveedores personalizados. [DPAPI de CNG](cng-dpapi.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[CNG DPAPI](cng-dpapi.md)
</dt> <dt>

[**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
</dt> <dt>

[Descriptores de protección](protection-descriptors.md)
</dt> </dl>

 

 



