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
# <a name="extending-adsi"></a>Extender ADSI

Con el modelo de extensión ADSI, puede asociar una clase de directorio a su propio objeto COM. Desde el punto de vista del programador ADSI o del escritor de script, la extensión se convierte en una parte integral de ADSI. Por ejemplo, cuando un nuevo empleado se une a Fabrikam, el administrador de Windows NT creará un objeto de usuario en el directorio y el administrador de nóminas tendrá que configurar algunas entradas en los sistemas de recursos humanos para este usuario. Con una extensión ADSI, este proceso se puede simplificar en un solo script.


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



Para obtener más información, consulte [ADSI Extensions](adsi-extensions.md).

 

 




