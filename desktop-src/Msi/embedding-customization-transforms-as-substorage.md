---
description: Puede almacenar la transformación de personalización en un almacenamiento del paquete Windows Installer para garantizar que la transformación siempre está disponible cuando el paquete de instalación está disponible.
ms.assetid: d4c022d2-a8c4-4b4e-8a6c-b14e1bc6effe
title: Inserción de transformaciones de personalización como subalmacenamiento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 175c2bd1e52a58d6c73e1e46f8b95501b016bc0e4e1069b86c9c53f47859f20c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947006"
---
# <a name="embedding-customization-transforms-as-substorage"></a>Inserción de transformaciones de personalización como subalmacenamiento

Puede almacenar la transformación de personalización en un almacenamiento del paquete Windows Installer para garantizar que la transformación siempre está disponible cuando el paquete de instalación está disponible. Vea [Transformaciones incrustadas.](embedded-transforms.md) Se proporciona un ejemplo de esto en el SDK Windows Installer como la utilidad WiSubStg.vbs. El siguiente fragmento de código, Emb.vbs, también muestra el uso de la tabla [Storages](-storages-table.md) para agregar una transformación incrustada y se usa con Windows script host.


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



Para agregar un almacenamiento denominado MNPtrans1 a MNP2000.msi y que contiene la transformación que creó en [Agregar](adding-summary-information-to-customization-transform.md)información de resumen a la transformación de personalización, cambie los directorios a la carpeta que contiene Emb.vbs, la base de datos original y el archivo de transformación y, a continuación, escriba la línea de comandos siguiente.

**Cscript.exe Emb.vbs MNP2000.msi MNPtrans.mst MNPtrans1**

Esto completa el ejemplo de transformación de personalización. Después de insertar la transformación en MNPtrans.mst, la transformación siempre está disponible con el paquete de instalación. El archivo MNPtrans.mst no necesita encontrarse en el origen para aplicar la transformación.

Quite MNPtrans.mst de la carpeta que contiene el paquete de instalación de ejemplo. Haga clic en MNP2000.msi icono de instalación para iniciar una instalación o use la siguiente línea de comandos.

**msiexec /i MNP2000.msi**

Tenga en cuenta que esto instala el producto sin las personalizaciones. Para instalar con las personalizaciones, escriba la siguiente línea de comandos. Use dos puntos para indicar que el valor de la propiedad [**TRANSFORMS**](transforms.md) hace referencia a una transformación incrustada.

msiexec /i MNP2000.msi TRANSFORMS=:MNPtrans1

Tenga en cuenta que la característica Puerta no aparece en el árbol de selección de características y que los componentes de la característica Puerta no están instalados aunque se seleccione Un tipo completo de instalación en la interfaz de usuario.

## <a name="next-example"></a>Ejemplo siguiente

[Ejemplo pequeño de aplicación de revisiones de actualizaciones](a-small-update-patching-example.md)

 

 



