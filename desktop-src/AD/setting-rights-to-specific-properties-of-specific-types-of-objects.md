---
title: Establecer derechos en propiedades específicas de tipos específicos de objetos
description: Los permisos específicos de la propiedad se pueden usar en combinación con la herencia específica del objeto para proporcionar la delegación eficaz y detallada de la administración.
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- establecimiento de derechos en propiedades específicas de tipos específicos de objetos de AD
- Active Directory, usar, seguridad, establecer derechos en propiedades específicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c01070b5c5b23e7524bd3b54293576e578861e0120b431e6dc95b7a5b4cc4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024743"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a>Establecer derechos en propiedades específicas de tipos específicos de objetos

Los permisos específicos de la propiedad se pueden usar en combinación con la herencia específica del objeto para proporcionar la delegación eficaz y detallada de la administración. Puede establecer una ACE heredable de objeto específica de la propiedad para permitir que un usuario o grupo especificado lea o escriba un atributo específico en una clase especificada de objetos secundarios en un contenedor. Por ejemplo, puede establecer una ACE en una unidad organizativa (OU) para permitir que un grupo lea y escriba el atributo de número de teléfono de todos los objetos de usuario de la unidad organizativa.

**Para establecer A ACE heredables de objetos específicos de la propiedad**

1.  Establezca [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT** o **ADS \_ ACETYPE ACCESS DENIED \_ \_ \_ OBJECT**.
2.  Establezca [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **el schemaIDGUID** del atributo. Por ejemplo, **el schemaIDGUID** del atributo **telephoneNumber** es {bf967a49-0de6-11d0-a285-00aa003049e2}.
3.  Establezca [**IADsAccessControlEntry.AceFlags en**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) **ADS \_ ACEFLAG INHERIT \_ \_ ACE**.
4.  Establezca [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **schemaIDGUID de** la clase de objeto que puede heredar la ACE. Por ejemplo, **el schemaIDGUID** de la clase **de** usuario es {bf967aba-0de6-11d0-a285-00aa003049e2}.
5.  Establezca [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT** y **ADS FLAG \_ \_ INHERITED OBJECT TYPE \_ \_ \_ PRESENT**.

> [!IMPORTANT]
> Establezca \_ ACEFLAG INHERIT ACE de ADS para que la ACE se \_ \_ herede. Además, establezca ADS ACEFLAG INHERIT ONLY ACE si el tipo de objeto al que se aplica esta ACE no coincide con el tipo de objeto del contenedor donde se \_ \_ especifica la \_ \_ ACE. Si esto no se hace, la ACE también se hará efectiva en el contenedor y puede conceder derechos inesperados.

 

Para obtener más información y ejemplos de código que se pueden usar para establecer este tipo de ACE, vea Ejemplo de código para establecer una [ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 