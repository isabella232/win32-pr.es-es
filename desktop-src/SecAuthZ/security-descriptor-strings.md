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
# <a name="security-descriptor-strings"></a><span data-ttu-id="d61f9-103">Cadenas de descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="d61f9-103">Security Descriptor Strings</span></span>

<span data-ttu-id="d61f9-104">Un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) funcional válido contiene información de seguridad en formato binario.</span><span class="sxs-lookup"><span data-stu-id="d61f9-104">A valid functional [*security descriptor*](/windows/desktop/SecGloss/s-gly) contains security information in binary format.</span></span> <span data-ttu-id="d61f9-105">La API de Windows proporciona funciones para convertir descriptores de seguridad binarios en cadenas de texto y desde ellas.</span><span class="sxs-lookup"><span data-stu-id="d61f9-105">The Windows API provides functions for converting binary security descriptors to and from text strings.</span></span> <span data-ttu-id="d61f9-106">Los descriptores de seguridad en formato de cadena no funcionan, pero pueden ser útiles para almacenar o transportar información del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d61f9-106">Security descriptors in string format are not functional, but they can be useful for storing or transporting security descriptor information.</span></span>

<span data-ttu-id="d61f9-107">Para convertir un descriptor de seguridad en un formato de cadena, llame a la función [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="d61f9-107">To convert a security descriptor to a string format, call the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) function.</span></span> <span data-ttu-id="d61f9-108">Para volver a convertir un descriptor de seguridad de formato de cadena en un descriptor de seguridad funcional válido, llame a la función [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) .</span><span class="sxs-lookup"><span data-stu-id="d61f9-108">To convert a string-format security descriptor back to a valid functional security descriptor, call the [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) function.</span></span>

<span data-ttu-id="d61f9-109">Para obtener más información, vea [lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md).</span><span class="sxs-lookup"><span data-stu-id="d61f9-109">For more information, see [Security Descriptor Definition Language](security-descriptor-definition-language.md).</span></span>

 

 
