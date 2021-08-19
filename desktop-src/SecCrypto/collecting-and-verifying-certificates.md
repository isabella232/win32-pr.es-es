---
description: En el ejemplo siguiente, los certificados de un almacén local se enumeran y comprueban su validez.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Recopilación y comprobación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60b793cf4aeca7d05d166a4b205b924db53faee09683cefcef7b0244a9eb0289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117769544"
---
# <a name="collecting-and-verifying-certificates"></a>Recopilación y comprobación de certificados

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

A menudo, es necesario [*recopilar y*](../secgloss/c-gly.md) comprobar un grupo de certificados. Esto suele hacerse para preparar un grupo de destinatarios para un mensaje envoltorio. En el ejemplo siguiente, los certificados de un almacén local se enumeran y comprueban su validez. A continuación, Active Directory se abre un almacén para recuperar y agregar nuevos certificados al almacén local. Los certificados recuperados del almacén de Active Directory se comprueban para comprobar su validez y, si son válidos, se agregan al almacén local. A continuación, ambos almacenes se cierran.

En cualquier error CAPICOM, se devuelve un valor decimal negativo **de Err.Number.** Para obtener más información, vea [**CAPICOM \_ ERROR \_ CODE**](capicom-error-code.md). Para obtener información sobre los valores decimales positivos **de Err.Number,** vea Winerror.h.

En este ejemplo, el nombre del almacén local se pasa como un parámetro de cadena. Una cadena que indica los criterios de búsqueda de los certificados en el almacén Active Directory también se pasa como parámetro.


```VB
Sub CollectValidCerts(ByVal storename As String, ByVal _
    certname As String)

    On Error GoTo errorhandler

    ' Prepare a local certificate store to contain valid
    ' certificates for the recipients of an enveloped
    ' message.

    ' Open the local store and go to the certificates in the store
    '   1. Display the certificate
    '   2. Check the validity of the certificate
    '   3. Remove certificates that are not valid from the store

    Dim LocalStore As New Store
    Dim ADStore As New Store
    Dim i As Long

    LocalStore.Open(CAPICOM_CURRENT_USER_STORE, storename, _
        CAPICOM_STORE_OPEN_READ_WRITE)

    MsgBox("There are " & LocalStore.Certificates.Count & _
        " certificates in this store ")
    For i = 1 To LocalStore.Certificates.Count
        If LocalStore.Certificates.Item(i).IsValid Then
            LocalStore.Certificates.Item(i).Display()
        Else
            MsgBox("A certificate that is not valid was found.")
        End If
    Next i

    ' Open the AD store and retrieve a certificate based
    ' on a string passed into the function. Add any valid
    ' certificates found to the local store.

    ADStore.Open(CAPICOM_ACTIVE_DIRECTORY_USER_STORE, certname, _
        CAPICOM_STORE_OPEN_READ_ONLY)
    MsgBox("There are " & ADStore.Certificates.Count & _
        " certificates in the AD store.")

    For i = 1 To ADStore.Certificates.Count
        If ADStore.Certificates.Item(i).IsValid Then
            ADStore.Certificates.Item(i).Display()
            LocalStore.Add(ADStore.Certificates.Item(i))
        Else
            MsgBox("the certificate from the AD store is not valid.")
        End If
    Next i

    LocalStore = Nothing
    ADStore = Nothing
    MsgBox("Sub finished without error ")
    Exit Sub
errorhandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found:" & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
