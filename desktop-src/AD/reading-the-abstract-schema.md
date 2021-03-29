---
title: Leer el esquema abstracto
description: En este tema se proporcionan ejemplos de código y directrices para leer desde el esquema abstracto, que proporciona un subconjunto de los datos almacenados en los objetos attributeSchema y classSchema del contenedor de esquemas.
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- esquema Active Directory, leer el esquema abstracto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904473"
---
# <a name="reading-the-abstract-schema"></a>Leer el esquema abstracto

En este tema se proporcionan ejemplos de código y directrices para leer desde el esquema abstracto, que proporciona un subconjunto de los datos almacenados en los objetos **attributeSchema** y **ClassSchema** del contenedor de esquemas. Para recuperar datos que no están disponibles en el esquema abstracto, lea directamente los datos desde el contenedor de esquemas, tal y como se describe en [leer objetos attributeSchema y ClassSchema](reading-attributeschema-and-classschema-objects.md).

Use la cadena de enlace "LDAP://schema" para enlazar con un puntero [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) en el esquema abstracto. Utilice este puntero para enumerar las entradas de la clase, el atributo y la sintaxis en el esquema abstracto. También puede utilizar el método [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) para recuperar entradas individuales.


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



Use una cadena de enlace similar, "LDAP://schema/ <object> ", para enlazar directamente a una entrada de clase o atributo en el esquema abstracto. En esta cadena, " &lt; Object &gt; " es el **lDAPDisplayName** de una clase o un atributo. Para las clases que se enlazan a la interfaz [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; en el caso de los atributos, enlace a la interfaz [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .


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



Además, la interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) proporciona la propiedad [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) . Esta propiedad devuelve el ADsPath de la clase de objeto en el formato de cadena de enlace del esquema abstracto. Si tiene un puntero **IADs** a un objeto, puede enlazar a su clase en el esquema abstracto mediante el ADsPath devuelto desde **IADs. Schema**.

En el caso de las clases, en la tabla siguiente se enumeran las propiedades clave proporcionadas por el esquema abstracto.



| Propiedad                                                             | Significado                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsClass. Abstract**](/windows/desktop/ADSI/iadsclass-property-methods)            | Indica si se trata de una clase abstracta.                                                                                                                                                                                                                                            |
| [**IADsClass. auxiliar**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica si se trata de una clase auxiliar.                                                                                                                                                                                                                                           |
| [**IADsClass.AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | Matriz de clases auxiliares de las que se deriva esta clase.                                                                                                                                                                                                                                     |
| [**IADsClass. Container**](/windows/desktop/ADSI/iadsclass-property-methods)           | Indica si los objetos de esta clase pueden contener otros objetos, que es true si alguna clase incluye esta clase en su lista de **possibleSuperiors**.                                                                                                                                 |
| [**IADsClass.DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | Matriz de clases de las que se deriva esta clase.                                                                                                                                                                                                                                       |
| [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | Recupera una matriz de las propiedades obligatorias que se deben establecer para una instancia de la clase. La lista devuelta incluye todos los valores **mustContain** y **systemMustContain** de la clase y las clases de las que se deriva, incluidas las superclases y las clases auxiliares. |
| [**IADsClass. OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | Recupera el governsID de la clase.                                                                                                                                                                                                                                                   |
| [**IADsClass. OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | Recupera una matriz de las propiedades opcionales que se pueden establecer para una instancia de la clase. La lista devuelta incluye todos los valores **mayContain** y **systemMayContain** de la clase y las clases de las que se deriva, incluidas las superclases y las clases auxiliares.   |
| [**IADsClass.PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | Recupera una matriz de los valores de **possibleSuperiors** para la clase, que indica las clases de objeto que pueden contener objetos de esta clase.                                                                                                                                        |



 

El esquema abstracto se almacena en el objeto de **subesquema** en el contenedor de esquemas. Para obtener el nombre distintivo del objeto de **subesquema** , enlace a RootDSE y lea el atributo **subSchemaSubEntry** , como se describe en [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md). Tenga en cuenta que es más eficaz leer el esquema abstracto enlazando a "LDAP://schema", que enlazando directamente al objeto de **subesquema** .

 

 