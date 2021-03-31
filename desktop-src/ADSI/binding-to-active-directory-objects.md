---
title: Enlazar a objetos de Active Directory
description: Antes de continuar con este escenario, debe comprender cómo se denominan los objetos ADSI en Active Directory y cómo enlazarlos. El enlace de un objeto ADSI conecta el objeto con el servicio de directorio y permite tener acceso a los métodos del objeto.
ms.assetid: 0d8d8f1c-786f-4d87-977c-91a167bcf118
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa54f2015e0d5663db2917eb27b250f39eb4c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075081"
---
# <a name="binding-to-active-directory-objects"></a><span data-ttu-id="7d70e-104">Enlazar a objetos de Active Directory</span><span class="sxs-lookup"><span data-stu-id="7d70e-104">Binding to Active Directory Objects</span></span>

<span data-ttu-id="7d70e-105">Antes de continuar con este escenario, debe comprender cómo se denominan los objetos ADSI en Active Directory y cómo enlazarlos.</span><span class="sxs-lookup"><span data-stu-id="7d70e-105">Before you continue with this scenario, you must understand how ADSI objects are named in Active Directory, and how to bind them.</span></span> <span data-ttu-id="7d70e-106">El enlace de un objeto ADSI conecta el objeto con el servicio de directorio y permite tener acceso a los métodos del objeto.</span><span class="sxs-lookup"><span data-stu-id="7d70e-106">Binding an ADSI object connects the object with the directory service, and allows you to access the methods of the object.</span></span>

## <a name="adspath"></a><span data-ttu-id="7d70e-107">ADsPath</span><span class="sxs-lookup"><span data-stu-id="7d70e-107">ADsPath</span></span>

<span data-ttu-id="7d70e-108">Un objeto ADSI se identifica de forma única mediante su cadena de enlace, que también se conoce como ADsPath.</span><span class="sxs-lookup"><span data-stu-id="7d70e-108">An ADSI object is uniquely identified by its binding string, which is also referred to as an ADsPath.</span></span> <span data-ttu-id="7d70e-109">ADsPath es una combinación de un identificador de programación (progID) del proveedor ADSI y el nombre distintivo (DN) del objeto.</span><span class="sxs-lookup"><span data-stu-id="7d70e-109">An ADsPath is a combination of a programmatic identifier (progID) of the ADSI provider, and the distinguished name (DN) of the object.</span></span>

<span data-ttu-id="7d70e-110">Este es el formato de ADsPath:</span><span class="sxs-lookup"><span data-stu-id="7d70e-110">Here's the format of an ADsPath:</span></span>

<span data-ttu-id="7d70e-111">"progID://DN"</span><span class="sxs-lookup"><span data-stu-id="7d70e-111">"progID://DN"</span></span>

-   <span data-ttu-id="7d70e-112">pogID: el identificador de programación del proveedor ADSI, como LDAP o Winnt.</span><span class="sxs-lookup"><span data-stu-id="7d70e-112">pogID — the programmatic identifier of the ADSI provider, such as LDAP or WinNT.</span></span>

-   <span data-ttu-id="7d70e-113">://: separa el progID del DN.</span><span class="sxs-lookup"><span data-stu-id="7d70e-113">:// — separates the progID from the DN.</span></span>

-   <span data-ttu-id="7d70e-114">DN: nombre distintivo del objeto ADSI, que es la ruta de acceso completa del objeto, donde la ruta de acceso consta de nombres distintivos relativos (RDN).</span><span class="sxs-lookup"><span data-stu-id="7d70e-114">DN — the distinguished name of the ADSI object, which is the full path of the object, where the path consists of relative distinguished names (RDNs).</span></span>

<span data-ttu-id="7d70e-115">Un RDN es el nombre del objeto sin la ruta de acceso y es único de sus objetos relacionados.</span><span class="sxs-lookup"><span data-stu-id="7d70e-115">An RDN is the name of the object without the path, and is unique from its sibling objects.</span></span> <span data-ttu-id="7d70e-116">Un RDN consta de un identificador de atributo y un valor, como "DC = Fabrikam", donde DC es el atributo y Fabrikam es el valor.</span><span class="sxs-lookup"><span data-stu-id="7d70e-116">An RDN consists of an attribute ID and value, such as "DC=Fabrikam", where DC is the attribute, and Fabrikam is the value.</span></span> <span data-ttu-id="7d70e-117">DC es un identificador de atributo RDN que representa el componente de dominio.</span><span class="sxs-lookup"><span data-stu-id="7d70e-117">DC is an RDN attribute ID that stands for domain component.</span></span>

<span data-ttu-id="7d70e-118">A continuación se muestra un ejemplo de una ADsPath:</span><span class="sxs-lookup"><span data-stu-id="7d70e-118">Here’s an example of an ADsPath:</span></span>

<span data-ttu-id="7d70e-119">"LDAP://DC = Fabrikam, DC = com"</span><span class="sxs-lookup"><span data-stu-id="7d70e-119">"LDAP://DC=Fabrikam,DC=Com"</span></span>

## <a name="binding-the-object"></a><span data-ttu-id="7d70e-120">Enlazar el objeto</span><span class="sxs-lookup"><span data-stu-id="7d70e-120">Binding the object</span></span>

<span data-ttu-id="7d70e-121">A continuación se muestra cómo puede enlazar el objeto de dominio en este escenario:</span><span class="sxs-lookup"><span data-stu-id="7d70e-121">Here's how you can bind the domain object in this scenario:</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=Com")
```



<span data-ttu-id="7d70e-122">Al ejecutar este ejemplo de código, ADSI utiliza el DN para determinar los objetos ADSI que se van a enlazar.</span><span class="sxs-lookup"><span data-stu-id="7d70e-122">When you run this code example, ADSI uses the DN to determine the ADSI objects to bind.</span></span> <span data-ttu-id="7d70e-123">Una vez que ADSI enlaza estos objetos, puede tener acceso a sus métodos.</span><span class="sxs-lookup"><span data-stu-id="7d70e-123">After ADSI binds these objects, you can access their methods.</span></span> <span data-ttu-id="7d70e-124">En el ejemplo de código anterior se enlaza un objeto de dominio a [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) e [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="7d70e-124">The previous code example binds a domain object to [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="7d70e-125">Ahora puede usar métodos en esas interfaces como [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete)y [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span><span class="sxs-lookup"><span data-stu-id="7d70e-125">You can now use methods on those interfaces such as [**Get**](/windows/desktop/api/Iads/nf-iads-iads-get), [**Put**](/windows/desktop/api/Iads/nf-iads-iads-put), [**Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create), [**Delete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete), and [**MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere).</span></span>

<span data-ttu-id="7d70e-126">Después de enlazar un objeto de dominio, puede imprimir algunos de sus atributos:</span><span class="sxs-lookup"><span data-stu-id="7d70e-126">After you bind a domain object, you can print some of its attributes:</span></span>


```VB
Debug.Print dom.Get("Name")
Debug.Print dom.Get("whenCreated")
```



<span data-ttu-id="7d70e-127">Para obtener más información sobre ADsPath, consulte [cadena de enlace](binding-string.md).</span><span class="sxs-lookup"><span data-stu-id="7d70e-127">For more information about ADsPath, see [Binding String](binding-string.md).</span></span> <span data-ttu-id="7d70e-128">Para obtener más información sobre el enlace, vea [enlazar a un objeto ADSI](binding-to-an-adsi-object.md).</span><span class="sxs-lookup"><span data-stu-id="7d70e-128">For more information about binding, see [Binding to an ADSI Object](binding-to-an-adsi-object.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d70e-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7d70e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d70e-130">Crear una unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="7d70e-130">Creating an Organizational Unit</span></span>](creating-an-organizational-unit.md)
</dt> </dl>

 

 




