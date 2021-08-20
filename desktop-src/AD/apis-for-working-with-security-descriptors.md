---
title: API para trabajar con descriptores de seguridad
description: API para trabajar con descriptores de seguridad
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- descriptores de seguridad de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78988a2c435f397f0030ebaaef4e6d06385e710bc3671995338052c220f852
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024577"
---
# <a name="apis-for-working-with-security-descriptors"></a>API para trabajar con descriptores de seguridad

Cada objeto de Active Directory Domain Services tiene un **atributo nTSecurityDescriptor** que contiene el descriptor de seguridad del objeto. Hay dos maneras principales de leer y manipular un descriptor de seguridad de objetos de directorio:

-   Use el [**método IADs::Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el descriptor de seguridad como un objeto COM ADSI con una [**interfaz IADsSecurityDescriptor.**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) Las **interfaces IADsSecurityDescriptor,** [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)e [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) se pueden usar para controlar el descriptor de seguridad y sus componentes (ACL, ACE, y así sucesivamente). Para obtener más información y un ejemplo de código, vea [Using IADs to Get a Security Descriptor](using-iads-to-get-a-security-descriptor.md).
-   Use el [**método IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar un descriptor de seguridad de objetos como puntero a una estructura [**DESCRIPTOR \_ DE**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) SEGURIDAD. Use este puntero con una función de control de acceso win32, como [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) o [**BuildSecurityDescriptor.**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora) Para obtener más información y un ejemplo de código, vea [Using IDirectoryObject to Get a Security Descriptor](using-idirectoryobject-to-get-a-security-descriptor.md).

La técnica recomendada, y la que usan la mayoría de los ejemplos de código de esta guía, es usar las **interfaces IAD _ porque simplifican el control de descriptores de seguridad, ACL y \* *ACE. Para Visual Basic programadores,* las interfaces _ \* IADs** son la manera más eficaz de controlar los descriptores de seguridad.

La [**técnica IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) es útil cuando se requiere una [**estructura \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) DE SEGURIDAD. Por ejemplo, el ejemplo de código de Comprobar un derecho de acceso de control en la [ACL](checking-a-control-access-right-in-an-objectampaposs-acl.md) de un objeto usa este método para recuperar un descriptor de seguridad para pasar a la [**función AccessCheckByTypeResultList.**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist)

Para más información, consulte:

-   [Uso de identificadores para obtener un descriptor de seguridad](using-iads-to-get-a-security-descriptor.md)
-   [Uso de IDirectoryObject para obtener un descriptor de seguridad](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Componentes del descriptor de seguridad](security-descriptor-components.md)
-   [Recuperar la DACL de un objeto](retrieving-an-objectampaposs-dacl.md)
-   [Recuperar la SACL de un objeto](retrieving-an-objectampaposs-sacl.md)
-   [Leer el descriptor de seguridad de un objeto](reading-an-objectampaposs-security-descriptor.md)
-   [Código de ejemplo para crear un descriptor de seguridad](example-code-for-creating-a-security-descriptor.md)
-   [Código de ejemplo para enumerar la ACL de un objeto en Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 