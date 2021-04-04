---
title: Usar objectGUID para enlazar a un objeto
description: Un nombre distintivo de objeto cambia si se cambia el nombre o se mueve el objeto, por lo que el nombre distintivo no es un identificador de objeto confiable.
ms.assetid: 6c038005-3ecb-4c00-b1a3-a231d3aea64e
ms.tgt_platform: multiple
keywords:
- Usar objectGUID para enlazar a un objeto AD
- TITULAR de objectGUID
- objectGUID AD, usar para enlazar a un objeto
- Active Directory, usar, enlazar, usar objectGUID para enlazar a un objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045c6194cf27b1697cc478b547105fb10335c219
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077485"
---
# <a name="using-objectguid-to-bind-to-an-object"></a><span data-ttu-id="3107d-107">Usar objectGUID para enlazar a un objeto</span><span class="sxs-lookup"><span data-stu-id="3107d-107">Using objectGUID to Bind to an Object</span></span>

<span data-ttu-id="3107d-108">Un nombre distintivo de objeto cambia si se cambia el nombre o se mueve el objeto, por lo que el nombre distintivo no es un identificador de objeto confiable.</span><span class="sxs-lookup"><span data-stu-id="3107d-108">An object distinguished name changes if the object is renamed or moved, therefore the distinguished name is not a reliable object identifier.</span></span> <span data-ttu-id="3107d-109">En Active Directory Domain Services, la propiedad **objectGUID** de un objeto nunca cambia, aunque se cambie el nombre del objeto o se mueva.</span><span class="sxs-lookup"><span data-stu-id="3107d-109">In Active Directory Domain Services, an object's **objectGUID** property never changes, even if the object is renamed or moved.</span></span> <span data-ttu-id="3107d-110">Para obtener más información sobre **objectGUID** e identificadores, vea [nombres de objeto e identidades](object-names-and-identities.md).</span><span class="sxs-lookup"><span data-stu-id="3107d-110">For more information about **objectGUID** and identifiers, see [Object Names and Identities](object-names-and-identities.md).</span></span>

<span data-ttu-id="3107d-111">El proveedor LDAP Active Directory proporciona un método para enlazar a un objeto utilizando el GUID del objeto.</span><span class="sxs-lookup"><span data-stu-id="3107d-111">The Active Directory LDAP provider provides a method to bind to an object using the object GUID.</span></span> <span data-ttu-id="3107d-112">El formato de la cadena de enlace es el siguiente:</span><span class="sxs-lookup"><span data-stu-id="3107d-112">The binding string format is as follows:</span></span>


```C++
LDAP://servername/<GUID=XXXXX>
```



<span data-ttu-id="3107d-113">En este ejemplo, "ServerName" es el nombre del servidor de directorio y "XXXXX" es la representación de cadena del valor hexadecimal del GUID.</span><span class="sxs-lookup"><span data-stu-id="3107d-113">In this example, "servername" is the name of the directory server and "XXXXX" is the string representation of the hexadecimal value of the GUID.</span></span> <span data-ttu-id="3107d-114">"ServerName" es opcional.</span><span class="sxs-lookup"><span data-stu-id="3107d-114">The "servername" is optional.</span></span> <span data-ttu-id="3107d-115">La cadena GUID se especifica en el formulario "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX".</span><span class="sxs-lookup"><span data-stu-id="3107d-115">The GUID string is specified in the "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX" form.</span></span> <span data-ttu-id="3107d-116">La cadena GUID también puede tener la forma "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", que es la misma forma que la cadena generada por la función [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) , sin las llaves circundantes " {} ".</span><span class="sxs-lookup"><span data-stu-id="3107d-116">The GUID string can also take the form "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX", which is the same form as the string produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function, without the surrounding braces "{}".</span></span> <span data-ttu-id="3107d-117">Para obtener más información y un ejemplo de código que muestra cómo crear una cadena enlazable desde un GUID, vea el [código de ejemplo para crear una representación de cadena enlazable de un GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span><span class="sxs-lookup"><span data-stu-id="3107d-117">For more information and a code example that shows how to create a bindable string from a GUID, see [Example Code for Creating a Bindable String Representation of a GUID](example-code-for-creating-a-bindable-string-representation-of-a-guid.md).</span></span> <span data-ttu-id="3107d-118">La propiedad [**IADs. GUID**](/windows/desktop/ADSI/iads-property-methods) se puede usar para recuperar el formato de cadena correcto del GUID.</span><span class="sxs-lookup"><span data-stu-id="3107d-118">The [**IADs.GUID**](/windows/desktop/ADSI/iads-property-methods) property can be used to retrieve the proper string form of the GUID.</span></span>

<span data-ttu-id="3107d-119">Al enlazar con el GUID del objeto, no se admiten algunos métodos y propiedades de [**IADs**](/windows/desktop/api/iads/nn-iads-iads) y [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) .</span><span class="sxs-lookup"><span data-stu-id="3107d-119">When binding using the object GUID, some [**IADs**](/windows/desktop/api/iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) methods and properties are not supported.</span></span> <span data-ttu-id="3107d-120">Las siguientes propiedades de **IADs** no son compatibles con los objetos obtenidos mediante el enlace con el GUID del objeto:</span><span class="sxs-lookup"><span data-stu-id="3107d-120">The following **IADs** properties are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="3107d-121">**ADsPath**</span><span class="sxs-lookup"><span data-stu-id="3107d-121">**ADsPath**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="3107d-122">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3107d-122">**Name**</span></span>](/windows/desktop/ADSI/iads-property-methods)
-   [<span data-ttu-id="3107d-123">**Parent**</span><span class="sxs-lookup"><span data-stu-id="3107d-123">**Parent**</span></span>](/windows/desktop/ADSI/iads-property-methods)

<span data-ttu-id="3107d-124">Los métodos **IADsContainer** siguientes no son compatibles con los objetos obtenidos mediante el enlace con el GUID del objeto:</span><span class="sxs-lookup"><span data-stu-id="3107d-124">The following **IADsContainer** methods are not supported by objects obtained by binding using the object GUID:</span></span>

-   [<span data-ttu-id="3107d-125">**GetObject**</span><span class="sxs-lookup"><span data-stu-id="3107d-125">**GetObject**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject)
-   [<span data-ttu-id="3107d-126">**A**</span><span class="sxs-lookup"><span data-stu-id="3107d-126">**Create**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-create)
-   [<span data-ttu-id="3107d-127">**Elimínelos**</span><span class="sxs-lookup"><span data-stu-id="3107d-127">**Delete**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)
-   [<span data-ttu-id="3107d-128">**CopyHere**</span><span class="sxs-lookup"><span data-stu-id="3107d-128">**CopyHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-copyhere)
-   [<span data-ttu-id="3107d-129">**MoveHere**</span><span class="sxs-lookup"><span data-stu-id="3107d-129">**MoveHere**</span></span>](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere)

<span data-ttu-id="3107d-130">Para usar estos métodos y propiedades después de enlazar a un objeto mediante el GUID del objeto, use el método [**IADs. Get**](/windows/desktop/api/iads/nf-iads-iads-get) para recuperar el nombre distintivo del objeto y, a continuación, use el nombre distintivo para enlazarlo de nuevo al objeto.</span><span class="sxs-lookup"><span data-stu-id="3107d-130">To use these methods and properties after binding to an object using the object GUID, use the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve the object distinguished name and then use the distinguished name to bind to the object again.</span></span>

<span data-ttu-id="3107d-131">Si una aplicación almacena o almacena en caché identificadores o referencias a objetos almacenados en Active Directory Domain Services, el GUID del objeto es el mejor identificador que se debe usar por varias razones:</span><span class="sxs-lookup"><span data-stu-id="3107d-131">If an application stores or caches identifiers or references to objects stored in Active Directory Domain Services, the object GUID is the best identifier to use for several reasons:</span></span>

-   <span data-ttu-id="3107d-132">La propiedad **objectGUID** de en el objeto nunca cambia aunque se cambie el nombre del objeto o se mueva.</span><span class="sxs-lookup"><span data-stu-id="3107d-132">The **objectGUID** property of on object never changes even if the object is renamed or moved.</span></span>
-   <span data-ttu-id="3107d-133">Es fácil enlazar con el objeto mediante el GUID del objeto.</span><span class="sxs-lookup"><span data-stu-id="3107d-133">It is easy to bind to the object using the object GUID.</span></span>
-   <span data-ttu-id="3107d-134">Si se cambia el nombre del objeto o se mueve, la propiedad **objectGUID** proporciona un identificador único que se puede usar para buscar e identificar rápidamente el objeto en lugar de tener que crear una consulta que tenga condiciones para todas las propiedades que identifiquen ese objeto.</span><span class="sxs-lookup"><span data-stu-id="3107d-134">If the object is renamed or moved, the **objectGUID** property provides a single identifier that can be used to quickly find and identify the object rather than having to compose a query that has conditions for all properties that would identify that object.</span></span>

 

 