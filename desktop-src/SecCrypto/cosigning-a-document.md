---
description: Más de un firmante puede firmar un documento.
ms.assetid: f81cbf7b-317d-4fab-9b30-88b6c6576db8
title: Cosignación de un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb384ef47001f1df85810ac37595988da96a356ff3b36b1b140d1a6f54d0d698
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769390"
---
# <a name="cosigning-a-document"></a>Cosignación de un documento

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Más de un firmante puede firmar un documento. Esto sucede cuando, por ejemplo, dos o más partes firman un contrato o un informe de gastos. En el ejemplo siguiente, un segundo firmante recibe un documento ya firmado. Este firmante usa el [**método CoSign**](signeddata-cosign.md) para adjuntar una firma adicional al documento.

Si se produce un error CAPICOM, se devuelve un valor negativo en la **propiedad Err.Number.** Para obtener más información sobre los códigos de error de CAPICOM, vea [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Si el código de error de **la propiedad Err.Number** es un valor positivo, el error es Windows error. Para obtener información sobre Windows de error, consulte Winerror.h.

> [!Note]
> La cofirmación de un documento también requiere que el cofirmador tenga un certificado [*disponible*](../secgloss/c-gly.md) con [*una clave privada*](../secgloss/p-gly.md) para crear la firma. Si no se especifica un firmante en la llamada del método [**Sign**](signeddata-sign.md) y no hay ningún certificado en CAPICOM MY STORE con una clave privada asociada, se produce un error en \_ el \_ método. Si hay uno y solo un certificado en CAPICOM MY STORE con una clave privada asociada, se usan esa clave \_ \_ y el certificado. Si hay más de un certificado utilizable, se muestra un mensaje para permitir que el usuario elija el certificado deseado.
> 
> Si el [**método CoSign**](signeddata-cosign.md) se usa en una aplicación basada en web, siempre se muestra un mensaje para obtener el permiso del usuario antes de crear una firma mediante la clave privada de ese firmante.

 

En el ejemplo siguiente, se leen los archivos que contienen el documento que se va a firmar y las firmas actuales en ese documento, la firma se firma y la nueva firma se escribe en un archivo. En el ejemplo se usa una firma desasociada con los datos firmados y la firma en archivos independientes.


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



 

 
