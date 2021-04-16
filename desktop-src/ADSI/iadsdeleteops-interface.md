---
title: Interfaz IADsDeleteOps
description: La interfaz IADsDeleteOps se usa en las rutinas de supervisión y mantenimiento para el almacén de directorios subyacente. Puede eliminar objetos hoja y subárboles completos en una sola operación.
ms.assetid: 821b71c2-e9f5-4ca8-9366-e8a3f1907670
ms.tgt_platform: multiple
keywords:
- Interfaz IADsDeleteOps ADSI
- IADsDeleteOps ADSI, usar
- ADSI ADSI, código de ejemplo C/C++, uso de IADsDeleteOps para eliminar grupos completos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6332dd28e903996e8688d6c6fc672df080822595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656175"
---
# <a name="iadsdeleteops-interface"></a><span data-ttu-id="41afc-107">Interfaz IADsDeleteOps</span><span class="sxs-lookup"><span data-stu-id="41afc-107">IADsDeleteOps Interface</span></span>

<span data-ttu-id="41afc-108">La interfaz [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) se usa en las rutinas de supervisión y mantenimiento para el almacén de directorios subyacente.</span><span class="sxs-lookup"><span data-stu-id="41afc-108">The [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops) interface is used in supervisory and maintenance routines for the underlying directory store.</span></span> <span data-ttu-id="41afc-109">Puede eliminar objetos hoja y subárboles completos en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="41afc-109">It can delete leaf objects and entire subtrees in a single operation.</span></span>

<span data-ttu-id="41afc-110">Si no se admite esta interfaz, la eliminación de un objeto de Active Directory requeriría que cada objeto contenido se Enumere y se eliminara de forma recursiva.</span><span class="sxs-lookup"><span data-stu-id="41afc-110">If this interface were not supported, deleting an object from Active Directory would require that each contained object be recursively enumerated and deleted.</span></span> <span data-ttu-id="41afc-111">Con esta interfaz, cualquier objeto contenedor, con todos sus objetos y subobjetos contenidos, se puede eliminar con una sola operación.</span><span class="sxs-lookup"><span data-stu-id="41afc-111">With this interface, any container object, with all its contained objects and subobjects, can be deleted with a single operation.</span></span>

<span data-ttu-id="41afc-112">En el ejemplo de código siguiente se elimina el contenedor "ENG" y todos los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="41afc-112">The following code example deletes the "Eng" container and all child objects.</span></span>


```C++
HRESULT hr;
IADsDeleteOps *pDeleteOps;
LPWSTR pwszUsername = NULL;
LPWSTR pwszPassword = NULL;

// Insert code to securely retrieve the pwszUsername and pwszPassword
// or leave as NULL to use the default security context of the 
// calling application.
 
// Bind to the LDAP provider.
hr = ADsOpenObject(L"LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com", 
    pwszUsername,
    pwszPassword,
    0,
    ADS_SECURE_AUTHENTICATION,
    IID_IADsDeleteOps, 
    (void**)&pDeleteOps);
if(S_OK == hr)
{
    // Delete the container and all child objects.
    pDeleteOps->DeleteObject(0);

    // Release the interface.
    pDeleteOps->Release();
}

if(pwszUsername)
{
    SecureZeroMemory(pwszUsername, lstrlen(pwszUsername) * sizeof(TCHAR));
}
if(pwszPassword)
{
    SecureZeroMemory(pwszPassword, lstrlen(pwszPassword) * sizeof(TCHAR));
}
```



<span data-ttu-id="41afc-113">En el ejemplo de código siguiente se elimina el contenedor "ENG" y todos los objetos secundarios.</span><span class="sxs-lookup"><span data-stu-id="41afc-113">The following code example deletes the "Eng" container and all child objects.</span></span>


```VB
Dim DeleteOps As IADsDeleteOps

' Bind to the LDAP provider.
Set DeleteOps = GetObject("LDAP://CN=Eng,CN=Users,DC=Fabrikam,DC=Com")

' Delete the container and all child objects.
DeleteOps.DeleteObject (0)
```



 

 




