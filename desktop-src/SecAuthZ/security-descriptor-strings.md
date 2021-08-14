---
description: Un descriptor de seguridad funcional válido contiene información de seguridad en formato binario.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Cadenas de descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edbefeb87a7fca30f0c33d6f180315df5e5d576dc018e69dc680391050a840d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119413795"
---
# <a name="security-descriptor-strings"></a>Cadenas de descriptor de seguridad

Un descriptor de [*seguridad funcional válido*](/windows/desktop/SecGloss/s-gly) contiene información de seguridad en formato binario. La API Windows proporciona funciones para convertir descriptores de seguridad binarios en cadenas de texto y desde estas. Los descriptores de seguridad en formato de cadena no son funcionales, pero pueden ser útiles para almacenar o transportar información del descriptor de seguridad.

Para convertir un descriptor de seguridad a un formato de cadena, llame a la [**función ConvertSecurityDescriptorToStringSecurityDescriptor.**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) Para volver a convertir un descriptor de seguridad con formato de cadena en un descriptor de seguridad funcional válido, llame a la [**función ConvertStringSecurityDescriptorToSecurityDescriptor.**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)

Para obtener más información, vea [Lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md).

 

 
