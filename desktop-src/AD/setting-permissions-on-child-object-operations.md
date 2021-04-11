---
title: Establecer permisos en operaciones de objetos secundarios
description: También se pueden conceder o denegar permisos, como crear elemento secundario y eliminar secundario, para operaciones en todos los subobjetos o subobjetos de una clase específica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Establecer permisos en operaciones de objetos secundarios AD
- objetos AD, Child, establecimiento de permisos en operaciones de objetos secundarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104149163"
---
# <a name="setting-permissions-on-child-object-operations"></a>Establecer permisos en operaciones de objetos secundarios

También se pueden conceder o denegar permisos, como crear elemento secundario y eliminar secundario, para operaciones en todos los subobjetos o subobjetos de una clase específica.

El siguiente procedimiento se puede usar para establecer permisos para un tipo de subobjeto específico.

**Para establecer permisos para un tipo de subobjeto específico**

1.  Establezca la propiedad [**IADsAccessControlEntry. AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ AceType \_ acceso \_ a \_ objetos permitidos** o **anuncios \_ AceType \_ acceso \_ denegado \_**.
2.  Establezca la propiedad [**IADsAccessControlEntry. ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el GUID de la clase de objeto. Esta es la propiedad **schemaIDGUID** del objeto ClassSchema que define la clase de objeto. Si la propiedad **objecttype** es **null**, la ACE se aplica a los subobjetos de cualquier clase.
3.  Establezca la propiedad [**IADsAccessControlEntry. Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el **tipo de \_ objeto marca de ADS \_ \_ \_ presente**.

Para obtener más información y un procedimiento para crear una ACE, vea [establecer derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE que controla las operaciones de objetos secundarios, vea el [código de ejemplo para establecer una ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 