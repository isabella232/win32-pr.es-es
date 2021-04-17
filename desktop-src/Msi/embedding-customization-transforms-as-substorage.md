---
description: Puede almacenar la transformación de personalización en un almacenamiento del paquete Windows Installer para garantizar que la transformación esté siempre disponible cuando el paquete de instalación esté disponible.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Incrustar transformaciones de personalización como subalmacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd275d36b37b2e29ae166a2a464a62495d2ca9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652750"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Incrustar transformaciones de personalización como subalmacenamiento

Puede almacenar la transformación de personalización en un almacenamiento del paquete Windows Installer para garantizar que la transformación esté siempre disponible cuando el paquete de instalación esté disponible. Vea [transformaciones incrustadas](embedded-transforms.md). Un ejemplo de esto se proporciona en el SDK de Windows Installer como la utilidad WiSubStg.vbs. En el siguiente fragmento de código, Emb.vbs, también se muestra el uso de la [tabla Storages](-storages-table.md) para agregar una transformación incrustada que se usa con Windows Script Host.


```VB
'Emb.vbs. Argument(0) is the original database. Argument(1) is the
'    path to the transform file. Argument(2) is the name of the storage.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
 WScript.Echo "Usage is emb.vbs [original database] [transform] [storage name]"
 WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Nothing
Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
 
' Evaluate command-line arguments and set open and update modes
Dim databasePath: databasePath = Wscript.Arguments(0)
Dim importPath  : importPath = Wscript.Arguments(1)
Dim storageName : storageName = Wscript.Arguments(2)
 
' Open database and create a view on the _Storages table
Dim sqlQuery : sqlQuery = "SELECT `Name`,`Data` FROM _Storages"
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim view     : Set view = database.OpenView(sqlQuery)
 
'Create and Insert the row.
Dim record   : Set record = installer.CreateRecord(2)
record.StringData(1) = storageName
view.Execute record
 
'Insert storage - copy data into stream
record.SetStream 2, importPath
view.Modify 3, record
database.Commit
Set view = Nothing
Set database = Nothing
```



Para agregar un almacenamiento llamado MNPtrans1 a MNP2000.msi y que contenga la transformación que creó en [Agregar información de resumen a la transformación de personalización](adding-summary-information-to-customization-transform.md), cambie los directorios a la carpeta que contiene Emb.vbs, la base de datos original y el archivo de transformación y, a continuación, escriba la siguiente línea de comandos.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans. MST MNPtrans1**

Esto completa el ejemplo de transformación de personalización. Después de incrustar la transformación en MNPtrans. MST, la transformación siempre está disponible con el paquete de instalación. No es necesario que el archivo MNPtrans. MST se encuentre en el origen para aplicar la transformación.

Quite MNPtrans. MST de la carpeta que contiene el paquete de instalación de ejemplo. Haga clic en el icono de MNP2000.msi para iniciar una instalación o use la siguiente línea de comandos.

**msiexec/i MNP2000.msi**

Tenga en cuenta que esto instala el producto sin las personalizaciones. Para instalar con las personalizaciones, escriba la siguiente línea de comandos. Use un signo de dos puntos para indicar que el valor de la propiedad [**TRANSformations**](transforms.md) hace referencia a una transformación incrustada.

msiexec/i MNP2000.msi transformaciones =: MNPtrans1

Tenga en cuenta que la característica de puerta no aparece en el árbol de selección de características y que los componentes de la característica de puerta no se instalan incluso si se selecciona un tipo de instalación completo en la interfaz de usuario.

## <a name="next-example"></a>Ejemplo siguiente

[Un pequeño ejemplo de revisión de actualización](a-small-update-patching-example.md)

 

 



