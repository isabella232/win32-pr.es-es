---
title: Traslado de usuarios existentes a la unidad organizativa
description: Cuando el administrador de la empresa, Joe Worden, actualiza el dominio de Windows NT 4,0 a Active Directory, se migran todos los usuarios y grupos a los contenedores de usuarios del dominio fabrikam.
ms.assetid: 230a594f-70c2-4ab6-a7e8-d5a77f2d6dd1
ms.tgt_platform: multiple
keywords:
- Traslado de usuarios existentes a la unidad organizativa AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 535ff7110eaf956f108854e8442faa7386667346
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104268256"
---
# <a name="moving-existing-users-to-the-organizational-unit"></a><span data-ttu-id="50b32-104">Traslado de usuarios existentes a la unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="50b32-104">Moving Existing Users to the Organizational Unit</span></span>

<span data-ttu-id="50b32-105">Cuando el administrador de la empresa, Joe Worden, actualiza el dominio de Windows NT 4,0 a Active Directory, se migran todos los usuarios y grupos a los contenedores de usuarios del dominio fabrikam.</span><span class="sxs-lookup"><span data-stu-id="50b32-105">When the enterprise administrator, Joe Worden, upgrades the Windows NT 4.0 domain to Active Directory, all users and groups are migrated to the Users containers in the Fabrikam domain.</span></span> <span data-ttu-id="50b32-106">Joe ahora puede trasladar esos usuarios y grupos a las unidades organizativas adecuadas.</span><span class="sxs-lookup"><span data-stu-id="50b32-106">Joe can now move those users and groups to the appropriate organizational units.</span></span> <span data-ttu-id="50b32-107">También se puede desplazar un objeto entre dominios de Windows 2000 relacionados mediante ADSI.</span><span class="sxs-lookup"><span data-stu-id="50b32-107">An object can also be moved between related Windows 2000 domains using ADSI.</span></span>

<span data-ttu-id="50b32-108">En el ejemplo de código siguiente, Joe mueve "juanpérez" a la organización de ventas.</span><span class="sxs-lookup"><span data-stu-id="50b32-108">In the following code example, Joe moves "jeffsmith" to the Sales organization.</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=fabrikam,DC=com", vbNullString)
```



<span data-ttu-id="50b32-109">El método [**IADsContainer. MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) toma el ADsPath del objeto que se va a desplace y el nuevo nombre de objeto (RDN).</span><span class="sxs-lookup"><span data-stu-id="50b32-109">The [**IADsContainer.MoveHere**](/windows/desktop/api/Iads/nf-iads-iadscontainer-movehere) method takes the ADsPath of the object to be moved and the new object name (RDN).</span></span> <span data-ttu-id="50b32-110">Para mantener el mismo nombre, puede especificar **null** (**vbNullString**) para el parámetro *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="50b32-110">To keep the same name, you can specify **NULL** (**vbNullString**) for the *bstrNewName* parameter.</span></span> <span data-ttu-id="50b32-111">Para cambiar el nombre del objeto cuando se mueve, especifique el nuevo nombre distintivo relativo para el parámetro *bstrNewName* .</span><span class="sxs-lookup"><span data-stu-id="50b32-111">To rename the object when it is moved, specify the new relative distinguished name for the *bstrNewName* parameter.</span></span> <span data-ttu-id="50b32-112">Por ejemplo, para migrar juanpérez a la organización sales y cambiar el nombre del objeto "juanpérez" a "Jeff \_ Smith" en la misma operación, Joe ejecutaría el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="50b32-112">For example, to move jeffsmith to the sales organization and rename the "jeffsmith" object to "jeff\_smith" in the same operation, Joe would execute the following code:</span></span>


```VB
Set usr = salesOU.MoveHere("LDAP://CN=jeffsmith,CN=Users,DC=Fabrikam,DC=com", "CN=jeff_smith")
```



## <a name="related-topics"></a><span data-ttu-id="50b32-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="50b32-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50b32-114">Creación de nuevos usuarios en la unidad organizativa</span><span class="sxs-lookup"><span data-stu-id="50b32-114">Creating New Users in the Organizational Unit</span></span>](creating-new-users-in-the-organizational-unit.md)
</dt> </dl>

 

 




