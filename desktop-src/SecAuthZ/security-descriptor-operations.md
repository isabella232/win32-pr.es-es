---
description: Use las funciones GetSecurityInfo y GetNamedSecurityInfo para recuperar un puntero a un descriptor de seguridad de objetos.
ms.assetid: 834f1b58-d403-4899-865e-5721a37587e9
title: Operaciones del descriptor de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9c7a7d1dab22f27bad785c6e1394403588a1719b2cc29932aba909aec89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780138"
---
# <a name="security-descriptor-operations"></a>Operaciones del descriptor de seguridad

La API Windows proporciona funciones para obtener y establecer los componentes del descriptor de [*seguridad*](/windows/desktop/SecGloss/s-gly) asociado a un objeto protegible. Use las [**funciones GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) [**y GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) para recuperar un puntero al descriptor de seguridad de un objeto. Estas funciones también pueden recuperar punteros a los componentes individuales del descriptor de seguridad: DACL, SACL, SID propietario y SID del grupo principal. Use las [**funciones SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) [**y SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) para establecer los componentes del descriptor de seguridad de un objeto.

En general, debe usar [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) y [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) con objetos identificados por un identificador, y [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) y [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) con objetos identificados por un nombre. Para obtener más información sobre las funciones específicas que se usarán al trabajar con los distintos tipos de objetos, vea [Objetos protegibles.](securable-objects.md)

La API Windows proporciona funciones adicionales para manipular los componentes de un descriptor de seguridad. Para obtener información sobre cómo trabajar con listas de control de acceso (DACL o SACL), vea Obtener información de una [ACL](getting-information-from-an-acl.md) y Crear o [modificar una ACL.](creating-or-modifying-an-acl.md) Para obtener información sobre los SID, vea [Identificadores de](security-identifiers.md) seguridad (SID).

Para obtener la información del control en un descriptor de seguridad, llame a la [**función GetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorcontrol) Para establecer los bits de control relacionados con la herencia ace automática, llame a la [**función SetSecurityDescriptorControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorcontrol) Las distintas funciones que establecen un componente de descriptor de seguridad establecen otros bits de control. Por ejemplo, si usa [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo) para cambiar la DACL de un objeto, la función establece o borra los bits según corresponda para indicar si el descriptor de seguridad tiene una DACL, si es una DACL predeterminada, y así sucesivamente. Otro ejemplo son los bits de control de [*Resource Manager*](/windows/desktop/SecGloss/r-gly) (RM) contenidos en el descriptor de seguridad. Estos bits se usan según la implementación del administrador de recursos y se accede a ellos a través de las funciones [**GetSecurityDescriptorRMControl**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-getsecuritydescriptorrmcontrol) y [**SetSecurityDescriptorRMControl.**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-setsecuritydescriptorrmcontrol)

 

 
