---
description: En el ejemplo siguiente se muestra cómo rellenar la tabla MsiDigitalCertificate y la tabla MsiDigitalSignature mediante una subrutina Visual Basic para Aplicaciones (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Crear una instalación firmada completamente comprobada mediante automatización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99267feffac71401f36635c08fa7f9f6598a0c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001732"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a><span data-ttu-id="4d466-103">Crear una instalación firmada completamente comprobada mediante automatización</span><span class="sxs-lookup"><span data-stu-id="4d466-103">Authoring a Fully Verified Signed Installation Using Automation</span></span>

<span data-ttu-id="4d466-104">En el ejemplo siguiente se muestra cómo rellenar la tabla [MsiDigitalCertificate](msidigitalcertificate-table.md) y la [tabla MsiDigitalSignature](msidigitalsignature-table.md) mediante una subrutina Visual Basic para aplicaciones (VBA).</span><span class="sxs-lookup"><span data-stu-id="4d466-104">The following sample demonstrates how to populate the [MsiDigitalCertificate table](msidigitalcertificate-table.md) and [MsiDigitalSignature table](msidigitalsignature-table.md) by using a Visual Basic for Applications (VBA) subroutine.</span></span> <span data-ttu-id="4d466-105">Para obtener más información acerca de cómo proteger los paquetes de Windows Installer, consulte [directrices para la creación de instalaciones seguras](guidelines-for-authoring-secure-installations.md).</span><span class="sxs-lookup"><span data-stu-id="4d466-105">For more information about securing Windows Installer packages see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md).</span></span>

<span data-ttu-id="4d466-106">El [**método FileSignatureInfo**](installer-filesignatureinfo.md) devuelve una matriz SafeArray de bytes.</span><span class="sxs-lookup"><span data-stu-id="4d466-106">The [**FileSignatureInfo method**](installer-filesignatureinfo.md) returns a SAFEARRAY of bytes.</span></span> <span data-ttu-id="4d466-107">Para obtener más información, vea el [**tipo de datos SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="4d466-107">For more information, see the [**SAFEARRAY Data Type**](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span> <span data-ttu-id="4d466-108">Los datos de esta matriz se deben convertir a Unicode porque Visual Basic no tiene una manera de escribir bytes directamente en un archivo.</span><span class="sxs-lookup"><span data-stu-id="4d466-108">The data from this array must be converted to Unicode because Visual Basic does not have a way to write bytes straight into a file.</span></span> <span data-ttu-id="4d466-109">El [**método SetStream**](record-setstream.md) puede usar el archivo de datos convertidos para escribir datos de secuencia en un campo de registro especificado de un [**objeto de registro**](record-object.md).</span><span class="sxs-lookup"><span data-stu-id="4d466-109">The [**SetStream method**](record-setstream.md) can then use the file of converted data to write stream data into a specified record field of a [**Record object**](record-object.md).</span></span> <span data-ttu-id="4d466-110">Tenga en cuenta que la conversión de los datos de bytes en Unicode puede cambiar potencialmente los datos y que los datos convertidos deben coincidir con los datos originales para comprobar la firma correcta.</span><span class="sxs-lookup"><span data-stu-id="4d466-110">Note that conversion of the byte data to Unicode can potentially change the data and that the converted data must match the original data for correct signature verification.</span></span> <span data-ttu-id="4d466-111">El autor del paquete debe asegurarse de que los datos originales y convertidos coincidan.</span><span class="sxs-lookup"><span data-stu-id="4d466-111">The package author must ensure that the original and converted data match.</span></span>


```VB
Sub PopulateDigitalSignature()

    Dim Installer As Object
    Dim Database As Object
    Dim x() As Byte
    
    Const szSignedCabinet = "c:\test.cab"
    Const szCertFile = "c:\temp\test.cer"
    Const szDatabase = "c:\test.msi"
        
    Set Installer = CreateObject("WindowsInstaller.Installer")
    
    x = Installer.FileSignatureInfo(szSignedCabinet, 0, msiSignatureInfoCertificate)
    
    Dim fs, ts
    Dim s As String
    Set fs = CreateObject("Scripting.FileSystemObject")
    Set ts = fs.CreateTextFile(szCertFile, True)        'Create a file
    
    s = StrConv(x, vbUnicode)
    ts.Write s
    ts.Close
        
    Set Database = Installer.OpenDatabase(szDatabase, msiOpenDatabaseModeTransact)
    Set ViewCert = Database.OpenView("SELECT * FROM `MsiDigitalCertificate`")
    ViewCert.Execute 0
    Set ViewSig = Database.OpenView("SELECT * FROM `MsiDigitalSignature`")
    ViewSig.Execute 0
    
    Set RecordCert = Installer.CreateRecord(2)
    RecordCert.StringData(1) = "Test"
    RecordCert.SetStream 2, szCertFile
    ViewCert.Modify msiViewModifyInsert, RecordCert
    
    Set RecordSig = Installer.CreateRecord(4)
    RecordSig.StringData(1) = "Media"
    RecordSig.StringData(2) = "1"
    RecordSig.StringData(3) = "Test"
    ViewSig.Modify msiViewModifyInsert, RecordSig
    
    Database.Commit
      fs.DeleteFile(szCertFile)
End Sub
```



 

 
