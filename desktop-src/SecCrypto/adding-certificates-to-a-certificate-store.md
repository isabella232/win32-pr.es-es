---
description: Los certificados se pueden agregar o quitar de los almacenes de certificados si el almacén se abre con permiso de lectura y escritura.
ms.assetid: a1cb6e1e-0702-4f73-827e-3f9e9237b4b6
title: Agregar certificados a un almacén de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6f4c018be697f48e40d52480f49694762fb956f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545670"
---
# <a name="adding-certificates-to-a-certificate-store"></a><span data-ttu-id="83f23-103">Agregar certificados a un almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="83f23-103">Adding Certificates to a Certificate Store</span></span>

<span data-ttu-id="83f23-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="83f23-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="83f23-105">En su lugar, use la .NET Framework para implementar características de seguridad.</span><span class="sxs-lookup"><span data-stu-id="83f23-105">Instead, use the .NET Framework to implement security features.</span></span> <span data-ttu-id="83f23-106">Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]</span><span class="sxs-lookup"><span data-stu-id="83f23-106">For more information, see [Alternatives to Using CAPICOM](alternatives-to-using-capicom.md).\]</span></span>

<span data-ttu-id="83f23-107">Los [*certificados*](../secgloss/c-gly.md) se pueden agregar o quitar de los [*almacenes de certificados*](../secgloss/c-gly.md) si el almacén se abre con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="83f23-107">[*Certificates*](../secgloss/c-gly.md) can be added to or removed from [*certificate stores*](../secgloss/c-gly.md) if the store is opened with read/write permission.</span></span> <span data-ttu-id="83f23-108">No se concede permiso de lectura y escritura a los almacenes de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83f23-108">Read/write permission is not granted to Active Directory stores.</span></span> <span data-ttu-id="83f23-109">Aunque los certificados se pueden agregar o quitar de los almacenes de memoria, los cambios en los almacenes de memoria no se conservan entre las sesiones.</span><span class="sxs-lookup"><span data-stu-id="83f23-109">While certificates can be added to or removed from memory stores, changes in memory stores are not persisted between sessions.</span></span>

<span data-ttu-id="83f23-110">Los certificados se pueden agregar a un almacén de certificados abierto con permisos de lectura y escritura mediante el método **Add** .</span><span class="sxs-lookup"><span data-stu-id="83f23-110">Certificates can be added to a certificate store that is opened with read/write permission by using the **Add** method.</span></span> <span data-ttu-id="83f23-111">Se puede quitar un certificado de un almacén de certificados que se abre con permiso de lectura y escritura mediante el método **Remove** .</span><span class="sxs-lookup"><span data-stu-id="83f23-111">A certificate can be removed from a certificate store that is opened with read/write permission by using the **Remove** method.</span></span> <span data-ttu-id="83f23-112">Se pueden crear nuevas tiendas y guardarlas en el \_ almacén de usuarios actual de CAPICOM y en las \_ ubicaciones del almacén de \_ \_ máquinas locales de CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="83f23-112">New stores can be created and saved in the CAPICOM\_CURRENT\_USER\_STORE and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="83f23-113">Los almacenes recién creados en cualquiera de estas ubicaciones pueden abrirse con permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="83f23-113">Newly created stores in either of these locations can be opened with read/write permission.</span></span>

<span data-ttu-id="83f23-114">En el ejemplo siguiente, se abren dos almacenes de certificados.</span><span class="sxs-lookup"><span data-stu-id="83f23-114">In the following example, two certificate stores are opened.</span></span> <span data-ttu-id="83f23-115">Los certificados de asuntos con los apellidos que empiezan por F se recuperan del almacén de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="83f23-115">Certificates of subjects with last names beginning with F are retrieved from the Active Directory store.</span></span> <span data-ttu-id="83f23-116">El almacén de \_ usuarios actual de CAPICOM, el almacén de \_ \_ \_ almacenamiento de CA de CAPICOM, \_ se abre como un almacén de lectura y escritura, y el primer certificado de la colección de certificados del almacén de Active Directory se agrega a los certificados del almacén de CA de CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="83f23-116">The CAPICOM\_CURRENT\_USER\_STORE, CAPICOM\_CA\_STORE store is then opened as a read/write store and the first certificate from the collection of certificates in the Active Directory store is added to the certificates in the CAPICOM\_CA\_STORE.</span></span>

<span data-ttu-id="83f23-117">Para fines de demostración, en el ejemplo se muestra la apertura de almacenes en el \_ almacén de memoria CAPICOM, el almacén de \_ usuarios actual de CAPICOM \_ y las ubicaciones del almacén de \_ \_ \_ máquinas locales de CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="83f23-117">For demonstration purposes, the example shows the opening of stores in the CAPICOM\_MEMORY\_STORE, CAPICOM\_CURRENT\_USER\_STORE, and CAPICOM\_LOCAL\_MACHINE\_STORE locations.</span></span> <span data-ttu-id="83f23-118">En el ejemplo se muestra cómo exportar todos los certificados de un almacén abierto, cómo escribir los certificados exportados en un archivo, cómo volver a leerlos e importarlos en un almacén diferente.</span><span class="sxs-lookup"><span data-stu-id="83f23-118">The example shows exporting all certificates from an open store, writing the exported certificates to a file, reading them back in, and importing them into a different store.</span></span> <span data-ttu-id="83f23-119">Los certificados recién importados se enumeran y se muestran.</span><span class="sxs-lookup"><span data-stu-id="83f23-119">The newly imported certificates are them enumerated and displayed.</span></span>

<span data-ttu-id="83f23-120">En cualquier error de CAPICOM, se devuelve un valor decimal negativo de **Err. Number** .</span><span class="sxs-lookup"><span data-stu-id="83f23-120">On any CAPICOM error, a negative decimal value of **Err.Number** is returned.</span></span> <span data-ttu-id="83f23-121">Para obtener más información, consulte el [**\_ \_ código de error de CAPICOM**](capicom-error-code.md).</span><span class="sxs-lookup"><span data-stu-id="83f23-121">For more information, see [**CAPICOM\_ERROR\_CODE**](capicom-error-code.md).</span></span> <span data-ttu-id="83f23-122">Para obtener información acerca de los valores decimales positivos de **Err. Number**, consulte Winerror. h.</span><span class="sxs-lookup"><span data-stu-id="83f23-122">For information about positive decimal values of **Err.Number**, see Winerror.h.</span></span>

<span data-ttu-id="83f23-123">En el ejemplo siguiente se muestra cómo abrir almacenes de certificados utilizando el enlace temprano en la declaración de los objetos **Store** y en la creación de una instancia de esos objetos.</span><span class="sxs-lookup"><span data-stu-id="83f23-123">The following example shows opening certificate stores using early binding in the declaration of the **Store** objects and in creating an instance of those objects.</span></span>


```VB
Sub AddCert()
On Error GoTo ErrorHandler
' The following shows two different ways to declare and
' create a store object.

Dim myADstore As New Store

Dim myCAstore As Store
Set myCAstore = New Store

' In this example, the Active Directory store will be searched for a 
' certificate with a subject name that begins with the letter F. 
' This is done by using the string "SN=F*" as the name of the store.

Dim SubjectNameSN As String
SubjectNameSN = "SN=F*"

' Active Directory stores can only be opened with read-only
' access.

myADstore.Open CAPICOM_ACTIVE_DIRECTORY_USER_STORE,
                SubjectNameSN , CAPICOM_STORE_OPEN_READ_ONLY

'  This example assumes that the store opened and that
'  at least one certificate was returned.
'  A complete application would ensure that at least one certificate
'  was in the store before proceeding and would
'  also select one or more of the certificates returned
'  to be added instead of using the first certificate
'  in the collection.

'  Open the MY store so that a certificate can be added.

myCAstore.Open CAPICOM_CURRENT_USER_STORE, CAPICOM_MY_STORE,
                    CAPICOM_STORE_OPEN_READ_WRITE

myCAstore.Add myADstore.certificates.Item(1)

' Release the two store objects.

Set myCAstore = Nothing
Set myADstore = Nothing
Exit Sub

ErrorHandler:
If Err.Number > 0 Then
    MsgBox "Visual Basic error found:" & Err.Description
Else
    MsgBox "CAPICOM error found : " & Err.Number
End If
End Sub


```



 

 
