---
title: Extender el esquema
description: El esquema del servicio de directorio de Active Directory define los atributos y las clases que se usan en Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, usar, esquema, extender el esquema
- esquema AD, extensión del esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c03d57468fb5275c55ce0d725a2decd7cfbf0f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656340"
---
# <a name="extending-the-schema"></a>Extender el esquema

El esquema del servicio de directorio de Active Directory define los atributos y las clases que se usan en Active Directory Domain Services. El esquema base incluido en el sistema contiene un conjunto completo de definiciones de clase, como **User**, **Computer** y **organizationalUnit**, y definiciones de atributos, como **userPrincipalName**, **telephoneNumber** y **objectSid**. El conjunto existente de clases y atributos será suficiente para la mayoría de las aplicaciones. Sin embargo, el esquema es extensible, lo que significa que puede definir nuevas clases y atributos. En esta sección se describe cómo extender el esquema de Active Directory.

## <a name="when-to-extend-the-schema"></a>Cuándo extender el esquema

Si las clases y los atributos existentes no se ajustan al tipo de datos que desea almacenar, debe extender el esquema. Es importante tener en cuenta que las adiciones de esquema son permanentes; puede deshabilitar clases y atributos, pero nunca puede quitarlos del esquema. Tenga esto en cuenta al probar el código.

También tenga en cuenta el tamaño de los datos que desea almacenar. Microsoft recomienda que ningún valor de atributo supere los 500 kilobytes, incluida la suma de los atributos multivalor. Además, los objetos no deben tener un tamaño superior a 1 megabyte. Considere también el número de instancias de los datos; Si agrega un nuevo atributo a la clase de [**usuario**](/windows/desktop/ADSchema/c-user) en un sistema que tiene 100.000 usuarios, puede usar un espacio considerable.

Los temas de esta sección incluyen:

-   Cómo enlazar con el contenedor de esquema y leer las propiedades de las clases y atributos existentes.
-   Cómo y cuándo extender el esquema definiendo nuevos atributos y clases.
-   Cómo instalar extensiones de esquema mediante LDIFDE, CSVDE o mediante programación con ADSI.

Para obtener más información y una información general sobre el esquema de Active Directory, incluida la información sobre la implementación del esquema, las definiciones de clase y las definiciones de atributo, vea [Active Directory esquema](active-directory-schema.md).

Para obtener más información, incluidas las páginas de referencia de las clases de esquema predefinidas, los atributos y las sintaxis de atributo, vea la referencia de esquemas de Active Directory en la [referencia de Active Directory Domain Services](active-directory-domain-services-reference.md).

 

 