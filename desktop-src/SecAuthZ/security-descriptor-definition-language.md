---
description: Explica el lenguaje de definición del descriptor de seguridad (SDDL).
ms.assetid: 2b15325e-34ed-497b-ae6d-3ec3ac168232
title: Lenguaje de definición del descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9de9d3535efe5c33ac633a9dbd295405d74b6a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073680"
---
# <a name="security-descriptor-definition-language"></a>Lenguaje de definición del descriptor de seguridad

El lenguaje de definición de descriptores de seguridad (SDDL) define el formato de cadena que las funciones [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/Sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora) usan para describir un [*descriptor*](/windows/desktop/SecGloss/s-gly) de seguridad como una cadena de texto. El lenguaje también define elementos de cadena para describir información en los componentes de un descriptor de seguridad.

> [!Note]  
> Las [*entradas de control de acceso condicional*](/windows/desktop/SecGloss/a-gly) (ACE) tienen un formato SDDL diferente al de otros tipos ace. Para las ACE, vea [Ace Strings](ace-strings.md). Para las ACE condicionales, vea [Lenguaje de definición de descriptores de seguridad para ACE condicionales.](security-descriptor-definition-language-for-conditional-aces-.md)

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de cadena del descriptor de seguridad](security-descriptor-string-format.md)
</dt> <dt>

[Lenguaje de definición de descriptores de seguridad para A CA condicionales](security-descriptor-definition-language-for-conditional-aces-.md)
</dt> <dt>

[Cadenas ACE](ace-strings.md)
</dt> <dt>

[Cadenas SID](sid-strings.md)
</dt> <dt>

[\[MS-DTYP: \] lenguaje de descripción del descriptor de seguridad](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

 

 
