---
title: Cómo capturar errores adsi
description: VBScript solo ofrece una manera de capturar errores en el control de errores en línea.
ms.assetid: 65379edf-54b0-475b-89ee-97d544d0d809
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd66283d2427c2c42162ce46a0a66ecbda87737cf2572d183ebdb0017232e8de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082539"
---
# <a name="how-to-trap-adsi-errors"></a>Cómo capturar errores adsi

VBScript solo ofrece una manera de capturar errores: control de errores en línea. Un controlador de errores en línea comienza con la **instrucción On Error Resume Next.** Puesto  que Al reanudar siguiente error impedirá que los errores detengan  la ejecución del script hasta el final del ámbito desde el que se llama a Al reanudar siguiente error, debe comprobar el valor de **Err** en cada punto después de la instrucción On **Error Resume Next** donde se espera que se produzca un error. En el ejemplo siguiente se muestra el control de errores en línea en un script ADSI:


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



Después de cada ubicación en la que es probable que el script encuentre un error, hay una **instrucción If Err.** El **objeto Err** contiene el código de error del último error que se produjo durante la ejecución del script; Si no se ha producido ningún error, **Err** siempre será cero (0). En el ejemplo anterior, un error hará que la ejecución salte a la subrutina **AdsiErr,** que comprueba el valor **de Err.Number** en busca de errores esperados. En lugar de tenerse con un mensaje de error críptico, el script dará una explicación un poco mejor de por qué dejó de ejecutarse.

Recuerde que, dentro del ámbito en el que se llama a **On Error Resume Next** ,se omitirá cualquier error que se produzca después de la llamada Al **reanudar** siguiente error. Esto puede dificultar la depuración de un script si olvida comprobar el valor **de Err** en las ubicaciones adecuadas. Siempre que se espere que sea probable un error, asegúrese de comprobar el valor de **Err**.

(Al depurar inicialmente el script, es posible que quiera dejar que el script detenga su ejecución y muestre el número de línea de error en caso de error y, a continuación, agregue los controladores de errores después de que el flujo de programa básico sea correcto).

 

 




