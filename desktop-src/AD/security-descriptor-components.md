---
title: Componentes del descriptor de seguridad
description: Después de usar el método IADs.Get para recuperar un puntero de interfaz IADsSecurityDescriptor, puede usar las propiedades IADsSecurityDescriptor para leer o escribir los componentes del descriptor de seguridad de un objeto de directorio.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- Componentes del descriptor de seguridad de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34aa5ec61507e56c03bcc3809a2a5eebcb2cbcd36e18f63119aca53448c8a0b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024923"
---
# <a name="security-descriptor-components"></a>Componentes del descriptor de seguridad

Después de usar el método [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar un puntero de interfaz [**IADsSecurityDescriptor,**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) puede usar las propiedades **IADsSecurityDescriptor** para leer o escribir los componentes del descriptor de seguridad de un objeto de directorio. Por ejemplo, para obtener o establecer la DACL del objeto, use la [**propiedad DiscretionaryAcl.**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods)

Un descriptor de seguridad puede almacenar los datos siguientes:

-   Identificador de seguridad (SID) que identifica el propietario del objeto: el propietario de un objeto tiene el derecho implícito de modificar la DACL y los datos de propietario en el descriptor de seguridad del objeto.
-   Una lista de control de acceso discrecional (DACL) que identifica los usuarios y grupos que pueden realizar varias operaciones en el objeto: una DACL contiene una lista de entradas de control de acceso (ACE). Cada ACE permite o deniega un conjunto especificado de derechos de acceso a una cuenta de usuario, cuenta de grupo u otro administrador de confianza especificados. Para obtener más información, [vea Retrieving an Object's DACL](retrieving-an-objectampaposs-dacl.md).
-   Una lista de control de acceso del sistema (SACL) que controla cómo las auditorías del sistema intentan acceder al objeto: cada ACE de una SACL especifica los tipos de intentos de acceso que generan una entrada de registro de auditoría para una cuenta de usuario, cuenta de grupo u otro administrador de confianza especificados. Para obtener más información, [vea Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md).
-   Conjunto de marcas de **\_ control DE \_ DESCRIPTOR** DE SEGURIDAD que califican el significado de un descriptor de seguridad o sus componentes: por ejemplo, la marca DACL PROTECTED de SE protege la **\_ DACL \_** del descriptor de seguridad de heredar las ACE de su objeto primario.
-   Identificador de seguridad (SID) que identifica el grupo principal del objeto: Active Directory Domain Services no utilice este componente.

Para obtener más información y un ejemplo de código que se puede usar para leer y mostrar los datos en un descriptor de seguridad de objetos y DACL, vea Leer el [descriptor de seguridad de un objeto](reading-an-objectampaposs-security-descriptor.md).

 

 