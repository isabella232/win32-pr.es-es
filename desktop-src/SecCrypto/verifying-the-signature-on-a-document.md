---
description: Cuando se recibe un documento firmado, se puede comprobar la validez de la firma o las firmas.
ms.assetid: 088915d8-768c-4378-a9dd-9347a428aff9
title: Comprobar la firma en un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f2886edcb9629011ddf1a0b5fb45a12a11f0556
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473447"
---
# <a name="verifying-the-signature-on-a-document"></a>Comprobar la firma en un documento

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Cuando se recibe un documento firmado, se puede comprobar la validez de la firma o las firmas. Se puede comprobar una firma para:

-   Validez del hash de firma
-   Validez del certificado del firmante

El [*hash de*](../secgloss/h-gly.md) firma se descifra mediante la clave [*pública*](../secgloss/p-gly.md) del firmante que se encuentra en el certificado del firmante, incluido como parte de la firma. [](../secgloss/c-gly.md) Si la firma descifrada coincide con un nuevo hash del documento original, la firma la creó el propietario de la clave privada asociada a la clave pública utilizada para descifrar el hash. Además, se garantiza que el documento en el que se basa la firma no se haya cambiado después de crear la firma.

También se puede comprobar la validez del certificado que proporcionó la clave pública y la identidad del firmante, incluidos problemas como si el certificado se ha revocado, si el certificado no está actualizado o si lo emitió un emisor de certificados de confianza.

En el ejemplo siguiente, el contenido firmado y el objeto **SignedData** se leen desde un archivo y se comprueban la firma y la validez del certificado usado para crear la firma.

> [!Note]  
> Si la firma no es criptográficamente válida o el certificado del firmante no es válido, se produce una excepción y el programa de comprobación debe controlar la excepción. En cualquier error CAPICOM, se devuelve un valor decimal negativo **de Err.Number.** Para obtener más información, vea [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obtener información sobre los valores decimales positivos **de Err.Number,** vea Winerror.h.

 


```VB
Sub VerifySig(ByVal FileToVerify As String, ByVal FileBase As String)
On Error GoTo ErrorHandler

Dim sdContent As String
Dim sdCheck As String
Dim mySD As SignedData
Set mySD = New SignedData

' Open a file and read the signature.
Open FileToVerify For Input As #1
Input #1, sdCheck
Close #1

' Open a file and input the plaintext content that was signed.
Open FileBase For Input As #2
Input #2, sdContent
Close #1

' Set the detached content upon which the signature is based.
mySD.Content = sdContent

' Verify the detached signature.
On Error Resume Next
    mySD.Verify sdCheck, True
If Err.Number <> 0 Then
    MsgBox "Signature verification failed. " & Err.Description
Else
    MsgBox "Verification complete."
End If

' Release the SignedData object.
Set mySD = Nothing

Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox "Visual Basic error found: " & Err.Description
    Else
        MsgBox "CAPICOM error found: " & Hex(Err.Number)
    End If
End Sub

```



 

 
