---
title: API para trabajar con descriptores de seguridad
description: API para trabajar con descriptores de seguridad
ms.assetid: eb5ee183-949c-41f5-9f74-f9c418fdf0a2
ms.tgt_platform: multiple
keywords:
- AD descriptores de seguridad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfb798e036d5e30ba58a83499b92340bf30ee3cb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995107"
---
# <a name="apis-for-working-with-security-descriptors"></a>API para trabajar con descriptores de seguridad

Cada objeto de Active Directory Domain Services tiene un atributo **nTSecurityDescriptor** que contiene el descriptor de seguridad del objeto. Hay dos formas principales de leer y manipular un descriptor de seguridad de objetos de directorio:

-   Use el método [**IADs:: get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el descriptor de seguridad como un objeto com ADSI con una interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) . Las interfaces **IADsSecurityDescriptor**, [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist)y [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) se pueden usar para controlar el descriptor de seguridad y sus componentes (ACL, ACE, etc.). Para obtener más información y un ejemplo de código, vea [usar iAds para obtener un descriptor de seguridad](using-iads-to-get-a-security-descriptor.md).
-   Use el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/iads/nf-iads-idirectoryobject-getobjectattributes) para recuperar un descriptor de seguridad de objeto como un puntero a una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Utilice este puntero con una función de control de acceso de Win32, como [**AccessCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheck) o [**BuildSecurityDescriptor**](/windows/desktop/api/aclapi/nf-aclapi-buildsecuritydescriptora). Para obtener más información y un ejemplo de código, vea [uso de IDirectoryObject para obtener un descriptor de seguridad](using-idirectoryobject-to-get-a-security-descriptor.md).

La técnica recomendada, y la que se usa en la mayoría de los ejemplos de código de esta guía, es usar las interfaces de **IADs \*** porque simplifican el control de los descriptores de seguridad, las ACL y las ACE. En el caso de los programadores de Visual Basic, las interfaces **IADs \*** son la manera más eficaz de controlar los descriptores de seguridad.

La técnica [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) es útil cuando se requiere una estructura de [**\_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) . Por ejemplo, el ejemplo de código de [comprobar un derecho de acceso a un control en la ACL de un objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md) usa este método para recuperar un descriptor de seguridad para pasarlo a la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) .

Para más información, consulte:

-   [Usar IADs para obtener un descriptor de seguridad](using-iads-to-get-a-security-descriptor.md)
-   [Uso de IDirectoryObject para obtener un descriptor de seguridad](using-idirectoryobject-to-get-a-security-descriptor.md)
-   [Componentes del descriptor de seguridad](security-descriptor-components.md)
-   [Recuperación de la DACL de un objeto](retrieving-an-objectampaposs-dacl.md)
-   [Recuperar la SACL de un objeto](retrieving-an-objectampaposs-sacl.md)
-   [Leer el descriptor de seguridad de un objeto](reading-an-objectampaposs-security-descriptor.md)
-   [Código de ejemplo para crear un descriptor de seguridad](example-code-for-creating-a-security-descriptor.md)
-   [Código de ejemplo para enumerar la ACL de un objeto en Active Directory Domain Services](example-code-for-enumerating-the-acl-of-an-active-directory-object.md)

 

 