---
description: Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0273522580c806caa5fe7848ff32a2017cfb37c4499dee21f5a3787ecae57b63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908634"
---
# <a name="cng-dpapi"></a>CNG DPAPI

Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) Windows 2000. La API consta de dos funciones, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) DPAPI forma parte de CryptoAPI y está pensado para desarrolladores que sabían muy poco sobre el uso de criptografía. Las dos funciones se pueden usar para cifrar y descifrar datos estáticos en un solo equipo.

Sin embargo, la informática en la nube a menudo requiere que el contenido cifrado en un equipo se descifre en otro. Por lo tanto, a Windows 8, Microsoft extendió la idea de usar una API relativamente sencilla para abarcar escenarios en la nube. Esta nueva API, denominada DPAPI-NG, permite compartir de forma segura secretos (claves, contraseñas, material de clave) y mensajes protegiéndolos en un conjunto de entidades de seguridad que se pueden usar para desprotegerlos en distintos equipos después de la autenticación y autorización adecuadas. Actualmente se admiten las entidades de seguridad siguientes:

-   Un grupo en un Active Directory de datos.
-   Credenciales web.

Para obtener más información, vea los temas siguientes:

-   [Proveedores de protección](protection-providers.md)
-   [Descriptores de protección](protection-descriptors.md)
-   [Formato de datos protegidos](protected-data-format.md)

DPAPI-NG se basa en Cryptography Next Generation (CNG) e incluye las siguientes funciones:

-   [**NCryptCreateProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor)
-   [**NCryptCloseProtectionDescriptor**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptcloseprotectiondescriptor)
-   [**NCryptProtectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptprotectsecret)
-   [**NCryptQueryProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptqueryprotectiondescriptorname)
-   [**NCryptRegisterProtectionDescriptorName**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptregisterprotectiondescriptorname)
-   [**NCryptStreamClose**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamclose)
-   [**NCryptStreamOpenToProtect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentoprotect)
-   [**NCryptStreamOpenToUnprotect**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamopentounprotect)
-   [**NCryptStreamUpdate**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptstreamupdate)
-   [**NCryptUnprotectSecret**](/windows/desktop/api/NCryptprotect/nf-ncryptprotect-ncryptunprotectsecret)

 

 
