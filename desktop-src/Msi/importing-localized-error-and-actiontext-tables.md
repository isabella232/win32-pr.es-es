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
# <a name="importing-localized-error-and-actiontext-tables"></a><span data-ttu-id="5cf22-104">Importación de tablas de error y de ActionText localizadas</span><span class="sxs-lookup"><span data-stu-id="5cf22-104">Importing Localized Error and ActionText Tables</span></span>

<span data-ttu-id="5cf22-105">El SDK de Windows Installer proporciona las versiones de idioma localizadas de la tabla de [errores](error-table.md) y la [tabla de ActionText](actiontext-table.md) .</span><span class="sxs-lookup"><span data-stu-id="5cf22-105">Localized language versions of the [Error table](error-table.md) and [ActionText table](actiontext-table.md) are provided by the Windows Installer SDK.</span></span> <span data-ttu-id="5cf22-106">Las versiones en francés de estas tablas, error. FRA y ActionTe. FRA, se encuentran en la carpeta Intl del SDK de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="5cf22-106">The French language versions of these tables, Error.FRA and ActionTe.FRA, are located in the Intl folder of the Windows Installer SDK.</span></span>

<span data-ttu-id="5cf22-107">Puede usar el editor de tablas Orca o la utilidad Msidb.exe proporciona el SDK para importar las versiones en francés de estas tablas en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="5cf22-107">You may use the table editor Orca or the utility Msidb.exe provided with the SDK to import the French versions of these tables into the database.</span></span>

<span data-ttu-id="5cf22-108">Un ejemplo del uso de [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) y el [**método de importación**](database-import.md) del objeto de base de [**datos**](database-object.md) se proporciona en el SDK de Windows Installer como la utilidad WiImport.vbs.</span><span class="sxs-lookup"><span data-stu-id="5cf22-108">An example of using [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) and the [**Import Method**](database-import.md) of the [**Database object**](database-object.md) is provided in the Windows Installer SDK as the utility WiImport.vbs.</span></span> <span data-ttu-id="5cf22-109">En el siguiente fragmento de código, Imp.vbs, también se muestra el uso del método de importación y se usa con Windows Script Host.</span><span class="sxs-lookup"><span data-stu-id="5cf22-109">The following snippet, Imp.vbs, also illustrates the use of the Import method and is for use with Windows Script Host.</span></span>


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



<span data-ttu-id="5cf22-110">Para importar y reemplazar la tabla de errores por error. FRA puede usar una línea de comandos como la siguiente.</span><span class="sxs-lookup"><span data-stu-id="5cf22-110">To import and replace the Error table with Error.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="5cf22-111">**Cscript Imp.vbs MNPFren.msi C: \\ Nota \_ \\ error francés del instalador. Fra**</span><span class="sxs-lookup"><span data-stu-id="5cf22-111">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French Error.FRA**</span></span>

<span data-ttu-id="5cf22-112">Para importar y reemplazar la tabla ActionText con ActionTe. FRA, puede usar una línea de comandos como la siguiente.</span><span class="sxs-lookup"><span data-stu-id="5cf22-112">To import and replace the ActionText table with ActionTe.FRA you may use a command line such as the following.</span></span>

<span data-ttu-id="5cf22-113">**Cscript Imp.vbs MNPFren.msi C: \\ Nota del \_ instalador \\ Francés ActionTe. Fra**</span><span class="sxs-lookup"><span data-stu-id="5cf22-113">**Cscript Imp.vbs MNPFren.msi C:\\Note\_Installer\\French ActionTe.FRA**</span></span>

<span data-ttu-id="5cf22-114">Vuelva a ejecutar la validación en MNPFren.msi como se describe en [validación de una actualización de instalación](validating-an-installation-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="5cf22-114">Rerun validation on MNPFren.msi as described in [Validating an Installation Upgrade](validating-an-installation-upgrade.md).</span></span>

[<span data-ttu-id="5cf22-115">Continuar</span><span class="sxs-lookup"><span data-stu-id="5cf22-115">Continue</span></span>](localizing-database-columns.md)

 

 



