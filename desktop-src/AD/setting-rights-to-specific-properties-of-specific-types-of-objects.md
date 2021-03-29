---
title: Establecer derechos en propiedades específicas de tipos específicos de objetos
description: Los permisos específicos de la propiedad se pueden usar en combinación con la herencia específica del objeto para proporcionar la delegación eficaz y detallada de la administración.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- establecer derechos en propiedades específicas de tipos específicos de objetos AD
- Active Directory, usar, seguridad, establecer derechos en propiedades específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487391"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Establecer derechos en propiedades específicas de tipos específicos de objetos

Los permisos específicos de la propiedad se pueden usar en combinación con la herencia específica del objeto para proporcionar la delegación eficaz y detallada de la administración. Puede establecer una ACE heredable de objeto específico de la propiedad para permitir que un usuario o grupo especificado lea o escriba un atributo específico en una clase especificada de objetos secundarios en un contenedor. Por ejemplo, puede establecer una ACE en una unidad organizativa (OU) para permitir que un grupo Lea y escriba el atributo de número de teléfono de todos los objetos de usuario en la unidad organizativa.

**Para establecer ACE que se puedan heredar del objeto específico de la propiedad**

1.  Establezca [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.
2.  Establezca [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** del atributo. Por ejemplo, el **schemaIDGUID** del atributo **telephoneNumber** es {bf967a49-0de6-11d0-A285-00aa003049e2}.
3.  Establezca [**IADsAccessControlEntry. AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ ACEFLAG \_ inherit \_ ACE**.
4.  Establezca [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **schemaIDGUID** de la clase de objeto que puede heredar la ACE. Por ejemplo, el **schemaIDGUID** de la clase **User** es {bf967aba-0de6-11d0-A285-00aa003049e2}.
5.  Establezca [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **\_ tipo de objeto de marca ADS \_ \_ \_ presente** y el **tipo de \_ \_ objeto heredado de marca de anuncios \_ \_ \_ presente**.

> [!IMPORTANT]
> Establezca ad \_ ACEFLAG \_ inherit \_ ACE para que la ACE se herede. Además, Set ADS \_ ACEFLAG \_ solo hereda \_ \_ ACE si el tipo de objeto al que se aplica esta ACE no coincide con el tipo de objeto del contenedor en el que se especifica la ACE. Si no se hace esto, la ACE también entrará en vigor en el contenedor y podrá conceder derechos inesperados.

 

Para obtener más información y ejemplos de código que se pueden usar para establecer este tipo de ACE, vea el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 