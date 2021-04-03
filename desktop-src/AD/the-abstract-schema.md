---
title: El esquema abstracto
description: El contenedor de esquemas contiene todos los objetos classSchema y attributeSchema que definen las clases y los atributos que pueden existir en un bosque de directorio.
ms.assetid: 688fccf7-37ce-4eea-b4ff-b0b3223a964e
ms.tgt_platform: multiple
keywords:
- El esquema abstracto de AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9123c72cc4cc38eafa77e0ad0c6384940667e54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075096"
---
# <a name="the-abstract-schema"></a>El esquema abstracto

El contenedor de esquemas contiene todos los objetos **ClassSchema** y **attributeSchema** que definen las clases y los atributos que pueden existir en un bosque de directorio. El contenedor de esquemas también contiene un objeto denominado agregado de **subesquema** de clase. Este objeto de **subesquema** se conoce como esquema abstracto.

El esquema abstracto contiene un subconjunto de los datos almacenados en los objetos **ClassSchema** y **attributeSchema** . Su finalidad es proporcionar un mecanismo sencillo y eficaz para recuperar los elementos usados con frecuencia de las definiciones de clase y atributo. Por ejemplo, para recuperar los atributos opcionales y obligatorios de una clase de objeto, enlace a varios objetos para recopilar los valores **mayContain**, **mustContain**, **systemMayContain** y **systemMustContain** de la clase y todas sus superclases, así como de las clases auxiliares de la clase y sus superclases. El esquema abstracto recopila de forma cómoda todos estos datos en un solo objeto.

Como con cualquier objeto de Active Directory Domain Services, puede enlazar con el objeto de **subesquema** y leer sus atributos, analizando los valores de cadena para recuperar los datos deseados. Sin embargo, ADSI proporciona un conjunto de interfaces que facilitan la lectura del esquema abstracto. Para obtener más información, vea [leer el esquema abstracto](reading-the-abstract-schema.md).

En la tabla siguiente se enumeran los atributos clave de un objeto de **subesquema** .



| Atributo                 | Descripción                                                                                                                                                                                                                                                                               |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **attributeTypes**        | Atributo de varios valores que contiene cadenas que representan cada atributo del esquema. Cada valor contiene el **attributeID**, **lDAPDisplayName**, **attributeSyntax**, **rangeLower**, **rangeUpper** y un elemento que indica si el atributo puede tener varios valores. |
| **extendedAttributeInfo** | Un atributo con varios valores que contiene cadenas que representan datos adicionales para cada atributo. Cada valor contiene los valores **attributeID**, **lDAPDisplayName**, **schemaIDGUID** y **attributeSecurityGUID**.                                                                          |
| **extendedClassInfo**     | Un atributo con varios valores que contiene cadenas que representan datos adicionales para cada clase. Cada valor contiene los **governsID**, **lDAPDisplayName** y **schemaIDGUID** de la clase.                                                                                              |
| **objectClasses**         | Un atributo con varios valores que contiene cadenas que representan cada clase en el esquema. Cada valor contiene los valores **governsID**, **lDAPDisplayName**, **mustContain**, **mayContain**, etc.                                                                                           |



 

 

 




