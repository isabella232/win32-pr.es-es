---
description: Un documento puede estar firmado por más de un firmante.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Firmar un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa06cbbc95dc0fe558c6e704bd18102e80221dbc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105689698"
---
# <a name="cosigning-a-document"></a>Firmar un documento

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

Un documento puede estar firmado por más de un firmante. Esto sucede cuando, por ejemplo, dos o más entidades firman un contrato o un informe de gastos. En el siguiente ejemplo, un documento ya firmado lo recibe un segundo firmante. Este firmante usa el método de [**cofirma**](signeddata-cosign.md) para adjuntar una firma adicional al documento.

Si se produce algún error de CAPICOM, se devuelve un valor negativo en la propiedad **Err. Number** . Para obtener más información sobre los códigos de error de CAPICOM, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md). Si el código de error de la propiedad **Err. Number** es un valor positivo, el error es un error de Windows. Para obtener información acerca de los códigos de error de Windows, consulte Winerror. h.

> [!Note]
> Para firmar un documento también es necesario que el cofirmador tenga un [*certificado*](../secgloss/c-gly.md) disponible con una [*clave privada*](../secgloss/p-gly.md) para crear la firma. Si no se especifica un firmante en la llamada del método [**Sign**](signeddata-sign.md) y no hay ningún certificado en CAPICOM \_ My \_ Store con una clave privada asociada, se produce un error en el método. Si solo hay un certificado en CAPICOM \_ My \_ Store con una clave privada asociada, se usan esa clave y el certificado. Si hay más de un certificado que se puede usar, se muestra un mensaje para permitir que el usuario elija el certificado deseado.
> 
> Si se usa el método de [**cofirmación**](signeddata-cosign.md) en una aplicación basada en Web, siempre se muestra un símbolo del sistema para obtener el permiso del usuario antes de crear una firma mediante la clave privada de dicho firmante.

 

En el ejemplo siguiente, se leen los archivos que contienen el documento que se va a firmar y las firmas actuales de dicho documento, la firma es cofirmada y la nueva firma se escribe en un archivo. En el ejemplo se utiliza una firma desasociada con los datos firmados y la firma en archivos independientes.


```VB
Sub CoSignContent(ByVal InputFile1Name As String, ByVal _
    InputFile2Name As String, ByVal OutputFileName As String)

    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim CS As String
    Dim Signobj As New SignedData
    Open InputFile1Name for Input as #1
    Input #1, s
    Close #1
    Open InputFileName2 for input as #2
    Input #2, c 
    Close #2

    Signobj.Content = c
    Signobj.Verify(s)
    CS = Signobj.CoSign
    Open OutputFileName for output as #3
    Write #3, CS
    Close # 3
    Signobj = Nothing
    MsgBox("Cosign finished. Cosignature saved to a file.")
    Exit Sub
ErrorHandler:
    If err.number > 0 Then
        MsgBox("Visual Basic error found:" & err.description)
    Else
        MsgBox("CAPICOM error found : " & err.number)
    End If
End Sub
```



 

 
