---
title: Extender ADSI
description: Con el modelo de extensión ADSI, puede asociar una clase de directorio a su propio objeto COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e597d4b2dd2cf6a3b4a81f1fff3515289418b9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772961"
---
# <a name="extending-adsi"></a><span data-ttu-id="5a25a-103">Extender ADSI</span><span class="sxs-lookup"><span data-stu-id="5a25a-103">Extending ADSI</span></span>

<span data-ttu-id="5a25a-104">Con el modelo de extensión ADSI, puede asociar una clase de directorio a su propio objeto COM.</span><span class="sxs-lookup"><span data-stu-id="5a25a-104">With the ADSI extension model, you can associate a directory class with your own COM object.</span></span> <span data-ttu-id="5a25a-105">Desde el punto de vista del programador ADSI o del escritor de script, la extensión se convierte en una parte integral de ADSI.</span><span class="sxs-lookup"><span data-stu-id="5a25a-105">From an ADSI programmer or script writer's perspective, the extension becomes an integral part of ADSI.</span></span> <span data-ttu-id="5a25a-106">Por ejemplo, cuando un nuevo empleado se une a Fabrikam, el administrador de Windows NT creará un objeto de usuario en el directorio y el administrador de nóminas tendrá que configurar algunas entradas en los sistemas de recursos humanos para este usuario.</span><span class="sxs-lookup"><span data-stu-id="5a25a-106">For example, when a new employee joins Fabrikam, the Windows NT administrator will create a user object in the directory and the payroll administrator will need to set up some entries in the human resource systems for this user.</span></span> <span data-ttu-id="5a25a-107">Con una extensión ADSI, este proceso se puede simplificar en un solo script.</span><span class="sxs-lookup"><span data-stu-id="5a25a-107">With an ADSI extension, this process can be streamlined into one single script.</span></span>


```VB
Dim usr
Dim sUserName

On Error Resume Next

sUserName = InputBox ("Enter the name of the user to add:")

Set usr = ou.Create("user", "CN=" & sUserName)

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

// Insert code to set some attributes

usr.SetInfo

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

usr.AddToPayroll  'this is a custom method from an ADSI Extension

If Err.Number <> 0 Then
    WScript.Echo "An error has occurred. " & Err.Number
    Exit Sub 
End If

Debug.Print "User: " & usr.Name & "has been created"
```



<span data-ttu-id="5a25a-108">Para obtener más información, consulte [ADSI Extensions](adsi-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="5a25a-108">For more information, see [ADSI Extensions](adsi-extensions.md).</span></span>

 

 




