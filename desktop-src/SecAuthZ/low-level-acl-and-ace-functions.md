---
description: Cree una lista de control de acceso (ACL) mediante las funciones de bajo nivel, asigne un búfer a la ACL y, a continuación, Inicialícelo mediante una llamada a la función InitializeAcl.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Funciones ACL y ACE de bajo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac63c17d84996afe9bdc43d0ccdd021db69ab488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912422"
---
# <a name="low-level-acl-and-ace-functions"></a>Funciones ACL y ACE de bajo nivel

Para crear una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) mediante las funciones de bajo nivel, asigne un búfer a la ACL y, a continuación, Inicialícelo mediante una llamada a la función [**InitializeAcl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) . Para agregar [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE) al final de una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL), use las funciones [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) y [**AddAccessDeniedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) . La función [**AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) agrega una ACE al final de una [*lista de control de acceso de sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Puede usar la función [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) para agregar una o más ACE en una posición especificada de una ACL. La función **AddAce** también le permite agregar una ACE heredable a una ACL. La función [**DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) quita una ACE de una posición especificada en una ACL. La función [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) recupera una ACE de una posición especificada en una ACL. La función [**FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) recupera un puntero al primer byte libre de una ACL.

Para modificar una ACL existente en el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)de un objeto, utilice la función [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) o [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) para obtener la ACL existente. Puede usar la función [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) para copiar las ACE de la ACL existente. Después de asignar e inicializar una nueva ACL, use funciones como [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) y [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) para agregarle ACE. Cuando haya terminado de generar la nueva ACL, utilice la función [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) o [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) para agregar la nueva ACL al descriptor de seguridad del objeto.

Puede usar las funciones [**AddAccessAllowedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace), [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)o [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) para agregar [ACE específicas del objeto](object-specific-aces.md) al final de una ACL.

 

 
