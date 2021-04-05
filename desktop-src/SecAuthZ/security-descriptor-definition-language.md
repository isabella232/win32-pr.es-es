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
# <a name="security-descriptor-definition-language"></a>Lenguaje de definición de descriptores de seguridad

El lenguaje de definición de descriptores de seguridad (SDDL) define el formato de cadena que usan las funciones [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) para describir un [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) como una cadena de texto. El lenguaje también define los elementos de cadena para describir la información de los componentes de un descriptor de seguridad.

> [!Note]  
> [*Las entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) condicional (ACE) tienen un formato SDDL diferente que otros tipos ACE. Para las ACE, consulte [cadenas ACE](ace-strings.md). Para las ACE condicionales, consulte [lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md).

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de cadena de descriptor de seguridad](security-descriptor-string-format.md)
</dt> <dt>

[Lenguaje de definición de descriptores de seguridad para ACE condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[Cadenas ACE](ace-strings.md)
</dt> <dt>

[Cadenas SID](sid-strings.md)
</dt> <dt>

[\[MS-DTYP \] : lenguaje de descripción de descriptores de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
