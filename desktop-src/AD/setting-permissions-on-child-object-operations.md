---
title: Establecer permisos en operaciones de objetos secundarios
description: Los permisos, como Crear elemento secundario y Eliminar elemento secundario, también se pueden conceder o denegar para las operaciones en todos los subobjetos o subobjetos de una clase específica.
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- Establecer permisos en operaciones de objetos secundarios ad
- objetos AD , secundario, establecer permisos en operaciones de objetos secundarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f136119d5e61ea312748d5cd64cabb8c0aee0b651d8b192519dc2d74e2045cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024773"
---
# <a name="setting-permissions-on-child-object-operations"></a>Establecer permisos en operaciones de objetos secundarios

Los permisos, como Crear elemento secundario y Eliminar elemento secundario, también se pueden conceder o denegar para las operaciones en todos los subobjetos o subobjetos de una clase específica.

El siguiente procedimiento se puede usar para establecer permisos para un tipo de subobjeto específico.

**Para establecer permisos para un tipo de subobjeto específico**

1.  Establezca la [**propiedad IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS \_ ACETYPE ACCESS ALLOWED \_ \_ \_ OBJECT** o **ADS \_ ACETYPE ACCESS DENIED \_ \_ \_ OBJECT**.
2.  Establezca la [**propiedad IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en el GUID de la clase de objeto. Esta es la **propiedad schemaIDGUID** del objeto classSchema que define la clase de objeto. Si la **propiedad ObjectType** **es NULL,** la ACE se aplica a los subobjetos de cualquier clase.
3.  Establezca la [**propiedad IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) en **ADS FLAG OBJECT TYPE \_ \_ \_ \_ PRESENT**.

Para obtener más información y un procedimiento para crear una ACE, vea [Establecer los derechos de acceso en un objeto](setting-access-rights-on-an-object.md).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE que controla las operaciones de objetos secundarios, vea Ejemplo de código para establecer una [ACE en un objeto de directorio](example-code-for-setting-an-ace-on-a-directory-object.md).

 

 