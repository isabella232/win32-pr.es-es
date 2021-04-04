---
description: Windows admite un conjunto de funciones que crean una lista de control de acceso (ACL) o modifican las entradas de control de acceso (ACE) en una ACL existente.
ms.assetid: 71301aab-1040-4f61-855f-2b891c8b6077
title: Crear o modificar una ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0deb72bcd1a1c805dd8524027601952dda0eac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908289"
---
# <a name="creating-or-modifying-an-acl"></a>Crear o modificar una ACL

Windows admite un conjunto de funciones que crean una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) o modifican las [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) en una ACL existente.

La función [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) crea una nueva ACL. **SetEntriesInAcl** puede especificar un conjunto de ACE completamente nuevo para la ACL, o puede combinar una o varias ACE nuevas con las ACE de una ACL existente. La función **SetEntriesInAcl** usa una matriz de estructuras de [**\_ acceso explícitas**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para especificar la información de las nuevas ACE. Cada estructura de **\_ acceso explícita** contiene información que describe una única ACE. Esta información incluye los derechos de acceso, el tipo de ACE, las marcas que controlan la herencia de ACE y una estructura de [**confianza**](/windows/desktop/api/AccCtrl/ns-accctrl-trustee_a) que identifica al administrador de confianza.

**Para agregar una nueva ACE a una ACL existente**

1.  Utilice la función [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) o [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para obtener la DACL o SACL existente del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto.
2.  Para cada nueva ACE, llame a la función [**BuildExplicitAccessWithName**](/windows/desktop/api/Aclapi/nf-aclapi-buildexplicitaccesswithnamea) para rellenar una estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) con la información que describe la ACE.
3.  Llame a [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla), especificando la ACL existente y una matriz de estructuras de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) para las nuevas ACE. La función **SetEntriesInAcl** asigna e INICIALIZA la ACL y sus ACE.
4.  Llame a la función [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) o [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para adjuntar la nueva ACL al descriptor de seguridad del objeto.

Si el autor de la llamada especifica una ACL existente, [**SetEntriesInAcl**](/windows/desktop/api/Aclapi/nf-aclapi-setentriesinacla) combina la nueva información de ACE con las ACE existentes en la ACL. Considere el caso, por ejemplo, en el que la ACL existente concede acceso a un administrador de confianza especificado y una estructura de [**\_ acceso explícita**](/windows/desktop/api/AccCtrl/ns-accctrl-explicit_access_a) deniega el acceso al mismo administrador de confianza. En este caso, **SetEntriesInAcl** agrega una nueva ACE de acceso denegado para el administrador de confianza y elimina o modifica la ACE existente permitida para el administrador de confianza.

Para ver el código de ejemplo que combina una nueva ACE en una ACL existente, vea [modificar las ACL de un objeto en C++](modifying-the-acls-of-an-object-in-c--.md).

 

 
