---
description: Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) en Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: DPAPI DE CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666260"
---
# <a name="cng-dpapi"></a>DPAPI DE CNG

Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) en Windows 2000. La API está compuesta de dos funciones: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata). DPAPI es parte de CryptoAPI y se ha diseñado para desarrolladores que sabían muy poco sobre el uso de la criptografía. Las dos funciones se pueden usar para cifrar y descifrar los datos estáticos en un único equipo.

La informática en la nube, sin embargo, a menudo requiere que el contenido cifrado en un equipo se descifre en otro. Por tanto, a partir de Windows 8, Microsoft amplió la idea de usar una API relativamente sencilla para abarcar escenarios de nube. Esta nueva API, denominada DPAPI-NG, permite compartir de forma segura secretos (claves, contraseñas, material de clave) y mensajes mediante su protección en un conjunto de entidades de seguridad que se pueden usar para desprotegerlos en equipos diferentes después de la autenticación y autorización adecuadas. Actualmente se admiten las siguientes entidades de seguridad:

-   Un grupo de un bosque de Active Directory.
-   Credenciales Web.

Para obtener más información, vea los temas siguientes:

-   [Proveedores de protección](protection-providers.md)
-   [Descriptores de protección](protection-descriptors.md)
-   [Formato de datos protegidos](protected-data-format.md)

DPAPI-NG se basa en CNG (Cryptography Next Generation) e incluye las siguientes funciones:

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

 

 
