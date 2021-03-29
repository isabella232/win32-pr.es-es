---
title: Definir una nueva clase
description: Al definir una nueva clase, especifique las clases principales válidas de la nueva clase, es decir, las clases que pueden contener instancias de la nueva clase.
ms.assetid: 24e346b3-2de2-41f9-a0a2-7b7d8ab5668b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 069d6c0ede945c39a00111cd43ece8257031b3aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993914"
---
# <a name="defining-a-new-class"></a>Definir una nueva clase

Al definir una nueva clase, especifique las clases principales válidas de la nueva clase, es decir, las clases que pueden contener instancias de la nueva clase. Las clases principales válidas se especifican en los atributos **possSuperiors** y **systemPossSuperiors** de la nueva clase, así como en las posibles superiores heredadas de sus superclases, pero no de las clases auxiliares.

Ser específico al definir las clases principales válidas para la nueva clase. Decida dónde desea que los usuarios creen instancias de la clase. Por ejemplo, si se especifica "Container" como primario legal, el usuario podrá crear instancias en cualquiera de los contenedores estándar (**Container**, **organizationalUnit**, etc.), mientras que si se especifica "Computer", solo se pueden crear instancias en instancias del objeto **Computer** .

**Para crear una clase**

1.  Elija un nombre para la clase. Para obtener más información sobre la creación de un nombre común y un nombre para mostrar de LDAP para una nueva clase, vea [asignar nombres a los atributos y las clases](naming-attributes-and-classes.md).
2.  Obtener un identificador de objeto (OID) para la clase. Para obtener más información, vea [obtener un identificador de objeto](obtaining-an-object-identifier.md).
3.  Elija una "categoría de objeto predeterminada" para la clase. Para obtener más información, vea [clase de objeto y categoría de objeto](object-class-and-object-category.md).
4.  Elija una "categoría de clase de objeto" para la clase. Indica si la clase es abstracta, estructural o auxiliar. Para obtener más información, vea [clases estructurales, abstractas y auxiliares](structural-abstract-and-auxiliary-classes.md).
5.  Cree un nuevo objeto **ClassSchema** . Se pueden establecer muchos atributos para un objeto **ClassSchema** . Los atributos siguientes son fundamentales para la definición de una nueva clase:

    -   Clases de las que hereda la nueva clase: **Subclasen**, **auxiliaryClass** y **systemAuxiliaryClass**
    -   Nombres e identificadores de la nueva clase: **CN**, **lDAPDisplayName**, **adminDisplayName**, **schemaIDGUID**, **governsID**
    -   Posibles atributos de la nueva clase: **mustContain**, **systemMustContain**, **mayContain**, **systemMayContain**
    -   Posibles elementos primarios de la nueva clase: **possSuperiors**, **systemPossSuperiors**
    -   **objectClassCategory**
    -   **defaultObjectCategory**
    -   **defaultHidingValue**
    -   **rDnAttId**
    -   **defaultSecurityDescriptor**
    -   **Descripción** (opcional)

    Para obtener más información y descripciones de estos atributos, vea [características de las clases de objeto](characteristics-of-object-classes.md).

    Tenga en cuenta que las clases especificadas en **subclasse**, **possSuperiors**, **systemPossSuperiors**, **auxiliaryClass** y **systemAuxiliaryClass** deben existir cuando la nueva clase se escribe en el directorio. de lo contrario, el objeto **ClassSchema** no se agregará al directorio. De forma similar, los atributos especificados en **mustContain**, **systemMustContain**, **mayContain** y **systemMayContain** deben existir o se producirá un error en la operación de creación de clases.

6.  Escriba el nuevo objeto **ClassSchema** en el directorio.

**Para agregar un atributo a la propiedad mayContain**

1.  Obtenga el objeto **ClassSchema** de la clase que se va a modificar.
2.  Agregue el nuevo atributo a la propiedad de varios valores de **mayContain** .
3.  Vuelva a escribir el objeto **ClassSchema** cambiado en el directorio.

Se pueden crear nuevos atributos al mismo tiempo que las clases nuevas; es importante el orden de creación de los nuevos atributos y clases. Para obtener más información, consulte [lo que debe hacer la instalación](what-the-installation-must-do.md).

**Para agregar nuevos atributos y clases nuevas al mismo tiempo**

1.  Defina primero todos los nuevos atributos. Para obtener más información, vea [definir un nuevo atributo](defining-a-new-attribute.md).
2.  Actualice la caché de esquema antes de definir nuevas clases. Para obtener más información, vea [actualizar la caché de esquema](updating-the-schema-cache.md).
3.  Cree las clases nuevas.
4.  Agregue los atributos deseados a las nuevas clases.
5.  Vuelva a actualizar la caché de esquema.

 

 




