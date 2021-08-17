---
title: Extender el esquema
description: El Active Directory de servicio de directorio define los atributos y las clases usados en Active Directory Domain Services.
ms.assetid: 1c7c1fa7-56d9-4b2d-9c48-aa10464064bc
ms.tgt_platform: multiple
keywords:
- Active Directory, using,schema,extending the schema
- schema AD , extending the schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c50853e7b782f46b84212965c249ac90b685958c799c1b44cd366d5526e158d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189563"
---
# <a name="extending-the-schema"></a>Extender el esquema

El Active Directory de servicio de directorio define los atributos y las clases usados en Active Directory Domain Services. El esquema base que se incluye en el sistema contiene un amplio conjunto de definiciones de clase, como user **,** **computer** y **organizationalUnit,** y definiciones de atributo, como **userPrincipalName**, **telephoneNumber** y **objectSid.** El conjunto existente de clases y atributos será suficiente para la mayoría de las aplicaciones. Sin embargo, el esquema es extensible, lo que significa que puede definir nuevas clases y atributos. En esta sección se describe cómo extender el Active Directory esquema.

## <a name="when-to-extend-the-schema"></a>Cuándo extender el esquema

Si las clases y atributos existentes no se ajustan al tipo de datos que desea almacenar, debe extender el esquema. Es importante tener en cuenta que las adiciones de esquema son permanentes; puede deshabilitar clases y atributos, pero nunca puede quitarlos del esquema. Tenga esto en cuenta al probar el código.

Tenga en cuenta también el tamaño de los datos que desea almacenar. Microsoft recomienda que ningún valor de atributo supere los 500 kilobytes, incluida la suma de atributos de varios valores. Además, los objetos no deben superar los 1 megabytes de tamaño. Tenga en cuenta también el número de instancias de los datos; Si agrega un nuevo atributo a la clase [**User**](/windows/desktop/ADSchema/c-user) en un sistema que tiene 100 000 usuarios, esto puede usar un espacio considerable.

Los temas de esta sección incluyen:

-   Cómo enlazar al contenedor de esquema y leer las propiedades de las clases y atributos existentes.
-   Cómo y cuándo extender el esquema mediante la definición de nuevos atributos y clases.
-   Cómo instalar extensiones de esquema mediante LDIFDE, CSVDE o mediante programación con ADSI.

Para obtener más información y una introducción al esquema Active Directory, incluida la información sobre la implementación del esquema, las definiciones de clase y las definiciones de atributos, [vea Active Directory Schema](active-directory-schema.md).

Para obtener más información, incluidas las páginas de referencia para las clases de esquema predefinidas, atributos y sintaxis de atributos, vea la referencia de esquema de Active Directory en la Active Directory Domain Services [referencia](active-directory-domain-services-reference.md).

 

 