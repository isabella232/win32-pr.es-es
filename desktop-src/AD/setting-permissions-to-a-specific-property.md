---
title: Establecer permisos para una propiedad específica
description: Los permisos se pueden establecer para aplicarse a una propiedad específica de un objeto.
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- Establecer permisos para una propiedad específica AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077491"
---
# <a name="setting-permissions-to-a-specific-property"></a>Establecer permisos para una propiedad específica

Los permisos se pueden establecer para aplicarse a una propiedad específica de un objeto.

**Para establecer permisos que se aplican a una propiedad específica de un objeto**

1.  Establezca la propiedad [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ right \_ DS \_ Read \_ prop** y/o **ADS \_ right \_ DS \_ Write \_ prop**.
2.  Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.
3.  Establezca la propiedad [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** de la propiedad. Es el **schemaIDGUID** del objeto **attributeSchema** que define la propiedad en el esquema. El GUID debe especificarse como una cadena del formulario generado por la función [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) en la biblioteca com.
4.  Establezca [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **\_ tipo de objeto de marca ADS \_ \_ \_ presente**.

Para obtener más información sobre el **schemaIDGUID** de un atributo predefinido, vea [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md).

Para obtener más información y un ejemplo de código que se puede usar para recuperar un schemaIDGUID, vea [leer objetos attributeSchema y ClassSchema](reading-attributeschema-and-classschema-objects.md).

Para obtener más información sobre cómo crear una ACE, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE específica de la propiedad, consulte el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 