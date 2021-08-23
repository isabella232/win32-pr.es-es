---
title: Implementación del esquema
description: En Active Directory Domain Services, las definiciones de clase y atributo se almacenan en el directorio como instancias de las clases classSchema y attributeSchema, respectivamente.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d35d29b4e10d27b1369c0f064e17a0ed4430cbe2d6cc59329380724cd444e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025023"
---
# <a name="schema-implementation"></a>Implementación del esquema

En Active Directory Domain Services, las definiciones de clase y atributo se almacenan en el directorio como instancias de las clases [**classSchema**](/windows/desktop/ADSchema/c-classschema) y [**attributeSchema,**](/windows/desktop/ADSchema/c-attributeschema) respectivamente. **classSchema** y **attributeSchema** son clases definidas en el esquema. Para manipular el esquema Active Directory, use las mismas operaciones LDAP usadas para manipular otro objeto. Dado que el esquema es una parte clave del directorio que afecta a todo el bosque, se aplican restricciones especiales a las extensiones de esquema. Para obtener más información sobre las restricciones, vea [Restricciones en las extensiones de esquema.](restrictions-on-schema-extension.md)

Para resumir la implementación del esquema:

-   Las instancias de la [**clase classSchema**](/windows/desktop/ADSchema/c-classschema) definen todas las clases de objeto admitidas por Active Directory Domain Services. Los atributos de un objeto **classSchema,** por ejemplo, sus atributos [**mayContain**](/windows/desktop/ADSchema/a-maycontain) y [**mustContain,**](/windows/desktop/ADSchema/a-mustcontain) describen una clase de objeto de la misma manera que los atributos de un objeto de usuario, por ejemplo, sus atributos [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) y [**telephoneNumber,**](/windows/desktop/ADSchema/a-telephonenumber) describen a ese usuario. Para obtener más información, vea [Características de las clases de objeto](characteristics-of-object-classes.md).
-   Las instancias de la [**clase attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) se usan para definir todos los atributos admitidos por Active Directory Domain Services. Los atributos de un objeto **attributeSchema,** por ejemplo, sus atributos **attributeSyntax** e **isSingleValued,** describen un atributo de la misma manera que los atributos de un objeto de usuario describen a ese usuario. Para obtener más información, vea [Características de los atributos](characteristics-of-attributes.md).
-   Las instancias de las [**clases attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) y [**classSchema**](/windows/desktop/ADSchema/c-classschema) se almacenan en un lugar conocido del directorio, el contenedor de esquema. El contenedor de esquemas siempre tiene un nombre distintivo del formulario:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    donde " DC=forestroot " es el nombre distintivo de la raíz del bosque, por &lt; &gt; ejemplo, "DC=Fabrikam,DC=Com".

    Para obtener el nombre distintivo del contenedor de esquemas, lea el atributo **schemaNamingContext** de rootDSE. Para obtener más información sobre rootDSE y sus atributos, vea [Enlace sin servidor y RootDSE.](serverless-binding-and-rootdse.md)

Al pensar en el esquema, recuerde:

-   Los cambios de esquema son globales. Hay un único esquema para todo un bosque. El esquema se replica globalmente: existe una copia del esquema en cada controlador de dominio del bosque. Al extender el esquema, lo hace para todo el bosque.
-   Las adiciones de esquema no son reversibles. Cuando se agrega una nueva clase o atributo al esquema, no se puede quitar. Se puede deshabilitar un atributo o clase existentes, pero no quitarse. Para obtener más información, [vea Deshabilitar clases y atributos existentes.](disabling-existing-classes-and-attributes.md)
-   Deshabilitar una clase o atributo no afecta a las instancias existentes de la clase o atributo, pero impide que se creen nuevas instancias. No se puede deshabilitar un atributo si se incluye en cualquier clase que no esté deshabilitada.

 

 