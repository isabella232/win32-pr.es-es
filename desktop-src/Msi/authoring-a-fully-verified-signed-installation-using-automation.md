---
description: En el ejemplo siguiente se muestra cómo rellenar la tabla MsiDigitalCertificate y la tabla MsiDigitalSignature mediante una subrutina Visual Basic para Aplicaciones (VBA).
ms.assetid: 3a23a721-0672-4eac-bdf2-434282b92590
title: Creación de una instalación firmada totalmente verificada mediante Automation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27f1b0b90296ad92e471449213e86721482a545ff1932458b2ad6b21d47b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559105"
---
# <a name="authoring-a-fully-verified-signed-installation-using-automation"></a>Creación de una instalación firmada totalmente verificada mediante Automation

En el ejemplo siguiente se muestra cómo rellenar la tabla [MsiDigitalCertificate](msidigitalcertificate-table.md) y la tabla [MsiDigitalSignature](msidigitalsignature-table.md) mediante una subrutina Visual Basic para Aplicaciones (VBA). Para obtener más información sobre cómo proteger los paquetes Windows Installer, vea [Directrices para crear instalaciones seguras.](guidelines-for-authoring-secure-installations.md)

El [**método FileSignatureInfo**](installer-filesignatureinfo.md) devuelve una SAFEARRAY de bytes. Para obtener más información, vea el [**tipo de datos SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray). Los datos de esta matriz se deben convertir a Unicode porque Visual Basic no tiene una manera de escribir bytes directamente en un archivo. A [**continuación, el**](record-setstream.md) método SetStream puede usar el archivo de datos convertidos para escribir datos de secuencia en un campo de registro especificado de un [**objeto Record**](record-object.md). Tenga en cuenta que la conversión de los datos de bytes a Unicode puede cambiar los datos y que los datos convertidos deben coincidir con los datos originales para la comprobación correcta de la firma. El autor del paquete debe asegurarse de que los datos originales y convertidos coinciden.


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



 

 
