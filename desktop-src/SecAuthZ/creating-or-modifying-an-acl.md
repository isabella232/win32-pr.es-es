---
description: Windows admite un conjunto de funciones que crean una lista de control de acceso (ACL) o modifican las entradas de control de acceso (ACE) en una ACL existente.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Creación o modificación de una ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0deb72bcd1a1c805dd8524027601952dda0eac1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160825"
---
# <a name="creating-or-modifying-an-acl"></a>Creación o modificación de una ACL

Windows admite un conjunto de funciones que crean una lista de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) o modifican las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) en una ACL existente.

La [**función SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) crea una nueva ACL. **SetEntriesInAcl** puede especificar un conjunto completamente nuevo de AAC para la ACL, o puede combinar uno o varios AAC nuevos con las ACE de una ACL existente. La **función SetEntriesInAcl** usa una matriz de estructuras [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para especificar la información de las nuevas ACE. Cada **estructura \_ EXPLICIT ACCESS** contiene información que describe una única ACE. Esta información incluye los derechos de acceso, el tipo de ACE, las marcas que controlan la herencia ace y una estructura [**TRUSTEE**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) que identifica al administrador de confianza.

**Para agregar una nueva ACE a una ACL existente**

1.  Use las [**funciones GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener la DACL o SACL existente del descriptor de seguridad [*de un objeto*](/windows/desktop/SecGloss/s-gly).
2.  Para cada nueva ACE, llame a la función [**BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) para rellenar una estructura [**EXPLICIT \_ ACCESS**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con la información que describe la ACE.
3.  Llame [**a SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), especificando la ACL existente y una matriz de estructuras [**DE ACCESO \_ EXPLÍCITO**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para las nuevas ACE. La **función SetEntriesInAcl** asigna e inicializa la ACL y sus ACE.
4.  Llame a [**la función SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) [**o SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para asociar la nueva ACL al descriptor de seguridad del objeto.

Si el autor de la llamada especifica una ACL existente, [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) combina la nueva información ace con las ACE existentes en la ACL. Considere el caso, por ejemplo, en el que la ACL existente concede acceso a un administrador de confianza especificado y una estructura [**DE \_ ACCESO**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) EXPLÍCITO deniega el acceso al mismo administrador de confianza. En este caso, **SetEntriesInAcl** agrega una nueva ACE de acceso denegado para el administrador de confianza y elimina o modifica la ACE existente con acceso permitido para el administrador de confianza.

Para obtener código de ejemplo que combina una nueva ACE en una ACL existente, vea Modificar las [ACL de un objeto en C++.](modifying-the-acls-of-an-object-in-c--.md)

 

 
