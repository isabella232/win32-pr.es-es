---
title: Componentes del descriptor de seguridad
description: Tras usar el método IADs. Get para recuperar un puntero de interfaz IADsSecurityDescriptor, puede utilizar las propiedades IADsSecurityDescriptor para leer o escribir los componentes del descriptor de seguridad de un objeto de directorio.
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- Componentes del descriptor de seguridad AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef87b0e23f60fdbb4d0b03b421012d5918ed3c83
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789466"
---
# <a name="security-descriptor-components"></a>Componentes del descriptor de seguridad

Tras usar el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar un puntero de interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) , puede utilizar las propiedades **IADsSecurityDescriptor** para leer o escribir los componentes del descriptor de seguridad de un objeto de directorio. Por ejemplo, para obtener o establecer la DACL del objeto, use la propiedad [**DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) .

Un descriptor de seguridad puede almacenar los datos siguientes:

-   Un identificador de seguridad (SID) que identifica al propietario del objeto: el propietario de un objeto tiene el derecho implícito para modificar los datos de la DACL y del propietario en el descriptor de seguridad del objeto.
-   Una lista de control de acceso discrecional (DACL) que identifica a los usuarios y grupos que pueden realizar varias operaciones en el objeto: una DACL contiene una lista de entradas de control de acceso (ACE). Cada ACE permite o deniega un conjunto de derechos de acceso especificado para una cuenta de usuario, una cuenta de grupo o cualquier otro administrador de confianza especificados. Para obtener más información, vea [recuperar la DACL de un objeto](retrieving-an-objectampaposs-dacl.md).
-   Una lista de control de acceso de sistema (SACL) que controla el modo en que las auditorías del sistema intentan obtener acceso al objeto: cada ACE de una SACL especifica los tipos de intentos de acceso que generan una entrada de registro de auditoría para una cuenta de usuario, una cuenta de grupo u otro administrador de confianza especificados. Para obtener más información, vea [recuperar la SACL de un objeto](retrieving-an-objectampaposs-sacl.md).
-   Un conjunto de marcas de control de **\_ descriptor \_ de seguridad** que califican el significado de un descriptor de seguridad o sus componentes: por ejemplo, la marca de **\_ DACL \_ protegida** del descriptor de seguridad evita que se hereden las ACE de su objeto primario.
-   Un identificador de seguridad (SID) que identifica el grupo primario del objeto: Active Directory Domain Services no usar este componente.

Para obtener más información y un ejemplo de código que se puede usar para leer y mostrar los datos en un descriptor de seguridad de objeto y DACL, vea [leer el descriptor de seguridad de un objeto](reading-an-objectampaposs-security-descriptor.md).

 

 