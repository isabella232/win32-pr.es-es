---
description: Explica el lenguaje de definición de descriptores de seguridad (SDDL).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Lenguaje de definición de descriptores de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908172"
---
# <a name="security-descriptor-definition-language"></a><span data-ttu-id="714cc-103">Lenguaje de definición de descriptores de seguridad</span><span class="sxs-lookup"><span data-stu-id="714cc-103">Security Descriptor Definition Language</span></span>

<span data-ttu-id="714cc-104">El lenguaje de definición de descriptores de seguridad (SDDL) define el formato de cadena que usan las funciones [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para describir un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) como una cadena de texto.</span><span class="sxs-lookup"><span data-stu-id="714cc-104">The security descriptor definition language (SDDL) defines the string format that the [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) functions use to describe a [*security descriptor*](/windows/desktop/SecGloss/s-gly) as a text string.</span></span> <span data-ttu-id="714cc-105">El lenguaje también define los elementos de cadena para describir la información de los componentes de un descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="714cc-105">The language also defines string elements for describing information in the components of a security descriptor.</span></span>

> [!Note]  
> <span data-ttu-id="714cc-106">[*Las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) condicional (ACE) tienen un formato SDDL diferente que otros tipos ACE.</span><span class="sxs-lookup"><span data-stu-id="714cc-106">Conditional [*access control entries*](/windows/desktop/SecGloss/a-gly) (ACEs) have a different SDDL format than other ACE types.</span></span> <span data-ttu-id="714cc-107">Para las ACE, consulte [cadenas ACE](ace-strings.md).</span><span class="sxs-lookup"><span data-stu-id="714cc-107">For ACEs, see [ACE Strings](ace-strings.md).</span></span> <span data-ttu-id="714cc-108">Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).</span><span class="sxs-lookup"><span data-stu-id="714cc-108">For conditional ACEs, see [Security Descriptor Definition Language for Conditional ACEs](security-descriptor-definition-language-for-conditional-aces-.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="714cc-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="714cc-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="714cc-110">Formato de cadena de descriptor de seguridad</span><span class="sxs-lookup"><span data-stu-id="714cc-110">Security Descriptor String Format</span></span>](security-descriptor-string-format.md)
</dt> <dt>

[<span data-ttu-id="714cc-111">Lenguaje de definición de descriptores de seguridad para ACE condicionales</span><span class="sxs-lookup"><span data-stu-id="714cc-111">Security Descriptor Definition Language for Conditional ACEs</span></span>](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[<span data-ttu-id="714cc-112">Cadenas ACE</span><span class="sxs-lookup"><span data-stu-id="714cc-112">ACE Strings</span></span>](ace-strings.md)
</dt> <dt>

[<span data-ttu-id="714cc-113">Cadenas SID</span><span class="sxs-lookup"><span data-stu-id="714cc-113">SID Strings</span></span>](sid-strings.md)
</dt> <dt>

<span data-ttu-id="714cc-114">[\[MS-DTYP \] : lenguaje de descripción de descriptores de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span><span class="sxs-lookup"><span data-stu-id="714cc-114">[\[MS-DTYP\]: Security Descriptor Description Language](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)</span></span>
</dt> </dl>

 

 
