---
title: Leer el esquema abstracto
description: En este tema se proporciona un ejemplo de código e instrucciones para leer desde el esquema abstracto, que proporciona un subconjunto de los datos almacenados en los objetos attributeSchema y classSchema en el contenedor de esquema.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- esquema Active Directory , leer el esquema abstracto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7095dc4fb5ffe5f11f64781ecd423a60b3d434d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881303"
---
# <a name="reading-the-abstract-schema"></a>Leer el esquema abstracto

En este tema se proporciona un ejemplo de código e instrucciones para leer desde el esquema abstracto, que proporciona un subconjunto de los datos almacenados en los objetos **attributeSchema** y **classSchema** en el contenedor de esquema. Para recuperar datos que no están disponibles en el esquema abstracto, lea los datos directamente desde el contenedor de esquemas como se describe en Lectura de attributeSchema y [classSchema Objects](reading-attributeschema-and-classschema-objects.md).

Use la cadena de enlace "LDAP://schema" para enlazar a un [**puntero IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) en el esquema abstracto. Use este puntero para enumerar las entradas de clase, atributo y sintaxis en el esquema abstracto. También puede usar el [**método IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) para recuperar entradas individuales.


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



Use una cadena de enlace similar, "LDAP://schema/ objeto ", para enlazar directamente a una entrada de clase &lt; o atributo en el esquema &gt; abstracto. En esta cadena, " &lt; object " es el &gt; **lDAPDisplayName** de una clase o atributo. Para las clases enlazan a [**la interfaz IADsClass;**](/windows/desktop/api/iads/nn-iads-iadsclass) para atributos, enlace a [**la interfaz IADsProperty.**](/windows/desktop/api/iads/nn-iads-iadsproperty)


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



Además, la [**interfaz IADs**](/windows/desktop/api/iads/nn-iads-iads) proporciona [**la propiedad IADs.Schema.**](/windows/desktop/ADSI/iads-property-methods) Esta propiedad devuelve ADsPath para la clase de objeto en formato de cadena de enlace de esquema abstracto. Si tiene un puntero **IAD a** un objeto , puede enlazar a su clase en el esquema abstracto mediante el ADsPath devuelto de **IADs.Schema**.

Para las clases, en la tabla siguiente se enumeran las propiedades clave proporcionadas por el esquema abstracto.



| Propiedad                                                             | Significado                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass.Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Indica si se trata de una clase abstracta.                                                                                                                                                                                                                                            |
| [**IADsClass.Auxiliary**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica si se trata de una clase auxiliar.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Matriz de clases auxiliares de la que se deriva esta clase.                                                                                                                                                                                                                                     |
| [**IADsClass.Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica si los objetos de esta clase pueden contener otros objetos, lo que es cierto si alguna clase incluye esta clase en su lista de **posiblesSuperiors**.                                                                                                                                 |
| [**IADsClass.DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Matriz de clases de las que se deriva esta clase.                                                                                                                                                                                                                                       |
| [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Recupera una matriz de las propiedades obligatorias que se deben establecer para una instancia de la clase . La lista devuelta incluye todos los valores **mustContain** y **systemMustContain** para la clase y las clases de las que se deriva, incluidas las superclases y las clases auxiliares. |
| [**IADsClass.OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Recupera el governsID de la clase .                                                                                                                                                                                                                                                   |
| [**IADsClass.OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Recupera una matriz de las propiedades opcionales que se pueden establecer para una instancia de la clase . La lista devuelta incluye todos los valores **mayContain** y **systemMayContain** de la clase y las clases de las que se deriva, incluidas las superclases y las clases auxiliares.   |
| [**IADsClass.PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Recupera una matriz de los valores **de possibleSuperiors** para la clase , que indica las clases de objeto que pueden contener objetos de esta clase.                                                                                                                                        |



 

El esquema abstracto se almacena en el **objeto subSchema** en el contenedor de esquema. Para obtener el nombre distintivo del objeto **subSchema,** enlace a rootDSE y lea el atributo **subSchemaSubEntry,** como se describe en Enlace sin servidor y [RootDSE](serverless-binding-and-rootdse.md). Tenga en cuenta que es más eficaz leer el esquema abstracto enlazando a "LDAP://schema", que enlazando directamente al **objeto subSchema.**

 

 
