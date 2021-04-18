---
description: El SDK de Windows Installer proporciona las versiones de idioma localizadas de la tabla de errores y la tabla de ActionText. Las versiones en francés de estas tablas, error. FRA y ActionTe. FRA, se encuentran en la carpeta Intl del SDK de Windows Installer.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importación de tablas de error y de ActionText localizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15d48a68ca1053a1a1c66899a17802ac337c3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652857"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importación de tablas de error y de ActionText localizadas

El SDK de Windows Installer proporciona las versiones de idioma localizadas de la tabla de [errores](error-table.md) y la [tabla de ActionText](actiontext-table.md) . Las versiones en francés de estas tablas, error. FRA y ActionTe. FRA, se encuentran en la carpeta Intl del SDK de Windows Installer.

Puede usar el editor de tablas Orca o la utilidad Msidb.exe proporciona el SDK para importar las versiones en francés de estas tablas en la base de datos.

Un ejemplo del uso de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) y el [**método de importación**](database-import.md) del objeto de base de [**datos**](database-object.md) se proporciona en el SDK de Windows Installer como la utilidad WiImport.vbs. En el siguiente fragmento de código, Imp.vbs, también se muestra el uso del método de importación y se usa con Windows Script Host.


```VB
'Imp.vbs. Argument(0) is the original database. Argument(1) is the
'    path of the folder containing the file to be imported. Argument(2) is the name of the file to be imported.
'
Option Explicit

' Check arguments
If WScript.Arguments.Count < 2 Then
    WScript.Echo "Usage is imp.vbs [original database] [folder path] [import file]"
    WScript.Quit(1)
End If

' Connect to Windows Installer object
On Error Resume Next
Dim installer : Set installer = Wscript.CreateObject("WindowsInstaller.Installer")
Dim databasePath : databasePath = Wscript.Arguments(0)
Dim folder : folder = Wscript.Arguments(1)
 
' Open database and process file
Dim database : Set database = installer.OpenDatabase(databasePath, 1)
Dim table : table = Wscript.Arguments(2)
database.Import folder, table 
 
' Commit database changes
database.Commit 'commit changes
Wscript.Quit 0
```



Para importar y reemplazar la tabla de errores por error. FRA puede usar una línea de comandos como la siguiente.

**Cscript Imp.vbs MNPFren.msi C: \\ Nota \_ \\ error francés del instalador. Fra**

Para importar y reemplazar la tabla ActionText con ActionTe. FRA, puede usar una línea de comandos como la siguiente.

**Cscript Imp.vbs MNPFren.msi C: \\ Nota del \_ instalador \\ Francés ActionTe. Fra**

Vuelva a ejecutar la validación en MNPFren.msi como se describe en [validación de una actualización de instalación](validating-an-installation-upgrade.md).

[Continuar](localizing-database-columns.md)

 

 



