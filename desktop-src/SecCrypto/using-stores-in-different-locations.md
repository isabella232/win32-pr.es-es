---
description: En el ejemplo siguiente se muestran aspectos del trabajo con el objeto Store. Muestra la apertura de almacenes en el \_ almacén de memoria CAPICOM \_ , el almacén de \_ usuarios actual de CAPICOM y las ubicaciones del almacén de \_ \_ \_ máquinas locales de CAPICOM \_ \_ .
ms.assetid: bfb7ff48-1d6b-404f-9dd4-6de1898354b7
title: Usar almacenes en ubicaciones diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e22fa4d4eca4748d6c4652a8b33d22a1db492a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811228"
---
# <a name="using-stores-in-different-locations"></a><span data-ttu-id="23c7f-104">Usar almacenes en ubicaciones diferentes</span><span class="sxs-lookup"><span data-stu-id="23c7f-104">Using Stores in Different Locations</span></span>

<span data-ttu-id="23c7f-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="23c7f-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="23c7f-106">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="23c7f-106">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="23c7f-107">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="23c7f-107">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="23c7f-108">En el ejemplo siguiente se muestran aspectos del trabajo con el objeto [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="23c7f-108">The following example demonstrates aspects of working with the [**Store**](store.md) object.</span></span> <span data-ttu-id="23c7f-109">Muestra la apertura de almacenes en el \_ almacén de memoria CAPICOM \_ , el almacén de \_ usuarios actual de CAPICOM y las ubicaciones del almacén de \_ \_ \_ máquinas locales de CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="23c7f-109">It shows opening stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span>

<span data-ttu-id="23c7f-110">En el ejemplo se muestra la exportación de [*certificados*](../secgloss/c-gly.md) desde un [*almacén*](../secgloss/c-gly.md)abierto, la escritura de los certificados exportados en un archivo, su lectura y su importación en un almacén diferente.</span><span class="sxs-lookup"><span data-stu-id="23c7f-110">The example shows exporting [*certificates*](../secgloss/c-gly.md) from an open [*store*](../secgloss/c-gly.md), writing the exported certificates to a file, reading them back in and importing them into a different store.</span></span> <span data-ttu-id="23c7f-111">Los certificados recién importados se enumeran y se muestran.</span><span class="sxs-lookup"><span data-stu-id="23c7f-111">The newly imported certificates are then enumerated and displayed.</span></span>

<span data-ttu-id="23c7f-112">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="23c7f-112">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="23c7f-113">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="23c7f-113">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="23c7f-114">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="23c7f-114">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>


```VB
Sub OpenStores()

    On Error GoTo ErrorHandler

    'Open Memory, current user, and local machine stores
    Dim MemoryStore As New Store
    Dim CurrentUserStore As New Store
    Dim LocalMachineStore As New Store
    Dim NumCerts As Integer

    MemoryStore.Open(CAPICOM_MEMORY_STORE, "MemStore", _
        CAPICOM_STORE_OPEN_READ_WRITE)
    CurrentUserStore.Open(CAPICOM_CURRENT_USER_STORE, _
        CAPICOM_MY_STORE, CAPICOM_STORE_OPEN_READ_ONLY)
    LocalMachineStore.Open(CAPICOM_LOCAL_MACHINE_STORE, _
        CAPICOM_CA_STORE, CAPICOM_STORE_OPEN_READ_ONLY)

    ' Check the number of certificates in the stores.
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the memory store. ")
    NumCerts = CurrentUserStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the current user store. ")
    NumCerts = LocalMachineStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates in the local machine store. ")


    '  Export the certificates in the current user MY store
    '  to a file.
    Dim ExportString As String
    ExportString = CurrentUserStore.Export
Open "Exportcerts.txt" For Output As #1
Write #1, ExportString
Close #1

    ' Read the store the file.
    Dim importString As String
Open "exportcerts.txt" For Input As #2
Input #2, importString
Close #2
    MemoryStore.Import(importString)

    ' Check the number of certificates in the memory store after 
    ' import()
    NumCerts = MemoryStore.Certificates.Count
    MsgBox("There are " & NumCerts & _
        " certificates now in the memory store. ")

    ' Enumerate the certificates in the memory store and display each
    ' certificate
    Dim i As Long
    For i = 1 To NumCerts
        MemoryStore.Certificates.Item(i).Display()
    Next i

    ' Release the store objects
    MemoryStore = Nothing
    CurrentUserStore = Nothing
    LocalMachineStore = Nothing
    Exit Sub
ErrorHandler:
    If Err.Number > 0 Then
        MsgBox("Visual Basic error found: " & Err.Description)
    Else
        MsgBox("CAPICOM error found : " & Err.Number)
    End If
End Sub
```



 

 
