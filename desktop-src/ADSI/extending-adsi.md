---
title: Extensión de ADSI
description: Con el modelo de extensión ADSI, puede asociar una clase de directorio a su propio objeto COM.
ms.assetid: bf9a324d-14eb-4eb9-a80d-b0431db3af26
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e9f5bd316fc4703cf522e2c5facfd6c32c5236da191668f6ba38ae6a904f00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428458"
---
# <a name="extending-adsi"></a>Extensión de ADSI

Con el modelo de extensión ADSI, puede asociar una clase de directorio a su propio objeto COM. Desde la perspectiva de un programador adsi o un escritor de scripts, la extensión se convierte en una parte integral de ADSI. Por ejemplo, cuando un nuevo empleado se une a Fabrikam, el administrador de Windows NT creará un objeto de usuario en el directorio y el administrador de nóminas deberá configurar algunas entradas en los sistemas de recursos humanos para este usuario. Con una extensión ADSI, este proceso se puede simplificar en un solo script.


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



Para obtener más información, vea [ADSI Extensions](adsi-extensions.md).

 

 




