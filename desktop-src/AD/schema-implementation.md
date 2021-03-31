---
title: Implementación de esquema
description: En Active Directory Domain Services, las definiciones de clase y atributo se almacenan en el directorio como instancias de las clases classSchema y attributeSchema, respectivamente.
ms.assetid: 917f8e65-df2c-457e-bfd8-3f1ce0d0fbae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7ff18046841b5603be235266e33a7252049f93c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077496"
---
# <a name="schema-implementation"></a>Implementación de esquema

En Active Directory Domain Services, las definiciones de clase y atributo se almacenan en el directorio como instancias de las clases [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) y [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) , respectivamente. **ClassSchema** y **attributeSchema** son clases definidas en el esquema. Para manipular el esquema de Active Directory, utilice las mismas operaciones LDAP que se usan para manipular otro objeto. Dado que el esquema es una parte fundamental del directorio que afecta a todo el bosque, se aplican restricciones especiales a las extensiones de esquema. Para obtener más información sobre las restricciones, vea [restricciones en las extensiones de esquema](restrictions-on-schema-extension.md).

Para resumir la implementación del esquema:

-   Las instancias de la clase [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) definen cada clase de objeto compatible con Active Directory Domain Services. Los atributos de un objeto **ClassSchema** , por ejemplo, sus [**atributos mayContain**](/windows/desktop/ADSchema/a-maycontain) y [**mustContain**](/windows/desktop/ADSchema/a-mustcontain) , describen una clase de objeto, de la misma forma que los atributos de un objeto de usuario, por ejemplo, los atributos [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) y [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) , describen dicho usuario. Para obtener más información, vea [características de las clases de objeto](characteristics-of-object-classes.md).
-   Las instancias de la clase [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) se utilizan para definir todos los atributos admitidos por Active Directory Domain Services. Los atributos de un objeto **attributeSchema** , por ejemplo, sus atributos **attributeSyntax** y **isSingleValued** , describen un atributo, de la misma forma que los atributos de un objeto de usuario describen dicho usuario. Para obtener más información, vea [características de los atributos](characteristics-of-attributes.md).
-   Las instancias de las clases [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) y [**ClassSchema**](/windows/desktop/ADSchema/c-classschema) se almacenan en un lugar conocido en el directorio, el contenedor de esquemas. El contenedor de esquemas siempre tiene un nombre distintivo con el formato:

    ```C++
    CN=Schema,CN=Configuration,<DC=forestroot>
    ```

    

    donde " &lt; DC = forestroot &gt; " es el nombre distintivo de la raíz del bosque, por ejemplo, "DC = Fabrikam, DC = com".

    Para obtener el nombre distintivo del contenedor de esquemas, lea el atributo **schemaNamingContext** de RootDSE. Para obtener más información acerca de rootDSE y sus atributos, vea [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).

Cuando piense en el esquema, recuerde:

-   Los cambios de esquema son globales. Hay un único esquema para todo el bosque. El esquema se replica globalmente: existe una copia del esquema en cada controlador de dominio del bosque. Al extender el esquema, lo hace para todo el bosque.
-   Las adiciones de esquema no son reversibles. Cuando se agrega una nueva clase o atributo al esquema, no se puede quitar. Un atributo o clase existente se puede deshabilitar, pero no se puede quitar. Para obtener más información, vea [deshabilitar clases y atributos existentes](disabling-existing-classes-and-attributes.md).
-   Deshabilitar una clase o atributo no afecta a las instancias existentes de la clase o atributo, pero impide que se creen instancias nuevas. No se puede deshabilitar un atributo si está incluido en una clase que no está deshabilitada.

 

 