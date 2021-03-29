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
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="ac8f3-104">Leer el esquema abstracto</span><span class="sxs-lookup"><span data-stu-id="ac8f3-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="ac8f3-105">En este tema se proporcionan ejemplos de código y directrices para leer desde el esquema abstracto, que proporciona un subconjunto de los datos almacenados en los objetos **attributeSchema** y **ClassSchema** del contenedor de esquemas.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="ac8f3-106">Para recuperar datos que no están disponibles en el esquema abstracto, lea directamente los datos desde el contenedor de esquemas, tal y como se describe en [leer objetos attributeSchema y ClassSchema](reading-attributeschema-and-classschema-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ac8f3-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="ac8f3-107">Use la cadena de enlace "LDAP://schema" para enlazar con un puntero [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) en el esquema abstracto.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="ac8f3-108">Utilice este puntero para enumerar las entradas de la clase, el atributo y la sintaxis en el esquema abstracto.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="ac8f3-109">También puede utilizar el método [**IADsContainer. GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) para recuperar entradas individuales.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


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



<span data-ttu-id="ac8f3-110">Use una cadena de enlace similar, "LDAP://schema/ <object> ", para enlazar directamente a una entrada de clase o atributo en el esquema abstracto.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="ac8f3-111">En esta cadena, " &lt; Object &gt; " es el **lDAPDisplayName** de una clase o un atributo.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="ac8f3-112">Para las clases que se enlazan a la interfaz [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) ; en el caso de los atributos, enlace a la interfaz [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) .</span><span class="sxs-lookup"><span data-stu-id="ac8f3-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


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



<span data-ttu-id="ac8f3-113">Además, la interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) proporciona la propiedad [**IADs. Schema**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="ac8f3-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="ac8f3-114">Esta propiedad devuelve el ADsPath de la clase de objeto en el formato de cadena de enlace del esquema abstracto.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="ac8f3-115">Si tiene un puntero **IADs** a un objeto, puede enlazar a su clase en el esquema abstracto mediante el ADsPath devuelto desde **IADs. Schema**.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="ac8f3-116">En el caso de las clases, en la tabla siguiente se enumeran las propiedades clave proporcionadas por el esquema abstracto.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="ac8f3-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="ac8f3-117">Property</span></span>                                                             | <span data-ttu-id="ac8f3-118">Significado</span><span class="sxs-lookup"><span data-stu-id="ac8f3-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac8f3-119">**IADsClass. Abstract**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="ac8f3-120">Indica si se trata de una clase abstracta.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="ac8f3-121">**IADsClass. auxiliar**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="ac8f3-122">Indica si se trata de una clase auxiliar.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="ac8f3-123">**IADsClass.AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="ac8f3-124">Matriz de clases auxiliares de las que se deriva esta clase.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="ac8f3-125">**IADsClass. Container**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="ac8f3-126">Indica si los objetos de esta clase pueden contener otros objetos, que es true si alguna clase incluye esta clase en su lista de **possibleSuperiors**.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="ac8f3-127">**IADsClass.DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="ac8f3-128">Matriz de clases de las que se deriva esta clase.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="ac8f3-129">**IADsClass.MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="ac8f3-130">Recupera una matriz de las propiedades obligatorias que se deben establecer para una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="ac8f3-131">La lista devuelta incluye todos los valores **mustContain** y **systemMustContain** de la clase y las clases de las que se deriva, incluidas las superclases y las clases auxiliares.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="ac8f3-132">**IADsClass. OID**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="ac8f3-133">Recupera el governsID de la clase.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="ac8f3-134">**IADsClass. OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="ac8f3-135">Recupera una matriz de las propiedades opcionales que se pueden establecer para una instancia de la clase.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="ac8f3-136">La lista devuelta incluye todos los valores **mayContain** y **systemMayContain** de la clase y las clases de las que se deriva, incluidas las superclases y las clases auxiliares.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="ac8f3-137">**IADsClass.PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="ac8f3-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="ac8f3-138">Recupera una matriz de los valores de **possibleSuperiors** para la clase, que indica las clases de objeto que pueden contener objetos de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="ac8f3-139">El esquema abstracto se almacena en el objeto de **subesquema** en el contenedor de esquemas.</span><span class="sxs-lookup"><span data-stu-id="ac8f3-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="ac8f3-140">Para obtener el nombre distintivo del objeto de **subesquema** , enlace a RootDSE y lea el atributo **subSchemaSubEntry** , como se describe en [enlace sin servidor y RootDSE](serverless-binding-and-rootdse.md).</span><span class="sxs-lookup"><span data-stu-id="ac8f3-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="ac8f3-141">Tenga en cuenta que es más eficaz leer el esquema abstracto enlazando a "LDAP://schema", que enlazando directamente al objeto de **subesquema** .</span><span class="sxs-lookup"><span data-stu-id="ac8f3-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 