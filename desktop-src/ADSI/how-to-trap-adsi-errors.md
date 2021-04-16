---
title: Cómo interceptar errores ADSI
description: VBScript solo ofrece una manera de interceptar errores de control de errores en línea.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa36b3e9b1027e1733009d58a572a0b27c7ef0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656177"
---
# <a name="how-to-trap-adsi-errors"></a>Cómo interceptar errores ADSI

VBScript solo ofrece una manera de interceptar errores: control de errores en línea. Un controlador de errores en línea comienza con la instrucción **On Error Resume Next** . Puesto que **al reanudar el error siguiente** impedirá que se detenga la ejecución del script hasta el final del ámbito desde el que se llama a la siguiente vez que se **reanuda el error** , debe comprobar el valor de **Err** en cada punto después de la instrucción **On Error Resume Next** en la que espera que se produzca un error. En el ejemplo siguiente se muestra el control de errores en línea en un script ADSI:


```VB
On Error Resume Next

Set myComputer = GetObject(computerPath)
If Err Then AdsiErr()

' Create the new user account
Set newUser = myComputer.Create("user", username)
newUser.SetInfo
If Err Then AdsiErr()

Sub AdsiErr()
    Dim s
    Dim e
    
    If Err.Number = &H8000500E Then
        WScript.Echo "The user " & username & " already exists."
    Elseif Err.Number = &H80005000 Then
        WScript.Echo "Computer " & computerPath & " not found.  Check the ADsPath and try again."
    Else
        e = Hex(Err.Number)
        WScript.Echo "Unexpected Error " & e & "(" & Err.Number & ")"
    End If
    WScript.Quit(1)

End Sub
```



Después de cada ubicación en la que es probable que se produzca un error en el script, hay una instrucción **If Err** . El objeto **Err** contiene el código de error del último error que se produjo durante la ejecución del script. Si no se ha producido ningún error, **Err** siempre será cero (0). En el ejemplo anterior, se producirá un error en la ejecución para saltar a la subrutina **AdsiErr** , que comprueba el valor de **Err. Number** en busca de errores esperados. En lugar de Dying con un mensaje de error críptico, el script proporcionará una explicación algo mejor sobre el motivo por el que dejó de ejecutarse.

Recuerde que, en el ámbito en el que se llama a la siguiente vez que se **reanuda el error** , se omitirá cualquier error que se produzca después de la siguiente llamada al **reanudar el error** . Esto puede hacer que un script sea más difícil de depurar si olvida comprobar el valor de **Err** en las ubicaciones adecuadas. Siempre que espera que se produzca un error, asegúrese de comprobar el valor de **Err**.

(Cuando esté depurando el script por primera vez, puede que desee dejar que el script detenga su ejecución y mostrar el número de línea infractor en un error y, a continuación, agregar los controladores de errores después de que el flujo de programa básico sea correcto).

 

 




