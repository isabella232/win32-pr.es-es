---
description: Cree una lista de control de acceso (ACL) mediante las funciones de bajo nivel, asigne un búfer para la ACL y, a continuación, inicialice mediante una llamada a la función InitializeAcl.
ms.assetid: 9dcbbd4c-b3b3-43fd-b3a6-0637a53a455a
title: Funciones de ACL y ACE de bajo nivel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dab8c968c19e652f530abe25aaae11e47f36db1cd6ea7184120987c63a1bd9b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670665"
---
# <a name="low-level-acl-and-ace-functions"></a>Funciones de ACL y ACE de bajo nivel

Para crear una [*lista de control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) mediante las funciones de bajo nivel, asigne un búfer para la ACL y, a continuación, inicialíicelo llamando a la función [**InitializeAcl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-initializeacl) Para agregar [*entradas de control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) al final de una lista de [*control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL), use las funciones [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) y [**AddAccessDeniedAce.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedace) La [**función AddAuditAccessAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessace) agrega una ACE al final de una lista de control de [*acceso del sistema*](/windows/desktop/SecGloss/s-gly) (SACL). Puede usar la [**función AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) para agregar una o varias ACE en una posición especificada de una ACL. La **función AddAce** también permite agregar una ACE heredable a una ACL. La [**función DeleteAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-deleteace) quita una ACE de una posición especificada en una ACL. La [**función GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) recupera una ACE de una posición especificada en una ACL. La [**función FindFirstFreeAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-findfirstfreeace) recupera un puntero al primer byte libre de una ACL.

Para modificar una ACL existente en el [*descriptor*](/windows/desktop/SecGloss/s-gly)de seguridad de un objeto , use la función [**GetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptordacl) o [**GetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorsacl) para obtener la ACL existente. Puede usar la función [**GetAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getace) para copiar las ACE de la ACL existente. Después de asignar e inicializar una nueva ACL, use funciones como [**AddAccessAllowedAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedace) y [**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace) para agregarle AAC. Cuando haya terminado de compilar la nueva ACL, use la función [**SetSecurityDescriptorDacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptordacl) o [**SetSecurityDescriptorSacl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorsacl) para agregar la nueva ACL al descriptor de seguridad del objeto.

Puede usar las funciones [](object-specific-aces.md) [**AddAccessAllowedObjectAce,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessallowedobjectace) [**AddAccessDeniedObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addaccessdeniedobjectace)o [**AddAuditAccessObjectAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addauditaccessobjectace) para agregar ACE específicas del objeto al final de una ACL.

 

 
