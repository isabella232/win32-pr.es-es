---
description: Un uso estándar de una firma es firmar un texto y guardar ese texto firmado en un archivo. También se puede enviar el texto firmado a través de Internet. El mensaje firmado está en \# formato PKCS 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Firmar un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ce1754cdfa1e89c23525474bae880dc2809c242
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666210"
---
# <a name="signing-a-document"></a>Firmar un documento

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

Un uso estándar de una firma es firmar un texto y guardar ese texto firmado en un archivo. También se puede enviar el texto firmado a través de Internet. El mensaje firmado está en \# formato PKCS 7.

En este ejemplo, la firma se crea para el contenido separado (cuando el contenido no se incluye con la firma). Una firma desasociada se utilizaría normalmente si el destinatario de la firma tiene una copia del texto con firma exacto. En el ejemplo siguiente, el mensaje original y la firma desasociada se escriben en archivos independientes.

En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** . Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md). Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.

Al crear una firma se usa la [*clave privada*](../secgloss/p-gly.md)del firmante. Solo se puede crear una firma si está disponible el certificado del firmante con una clave privada asociada. Este ejemplo del método **Sign** no especifica un firmante. Si no se especifica un firmante y ningún certificado de **CAPICOM \_ My \_ Store** tiene una clave privada asociada, se produce un error en el método **Sign** . Si un solo certificado de **CAPICOM \_ My \_ Store** tiene una clave privada asociada, el certificado y su clave privada se usan para crear la firma. Si hay más de un certificado en la tienda **CAPICOM \_ My \_ Store** que tiene una clave privada asociada, aparece un cuadro de diálogo y el usuario puede elegir el certificado que se usará para crear la firma.

Cuando una aplicación basada en Web usa el método **Sign** , siempre se muestra un mensaje y se requiere el permiso del usuario antes de crear una firma que use la clave privada de dicho firmante.


```VB
Sub Signfile(ByVal InputFileName As String, _
    ByVal OutputFileName As String)
    
    On Error GoTo ErrorHandler
    Dim c As String
    Dim s As String
    Dim MyStore As New Store
    Dim Signobj As New SignedData
    Dim Signer As New Signer

    ' NOTE: the name 'Attribute' is not a unique name
    ' and must be preceded by 'CAPICOM.'
    Dim SigningTime As New CAPICOM.Attribute

    ' Open the MY store and retrieve the first certificate from the
    ' Store. The signing operation will only work if this
    ' certificate is valid and has access to the signer's private key.
    MyStore.Open CAPICOM_CURRENT_USER_STORE, "MY", _
        CAPICOM_STORE_OPEN_READ_ONLY
    Signer.Certificate = MyStore.Certificates.Item(1)

    ' Open the input file and read the content to be signed from
    ' the file.
    Open App.Path & "\" & InputFileName For Input As #1
    Input #1, c
    Close #1
    
    ' Set the content to be signed.
    Signobj.Content = c

    ' Save the time the data was signed as a signer attribute.
    SigningTime.Name = CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME
    SigningTime.Value = Now
    Signer.AuthenticatedAttributes.Add SigningTime

    ' Sign the content using the signer's private key.
    ' The 'True' parameter indicates that the content signed is not
    ' included in the signature string.
    s = Signobj.Sign(Signer, True)

    Open App.Path & "\" & OutputFileName For Output As #2
    Write #2, s
    Close #2

    MsgBox ("Signature done - Saved to file" & OutputFileName)
    Set Signobj = Nothing
    Set MyStore = Nothing
    Set Signer = Nothing
    Set SigningTime = Nothing

    Exit Sub

ErrorHandler:
    If Err.Number > 0 Then
        MsgBox ("Visual Basic error found:" & Err.Description)
    Else
        MsgBox ("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Store. Open**](store-open.md)
</dt> <dt>

[**Certificado de firmante**](signer-certificate.md)
</dt> <dt>

[**Atributo**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
