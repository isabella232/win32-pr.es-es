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
# <a name="how-to-trap-adsi-errors"></a><span data-ttu-id="d02c3-103">Cómo interceptar errores ADSI</span><span class="sxs-lookup"><span data-stu-id="d02c3-103">How to Trap ADSI Errors</span></span>

<span data-ttu-id="d02c3-104">VBScript solo ofrece una manera de interceptar errores: control de errores en línea.</span><span class="sxs-lookup"><span data-stu-id="d02c3-104">VBScript only offers one way to trap errors: inline error handling.</span></span> <span data-ttu-id="d02c3-105">Un controlador de errores en línea comienza con la instrucción **On Error Resume Next** .</span><span class="sxs-lookup"><span data-stu-id="d02c3-105">An inline error handler begins with the **On Error Resume Next** statement.</span></span> <span data-ttu-id="d02c3-106">Puesto que **al reanudar el error siguiente** impedirá que se detenga la ejecución del script hasta el final del ámbito desde el que se llama a la siguiente vez que se **reanuda el error** , debe comprobar el valor de **Err** en cada punto después de la instrucción **On Error Resume Next** en la que espera que se produzca un error.</span><span class="sxs-lookup"><span data-stu-id="d02c3-106">Since **On Error Resume Next** will prevent any errors from stopping execution of the script until the end of the scope from which **On Error Resume Next** is called, you must check the value of **Err** at every point after the **On Error Resume Next** statement where you expect an error might occur.</span></span> <span data-ttu-id="d02c3-107">En el ejemplo siguiente se muestra el control de errores en línea en un script ADSI:</span><span class="sxs-lookup"><span data-stu-id="d02c3-107">The following example demonstrates inline error handling in an ADSI script:</span></span>


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



<span data-ttu-id="d02c3-108">Después de cada ubicación en la que es probable que se produzca un error en el script, hay una instrucción **If Err** .</span><span class="sxs-lookup"><span data-stu-id="d02c3-108">After each location where the script is likely to encounter an error, there is an **If Err** statement.</span></span> <span data-ttu-id="d02c3-109">El objeto **Err** contiene el código de error del último error que se produjo durante la ejecución del script. Si no se ha producido ningún error, **Err** siempre será cero (0).</span><span class="sxs-lookup"><span data-stu-id="d02c3-109">The **Err** object contains the error code of the last error that occurred during execution of the script; if no error has occurred, **Err** will always be zero (0).</span></span> <span data-ttu-id="d02c3-110">En el ejemplo anterior, se producirá un error en la ejecución para saltar a la subrutina **AdsiErr** , que comprueba el valor de **Err. Number** en busca de errores esperados.</span><span class="sxs-lookup"><span data-stu-id="d02c3-110">In the previous example, an error will cause execution to jump to the **AdsiErr** subroutine, which checks the value of **Err.Number** for expected errors.</span></span> <span data-ttu-id="d02c3-111">En lugar de Dying con un mensaje de error críptico, el script proporcionará una explicación algo mejor sobre el motivo por el que dejó de ejecutarse.</span><span class="sxs-lookup"><span data-stu-id="d02c3-111">Instead of dying with a cryptic error message, the script will give a somewhat better explanation for why it stopped running.</span></span>

<span data-ttu-id="d02c3-112">Recuerde que, en el ámbito en el que se llama a la siguiente vez que se **reanuda el error** , se omitirá cualquier error que se produzca después de la siguiente llamada al **reanudar el error** .</span><span class="sxs-lookup"><span data-stu-id="d02c3-112">Remember that within the scope in which **On Error Resume Next** is called, any error that occurs after the **On Error Resume Next** call will be ignored.</span></span> <span data-ttu-id="d02c3-113">Esto puede hacer que un script sea más difícil de depurar si olvida comprobar el valor de **Err** en las ubicaciones adecuadas.</span><span class="sxs-lookup"><span data-stu-id="d02c3-113">This can actually make a script harder to debug if you forget to check the value of **Err** in appropriate locations.</span></span> <span data-ttu-id="d02c3-114">Siempre que espera que se produzca un error, asegúrese de comprobar el valor de **Err**.</span><span class="sxs-lookup"><span data-stu-id="d02c3-114">Wherever you expect an error to be likely, be sure to check the value of **Err**.</span></span>

<span data-ttu-id="d02c3-115">(Cuando esté depurando el script por primera vez, puede que desee dejar que el script detenga su ejecución y mostrar el número de línea infractor en un error y, a continuación, agregar los controladores de errores después de que el flujo de programa básico sea correcto).</span><span class="sxs-lookup"><span data-stu-id="d02c3-115">(When you are initially debugging the script you may want to simply let the script halt its execution and display the offending line number on an error, then add the error handlers after the basic program flow is correct.)</span></span>

 

 




