---
title: Crear una unidad organizativa
description: Ahora que tiene el objeto de dominio, puede empezar a crear unidades organizativas.
ms.assetid: c9955b44-5ca1-4b4b-85c8-e0d55a4304ca
ms.tgt_platform: multiple
keywords:
- Creación de una unidad organizativa ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78ec0da1efe78d54eba8bc0dc05a998717aaf91f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103993863"
---
# <a name="creating-an-organizational-unit"></a><span data-ttu-id="fd0ba-104">Crear una unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="fd0ba-104">Creating an Organizational Unit</span></span>

<span data-ttu-id="fd0ba-105">Ahora que tiene el objeto de dominio, puede empezar a crear unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-105">Now that you have the domain object, you can start creating organizational units.</span></span> <span data-ttu-id="fd0ba-106">Fabrikam tiene dos divisiones: sales y Production.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-106">Fabrikam has two divisions: Sales and Production.</span></span> <span data-ttu-id="fd0ba-107">La compañía planea contratar dos administradores de Windows 2000 para administrar cada división.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-107">The company is planning to hire two Windows 2000 administrators to manage each division.</span></span> <span data-ttu-id="fd0ba-108">Joe Worden, como administrador de la empresa, creará dos nuevas unidades organizativas en el dominio de fabrikam.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-108">Joe Worden, as the enterprise administrator, will create two new organizational units under the Fabrikam domain.</span></span> <span data-ttu-id="fd0ba-109">Al crear una unidad organizativa, Joe puede agrupar varios objetos y permitir que otra persona administre estos objetos.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-109">By creating an organizational unit, Joe can group multiple objects together and let someone else manage these objects.</span></span> <span data-ttu-id="fd0ba-110">En el ejemplo de código siguiente se crea la unidad organizativa (OU) de ventas.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-110">The following code example creates the Sales Organizational Unit (OU).</span></span>


```VB
Dim dom as IADsContainer
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
Set salesOrg = dom.Create("organizationalUnit", "OU=Sales")
salesOrg.Put "description", "Sales Headquarter,SF"
salesOrg.Put "wwwHomePage", "https://fabrikam.com/sales"
salesOrg.SetInfo
```



<span data-ttu-id="fd0ba-111">El método [**IADsContainer. Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) acepta el nombre de clase y el nombre del nuevo objeto.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-111">The [**IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) method accepts the class name and the name of the new object.</span></span> <span data-ttu-id="fd0ba-112">En este momento, el objeto no se confirma en Active Directory.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-112">At this point the object is not committed to Active Directory.</span></span> <span data-ttu-id="fd0ba-113">Sin embargo, tendrá una referencia de objeto ADSI/COM en el cliente.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-113">You, however, will have an ADSI/COM object reference on the client.</span></span> <span data-ttu-id="fd0ba-114">Con este objeto ADSI, puede establecer o modificar atributos mediante el método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) .</span><span class="sxs-lookup"><span data-stu-id="fd0ba-114">With this ADSI object, you can set or modify attributes using the [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) method.</span></span> <span data-ttu-id="fd0ba-115">El método **IADs. put** acepta el nombre del atributo y el valor del atributo.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-115">The **IADs.Put** method accepts the attribute name and the value of the attribute.</span></span> <span data-ttu-id="fd0ba-116">Sin embargo, no se confirma nada en el directorio. todo está almacenado en la memoria caché del cliente.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-116">Still, nothing is committed to the directory; everything is cached at the client.</span></span> <span data-ttu-id="fd0ba-117">Cuando se llama al método [**IADs. SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) , los cambios, en este caso, la creación de objetos y la modificación de atributos, se confirman en el directorio.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-117">When you call the [**IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) method, the changes, in this case, object creation and attribute modification, are committed to the directory.</span></span> <span data-ttu-id="fd0ba-118">Estos cambios se transfieren, lo que significa que verá el nuevo objeto con todos los atributos que establezca, o bien ningún objeto.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-118">These changes are transacted, meaning that you will see either the new object with all attributes you set, or no object at all.</span></span>

<span data-ttu-id="fd0ba-119">También puede anidar unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-119">You can also nest organizational units.</span></span> <span data-ttu-id="fd0ba-120">En el ejemplo de código siguiente se da por supuesto que la división sales está dividida en las regiones este y oeste.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-120">The following code example assumes that the Sales division is divided further into the East and West regions.</span></span>


```VB
Set east = salesOrg.Create("organizationalUnit", "OU=East")
east.SetInfo
```



<span data-ttu-id="fd0ba-121">Esto también se aplica a la región oeste.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-121">This also applies for the West region.</span></span>

<span data-ttu-id="fd0ba-122">Para enlazar directamente con la región East de la organización sales, especifique el nombre distintivo.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-122">To bind directly to the East region in the Sales organization, specify the distinguished name.</span></span>


```VB
Set east = GetObject("LDAP://OU=East,OU=Sales,DC=Fabrikam,DC=COM")
Debug.Print east.Get "description"
east.Put "wwwHomePage", "https://fabrikam.com/sales/east"
```



<span data-ttu-id="fd0ba-123">Si ya ha enlazado al objeto primario (sales), puede enlazar con el objeto secundario (East) del objeto primario mediante el nombre relativo del objeto secundario.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-123">If you have already bound to the parent object (Sales), you can bind to the child object (East) from the parent object using the relative name of the child object.</span></span>


```VB
Set east = salesOU.GetObject("organizationalUnit", "OU=East")
```



<span data-ttu-id="fd0ba-124">Para asegurarse de que los objetos se han creado, use el complemento de MMC Active Directory usuarios y equipos para ver las nuevas unidades organizativas.</span><span class="sxs-lookup"><span data-stu-id="fd0ba-124">To ensure that the objects have been created, use the Active Directory Users and Computers MMC snap-in to view the new organizational units.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd0ba-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd0ba-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd0ba-126">Traslado de usuarios existentes a la unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="fd0ba-126">Moving Existing Users to the Organizational Unit</span></span>](moving-existing-users-to-the-organizational-unit.md)
</dt> </dl>

 

 




