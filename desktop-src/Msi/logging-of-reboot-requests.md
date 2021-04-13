---
description: Si la acción InstallValidate detecta la instalación de un archivo en uso, muestra el cuadro de diálogo FilesInUse y registra la información siguiente.
ms.assetid: 59237d2c-6dda-4edc-bbaf-39c6b4c221b9
title: Registro de solicitudes de reinicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a256f9042dc40633932a36e288ad18d8194f4739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104547003"
---
# <a name="logging-of-reboot-requests"></a><span data-ttu-id="dfd14-103">Registro de solicitudes de reinicio</span><span class="sxs-lookup"><span data-stu-id="dfd14-103">Logging of Reboot Requests</span></span>

<span data-ttu-id="dfd14-104">Si la [acción InstallValidate](installvalidate-action.md) detecta la instalación de un archivo en uso, muestra el [cuadro de diálogo FilesInUse](filesinuse-dialog.md) y registra la información siguiente.</span><span class="sxs-lookup"><span data-stu-id="dfd14-104">If the [InstallValidate action](installvalidate-action.md) detects the installation of a file in use it displays the [FilesInUse Dialog](filesinuse-dialog.md) and logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct1.dll is being held in use
by the following process: Name: test, Id: 137, Window Title: 'Test'.
```

<span data-ttu-id="dfd14-105">Si el instalador detecta que está a punto de sobrescribir un archivo que está en uso, registra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="dfd14-105">If the installer detects that it is about to overwrite a file that is in use, it logs the following information.</span></span>

``` syntax
Info 1603. The file E:\testdb\Test\CustAct2.dll is being held in use.

Info 1903.Scheduling reboot operation: Deleting file [filename]. Must 
reboot to complete operation.
```

<span data-ttu-id="dfd14-106">El \[ token de nombre de archivo \] puede contener realmente una ruta de acceso a un archivo con una extensión. Rbf.</span><span class="sxs-lookup"><span data-stu-id="dfd14-106">The \[filename\] token may actually contain a path to a file with an .rbf extension.</span></span> <span data-ttu-id="dfd14-107">En este caso, el archivo. Rbf es realmente el archivo original registrado por el mensaje 1603, al que se le ha cambiado el nombre al archivo. Rbf.</span><span class="sxs-lookup"><span data-stu-id="dfd14-107">In this case the .rbf file is actually the original file logged by the 1603 message which has been renamed to the .rbf file.</span></span> <span data-ttu-id="dfd14-108">Primero se cambia el nombre del archivo que se está usando con una extensión. Rbf y, a continuación, se elimina.</span><span class="sxs-lookup"><span data-stu-id="dfd14-108">The file that's in use is first renamed with an .rbf extension and then deleted.</span></span>

<span data-ttu-id="dfd14-109">Para obtener más información acerca de por qué el instalador está intentando sobrescribir este archivo en particular, puede usar la opción de registro detallado.</span><span class="sxs-lookup"><span data-stu-id="dfd14-109">To obtain more information about why the installer is attempting to overwrite this particular file, you can use the verbose logging option.</span></span> <span data-ttu-id="dfd14-110">Use el \_ valor detallado de INSTALLLOGMODE en una llamada a [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) o use la opción de salida detallada de las [Opciones](command-line-options.md)de la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="dfd14-110">Use the INSTALLLOGMODE\_VERBOSE value in a call to [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) or use the verbose output option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="dfd14-111">Esto registra la siguiente información.</span><span class="sxs-lookup"><span data-stu-id="dfd14-111">This logs the following information.</span></span>

``` syntax
MSI (s) (D0:F0): File: E:\testdb\Test\CustAct2.dll;  Overwrite;  
REINSTALLMODE specifies all files to be overwritten
```

<span data-ttu-id="dfd14-112">El registro incluirá un mensaje como "el archivo existente es una versión anterior" o "el archivo existente está dañado (suma de comprobación no válida)"</span><span class="sxs-lookup"><span data-stu-id="dfd14-112">The log will include a message such as "Existing file is a lower version" or "Existing file is corrupt (invalid checksum)"</span></span>

 

 



