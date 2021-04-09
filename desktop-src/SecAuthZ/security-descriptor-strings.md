---
description: Un descriptor de seguridad funcional válido contiene información de seguridad en formato binario.
ms.assetid: 8f802652-b2bf-45cf-8186-1ac31eef1fe1
title: Cadenas de descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb875bee4d35267b578193ca7cd08420722400a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154748"
---
# <a name="security-descriptor-strings"></a>Cadenas de descriptor de seguridad

Un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) funcional válido contiene información de seguridad en formato binario. La API de Windows proporciona funciones para convertir descriptores de seguridad binarios en cadenas de texto y desde ellas. Los descriptores de seguridad en formato de cadena no funcionan, pero pueden ser útiles para almacenar o transportar información del descriptor de seguridad.

Para convertir un descriptor de seguridad en un formato de cadena, llame a la función [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) . Para volver a convertir un descriptor de seguridad de formato de cadena en un descriptor de seguridad funcional válido, llame a la función [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .

Para obtener más información, vea [lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md).

 

 
