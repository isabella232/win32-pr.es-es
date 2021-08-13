---
description: Puede generar un archivo de transformación mediante MsiDatabaseGenerateTransform o el método GenerateTransform del objeto Database.
ms.assetid: c016fcba-0d54-4b99-bcdd-36967b2c9da0
title: Generar una transformación de personalización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b790917100cc06da97e09fd8aabf45b580e62008d23c9fc5065e6005112d8d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118636003"
---
# <a name="generating-a-customization-transform"></a>Generar una transformación de personalización

Puede generar un archivo de transformación mediante [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma) o el [**método GenerateTransform**](database-generatetransform.md) del objeto [**Database**](database-object.md). Se proporciona un ejemplo de esto en el SDK Windows Installer como la utilidad WiGenXfm.vbs. El siguiente fragmento de código, Gen.vbs, también muestra el método **GenerateTransform** y se usa con Windows host de script.


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



Para generar el archivo de transformación MNPtrans.mst a partir de la base de datos MNP2000.msi original y la base de datos MNP2000t.msi que modificó en Personalización de una base de datos [original,](customizing-an-original-database.md)cambie los directorios a la carpeta que contiene Gen.vbs, la base de datos original y la base de datos del instalador actualizada y escriba la línea de comandos siguiente.

**Cscript.exe Gen.vbs MNP2000.msi MNP2000t.msi MNPtrans.mst**

[Continuar](adding-summary-information-to-customization-transform.md)

 

 



