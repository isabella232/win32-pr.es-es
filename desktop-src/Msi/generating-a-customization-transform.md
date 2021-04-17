---
description: Puede generar un archivo de transformación mediante MsiDatabaseGenerateTransform o el método GenerateTransform del objeto de base de datos.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Generar una transformación de personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f73609b7be60dbfe236d31ed5a865e86ff6e310
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652831"
---
# <a name="generating-a-customization-transform"></a>Generar una transformación de personalización

Puede generar un archivo de transformación mediante [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) o el [**método GenerateTransform**](database-generatetransform.md) del objeto de [**base de datos**](database-object.md). Un ejemplo de esto se proporciona en el SDK de Windows Installer como la utilidad WiGenXfm.vbs. El siguiente fragmento de código, Gen.vbs, también muestra el método **GenerateTransform** y es para su uso con Windows Script Host.


```VB
'Gen.vbs. Argument(0) is the original database. Argument(1) is the
'    customized database. Argument(2) is the transform file.
 
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is gen.vbs [original database] [customized database] [transform file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer") 
' Open databases
Dim database1 : Set database1 = 
    installer.OpenDatabase(Wscript.Arguments(0), 0) 
Dim database2 : Set database2 = 
    installer.OpenDatabase(Wscript.Arguments(1), 0) 
' Generate transform
Dim transform : transform = Database2.GenerateTransform(Database1,
    Wscript.Arguments(2))
```



Para generar el archivo de transformación MNPtrans. MST desde la base de datos de MNP2000.msi original y la base de datos de MNP2000t.msi modificada en la [Personalización de una base de datos original](customizing-an-original-database.md), cambie los directorios a la carpeta que contiene Gen.vbs, la base de datos original y la base de datos del instalador actualizada y escriba la siguiente línea de comandos.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans. MST**

[Continuar](adding-summary-information-to-customization-transform.md)

 

 



