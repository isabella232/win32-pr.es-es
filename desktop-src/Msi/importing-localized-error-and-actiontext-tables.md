---
description: Las versiones de idioma localizadas de la tabla Error y la tabla ActionText se proporcionan mediante el SDK Windows Installer. Las versiones en francés de estas tablas, Error.FRA y ActionTe.FRA, se encuentran en la carpeta Intl del SDK Windows Installer.
ms.assetid: 8de687c8-c7da-497e-8a90-2404096ad100
title: Importar tablas De error localizadas y ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda0916f634d986874cd17f9871fa602277b180e1ba436e9d9786fb061f3ac4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118142255"
---
# <a name="importing-localized-error-and-actiontext-tables"></a>Importar tablas De error localizadas y ActionText

Las versiones de idioma localizadas [de la tabla Error y](error-table.md) la tabla [ActionText](actiontext-table.md) se proporcionan mediante el SDK Windows Installer. Las versiones en francés de estas tablas, Error.FRA y ActionTe.FRA, se encuentran en la carpeta Intl del SDK Windows Installer.

Puede usar el editor de tablas Orca o la utilidad Msidb.exe con el SDK para importar las versiones en francés de estas tablas en la base de datos.

En el SDK del instalador de Windows se proporciona un ejemplo del uso de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) y el método [**Import**](database-import.md) del objeto [**Database**](database-object.md) como la utilidad WiImport.vbs. El siguiente fragmento de código, Imp.vbs, también muestra el uso del método Import y se usa con Windows host de script.


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



Para importar y reemplazar la tabla Error por Error.FRA, puede usar una línea de comandos como la siguiente.

**Cscript Imp.vbs MNPFren.msi C: Nota \\ \_ Instalador Francés \\ Error.FRA**

Para importar y reemplazar la tabla ActionText por ActionTe.FRA, puede usar una línea de comandos como la siguiente.

**Cscript Imp.vbs MNPFren.msi C: \\ Nota Installer French \_ \\ ActionTe.FRA**

Vuelva a ejecutar la validación MNPFren.msi como se describe [en Validación de una actualización de instalación](validating-an-installation-upgrade.md).

[Continuar](localizing-database-columns.md)

 

 



