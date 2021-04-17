---
description: Los certificados se pueden recuperar de un almacén de Active Directory donde se almacenan los certificados de los usuarios de un dominio.
ms.assetid: 5c4d1629-88f3-41f4-afb3-7791cd590e6c
title: Abrir el Active Directory almacenar y recuperar certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd60c7414aaec8b069817b47fbd2493bb11d98c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668023"
---
# <a name="opening-the-active-directory-store-and-retrieving-certificates"></a><span data-ttu-id="b54b0-103">Abrir el Active Directory almacenar y recuperar certificados</span><span class="sxs-lookup"><span data-stu-id="b54b0-103">Opening the Active Directory Store and Retrieving Certificates</span></span>

<span data-ttu-id="b54b0-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b54b0-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b54b0-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="b54b0-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="b54b0-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="b54b0-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="b54b0-107">Los [*certificados*](../secgloss/c-gly.md) se pueden recuperar de un almacén de Active Directory donde se almacenan los certificados de los usuarios de un dominio.</span><span class="sxs-lookup"><span data-stu-id="b54b0-107">[*Certificates*](../secgloss/c-gly.md) can be retrieved from an Active Directory store where the certificates of users of a domain are stored.</span></span> <span data-ttu-id="b54b0-108">Un almacén de Active Directory solo se puede abrir en el modo de solo lectura y las aplicaciones no pueden agregar o quitar certificados de un almacén de Active Directory mediante CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="b54b0-108">An Active Directory store can only be opened in the read-only mode and applications cannot added certificates to or remove certificates from an Active Directory store using CAPICOM.</span></span>

<span data-ttu-id="b54b0-109">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="b54b0-109">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="b54b0-110">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="b54b0-110">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="b54b0-111">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="b54b0-111">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="b54b0-112">En el ejemplo siguiente se muestra cómo abrir un Active Directory almacenar y recuperar certificados de ese almacén.</span><span class="sxs-lookup"><span data-stu-id="b54b0-112">The following example shows opening an Active Directory store and retrieving certificates from that store.</span></span>


```VB
Sub OpenADStore()
        On Error GoTo ErrorHandler
        Dim mystore As Store
        Set mystore = New Store
        
        ' Put a string that represents the name of a certificate 
        ' subject in SubjectNameCn. In the following example, 
        ' the * wildcard character is used in the string so that
        ' the Active Directory store will be searched for all 
        ' certificates with a subject name beginning with 'S.'
       
        Dim SubjectNameCn As String
        ' The following uses 'cn=' and the * wildcard character.
        ' Using this string, all certificates in the Active Directory
        ' store with a subject name beginning with an 'S' would
        ' be returned.

        SubjectNameCn = "CN=S*"
        
        ' Active Directory stores can only be opened with read-only
        ' access.
        
         mystore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE, _
              SubjectNameCn, CAPICOM_STORE_OPEN_READ_ONLY
        
        If mystore.Certificates.Count < 1 Then
               MsgBox "A certificate for " & SubjectNameCn & _
                      " was not found "
        Else
               MsgBox "The certificate has been retrieved."
        End If
        
        Set mystore = Nothing
        Exit Sub

ErrorHandler:
         
         If Err.Number > 0 Then
               MsgBox "Visual Basic error found:" & Err.Description
         Else
               MsgBox "CAPICOM error found : " & Err.Number
         End If
End Sub
```



 

 
