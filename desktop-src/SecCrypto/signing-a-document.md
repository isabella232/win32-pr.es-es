---
description: Un uso estándar de una firma es firmar un texto y guardarlo en un archivo. El texto firmado también se puede enviar a través de Internet. El mensaje firmado está en formato PKCS \# 7.
ms.assetid: 67a36123-4fce-4d40-83c3-b9668221276b
title: Firma de un documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 526bc4cd98d6cab40efc884a2377f3720c9849dbb7f6c1d4e8da5d49898bfa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898169"
---
# <a name="signing-a-document"></a>Firma de un documento

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

Un uso estándar de una firma es firmar un texto y guardarlo en un archivo. El texto firmado también se puede enviar a través de Internet. El mensaje firmado está en formato PKCS \# 7.

En este ejemplo, se crea la firma para el contenido desasociado (cuando el contenido no se incluye con la firma). Una firma desasociada se usaría con mayor frecuencia si el destinatario de la firma tiene una copia del texto firmado exacto. En el ejemplo siguiente, el mensaje original y la firma desasociada se escriben en archivos independientes.

En cualquier error CAPICOM, se devuelve un valor decimal negativo **de Err.Number.** Para obtener más información, vea [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obtener información sobre los valores decimales positivos **de Err.Number,** vea Winerror.h.

Al crear una firma se usa la clave privada [*del firmante.*](../secgloss/p-gly.md) Solo se puede crear una firma si el certificado del firmante con una clave privada asociada está disponible. Este ejemplo del **método Sign** no especifica un firmante. Si no se especifica un firmante y no hay ningún certificado en **CAPICOM \_ MY \_ STORE** tiene una clave privada asociada, se produce un error **en el método Sign.** Si uno y solo un certificado de **CAPICOM \_ MY \_ STORE** tiene una clave privada asociada, ese certificado y su clave privada se usan para crear la firma. Si más de un certificado del almacén **CAPICOM \_ MY \_ STORE** tiene una clave privada asociada, aparece un cuadro de diálogo y el usuario puede elegir el certificado que se usará para crear la firma.

Cuando una aplicación basada en web usa el método **Sign,** siempre se muestra un símbolo del sistema y se requiere el permiso del usuario antes de crear una firma que use esa clave privada del firmante.


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

[**Store.Open**](store-open.md)
</dt> <dt>

[**Signer.Certificate**](signer-certificate.md)
</dt> <dt>

[**Atributo**](attribute.md)
</dt> <dt>

[**SignedData**](signeddata.md)
</dt> </dl>

 

 
