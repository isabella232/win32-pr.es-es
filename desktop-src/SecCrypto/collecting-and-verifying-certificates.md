---
description: En el ejemplo siguiente, se enumeran y se comprueba la validez de los certificados de un almacén local.
ms.assetid: 59ae22f6-aa6d-4b53-8a27-73e1e5c62755
title: Recopilación y comprobación de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0b160f373d5ade65679fcc4dd87e3c1c86dc4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687256"
---
# <a name="collecting-and-verifying-certificates"></a>Recopilación y comprobación de certificados

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

A menudo es necesario recopilar y comprobar un grupo de [*certificados*](../secgloss/c-gly.md) . Esto se suele hacer para preparar un grupo de destinatarios para un mensaje con doble cifrado. En el ejemplo siguiente, se enumeran y se comprueba la validez de los certificados de un almacén local. A continuación, se abre un almacén de Active Directory para recuperar y agregar los certificados nuevos del almacén local. Se comprueba la validez de los certificados recuperados del almacén de Active Directory y, si es válido, se agregan al almacén local. A continuación, se cierran ambos almacenes.

En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** . Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md). Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.

En este ejemplo, el nombre del almacén local se pasa como un parámetro de cadena. Una cadena que indica los criterios de búsqueda para los certificados del almacén de Active Directory se pasa también como parámetro.


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



 

 
