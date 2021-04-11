---
title: Sintaxis para los atributos de Active Directory Domain Services
description: Active Directory Domain Services definir un conjunto de sintaxis de atributo para especificar el tipo de datos que contiene un atributo.
ms.assetid: 79d27d47-5d03-4ad6-bf97-c387c34fa454
ms.tgt_platform: multiple
keywords:
- Sintaxis para Active Directory Domain Services atributos Active Directory
- Atributos Active Directory, sintaxis para
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04386e1b4981a81585fe208afa4cca6ed02d4c3c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149160"
---
# <a name="syntaxes-for-attributes-in-active-directory-domain-services"></a>Sintaxis para los atributos de Active Directory Domain Services

Active Directory Domain Services definir un conjunto de sintaxis de atributo para especificar el tipo de datos que contiene un atributo. En realidad, las sintaxis predefinidas no aparecen en el directorio y no se pueden agregar nuevas sintaxis. Se pueden usar varios métodos para identificar la sintaxis de una clase de atributo:

-   Los métodos [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get), [**IADs. GETEX**](/windows/desktop/api/iads/nf-iads-iads-getex), [**IADs. put**](/windows/desktop/api/iads/nf-iads-iads-put)y [**IADs. PutEx**](/windows/desktop/api/iads/nf-iads-iads-putex) usan la estructura [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) para obtener y establecer los valores de los atributos de un objeto. El miembro **VT** de esta estructura es un valor de **VARTYPE** que identifica el tipo de datos.
-   Los métodos de las interfaces [**IDirectoryObject**](/windows/desktop/api/iads/nn-iads-idirectoryobject) y [**IDirectorySearch**](/windows/desktop/api/iads/nn-iads-idirectorysearch) usan un valor de la enumeración [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) para especificar el tipo de datos.
-   Para especificar la sintaxis de una nueva clase de atributo, establezca los atributos [**attributeSyntax**](/windows/desktop/ADSchema/a-attributesyntax) y [**oMSyntax**](/windows/desktop/ADSchema/a-omsyntax) de un objeto [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) . Si el valor de **oMSyntax** es 127, también debe establecer el atributo [**oMObjectClass**](/windows/desktop/ADSchema/a-omobjectclass) . Para obtener más información, vea [elegir una sintaxis](choosing-a-syntax.md).

Para obtener una lista completa de las sintaxis que proporciona Active Directory Domain Services, incluidos los valores de **VARTYPE** y [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum) correspondientes de cada sintaxis, vea [Sintaxis](/windows/desktop/ADSchema/syntaxes).

 

 