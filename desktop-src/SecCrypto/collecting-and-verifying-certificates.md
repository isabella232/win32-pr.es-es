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
# <a name="collecting-and-verifying-certificates"></a><span data-ttu-id="9a684-103">Recopilación y comprobación de certificados</span><span class="sxs-lookup"><span data-stu-id="9a684-103">Collecting and Verifying Certificates</span></span>

<span data-ttu-id="9a684-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9a684-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9a684-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="9a684-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="9a684-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="9a684-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="9a684-107">A menudo es necesario recopilar y comprobar un grupo de [*certificados*](../secgloss/c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="9a684-107">Often a group of [*certificates*](../secgloss/c-gly.md) needs to be collected and verified.</span></span> <span data-ttu-id="9a684-108">Esto se suele hacer para preparar un grupo de destinatarios para un mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="9a684-108">This would often be done to prepare a group of recipients for an enveloped message.</span></span> <span data-ttu-id="9a684-109">En el ejemplo siguiente, se enumeran y se comprueba la validez de los certificados de un almacén local.</span><span class="sxs-lookup"><span data-stu-id="9a684-109">In the example that follows, the certificates in a local store are enumerated and checked for validity.</span></span> <span data-ttu-id="9a684-110">A continuación, se abre un almacén de Active Directory para recuperar y agregar los certificados nuevos del almacén local.</span><span class="sxs-lookup"><span data-stu-id="9a684-110">Next, an Active Directory store is opened to retrieve and add to the local store new certificates.</span></span> <span data-ttu-id="9a684-111">Se comprueba la validez de los certificados recuperados del almacén de Active Directory y, si es válido, se agregan al almacén local.</span><span class="sxs-lookup"><span data-stu-id="9a684-111">The certificates retrieved from the active directory store are checked for validity and, if valid, are added to the local store.</span></span> <span data-ttu-id="9a684-112">A continuación, se cierran ambos almacenes.</span><span class="sxs-lookup"><span data-stu-id="9a684-112">Both stores are then closed.</span></span>

<span data-ttu-id="9a684-113">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="9a684-113">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="9a684-114">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="9a684-114">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="9a684-115">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="9a684-115">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="9a684-116">En este ejemplo, el nombre del almacén local se pasa como un parámetro de cadena.</span><span class="sxs-lookup"><span data-stu-id="9a684-116">In this example, the name of the local store is passed in as a string parameter.</span></span> <span data-ttu-id="9a684-117">Una cadena que indica los criterios de búsqueda para los certificados del almacén de Active Directory se pasa también como parámetro.</span><span class="sxs-lookup"><span data-stu-id="9a684-117">A string indicating the search criteria for certificates in the Active Directory store is also passed in as a parameter.</span></span>


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



 

 
