---
description: Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) Windows 2000.
ms.assetid: 048DEA72-39E1-4129-A554-F7D08442C2D9
title: CNG DPAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd0771b9838b2dbcfbedb3d025a7f650429bba5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271228"
---
# <a name="cng-dpapi"></a>CNG DPAPI

Microsoft presentó la interfaz de programación de aplicaciones de protección de datos (DPAPI) Windows 2000. La API consta de dos funciones, [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) y [**CryptUnprotectData.**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) DPAPI forma parte de CryptoAPI y está pensado para desarrolladores que sabían muy poco sobre el uso de criptografía. Las dos funciones se pueden usar para cifrar y descifrar datos estáticos en un solo equipo.

Sin embargo, la informática en la nube a menudo requiere que el contenido cifrado en un equipo se descifre en otro. Por lo tanto, a Windows 8, Microsoft extendió la idea de usar una API relativamente sencilla para abarcar escenarios en la nube. Esta nueva API, denominada DPAPI-NG, permite compartir de forma segura secretos (claves, contraseñas, material de clave) y mensajes protegiéndolos en un conjunto de entidades de seguridad que se pueden usar para desprotegerlos en distintos equipos después de la autenticación y autorización adecuadas. Actualmente se admiten las entidades de seguridad siguientes:

-   Un grupo de un Active Directory bosque.
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

 

 
