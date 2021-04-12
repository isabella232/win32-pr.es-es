---
description: El programa FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino del historial de archivos asignado actualmente.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496186"
---
# <a name="fhmanagewexe"></a><span data-ttu-id="533db-103">FhManagew.exe</span><span class="sxs-lookup"><span data-stu-id="533db-103">FhManagew.exe</span></span>

<span data-ttu-id="533db-104">El programa FhManagew.exe elimina las versiones de archivo que superan una antigüedad especificada del dispositivo de destino del historial de archivos asignado actualmente.</span><span class="sxs-lookup"><span data-stu-id="533db-104">The FhManagew.exe program deletes file versions that exceed a specified age from the currently assigned File History target device.</span></span>

<span data-ttu-id="533db-105">Este programa está disponible en Windows 8 y Windows Server 2012 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="533db-105">This program is available in Windows 8 and Windows Server 2012 and later.</span></span>

<span data-ttu-id="533db-106">Para ejecutar este programa, vaya al menú **Inicio** , haga clic en **Ejecutar** y escriba el siguiente comando.</span><span class="sxs-lookup"><span data-stu-id="533db-106">To execute this program, go to the **Start** menu, click **Run**, and type the following command.</span></span>

<span data-ttu-id="533db-107">*Antigüedad* **de la limpieza deFhManagew.exe**</span><span class="sxs-lookup"><span data-stu-id="533db-107">**FhManagew.exe -cleanup** *age*</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="533db-108">Parámetro</span><span class="sxs-lookup"><span data-stu-id="533db-108">Parameter</span></span></th>
<th><span data-ttu-id="533db-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="533db-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="533db-110"><span id="age"></span><span id="AGE"></span><em>antig</em></span><span class="sxs-lookup"><span data-stu-id="533db-110"><span id="age"></span><span id="AGE"></span><em>age</em></span></span><br/></td>
<td><span data-ttu-id="533db-111">Este parámetro especifica la antigüedad mínima, en días, de las versiones de archivo que se pueden eliminar.</span><span class="sxs-lookup"><span data-stu-id="533db-111">This parameter specifies the minimum age, in days, of file versions that can be deleted.</span></span> <span data-ttu-id="533db-112">Se elimina una versión de archivo si se cumplen las dos condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="533db-112">A file version is deleted if both of the following conditions are true:</span></span><br/>
<ul>
<li><span data-ttu-id="533db-113">La versión del archivo es anterior a la edad especificada.</span><span class="sxs-lookup"><span data-stu-id="533db-113">The file version is older than the specified age.</span></span></li>
<li><span data-ttu-id="533db-114">El archivo ya no se incluye en el ámbito de protección o hay una versión más reciente del mismo archivo en el dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="533db-114">The file is no longer included in the protection scope, or there is a newer version of the same file on the target device.</span></span></li>
</ul>
<span data-ttu-id="533db-115">Si el parámetro <em>Age</em> está establecido en cero, se eliminarán todas las versiones de archivo, excepto la versión más reciente de cada archivo que se encuentre actualmente en el ámbito de protección.</span><span class="sxs-lookup"><span data-stu-id="533db-115">If the <em>age</em> parameter is set to zero, all file versions are deleted, except for the newest version of each file that is currently present in the protection scope.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="533db-116">Para suprimir todos los resultados de este programa, use la opción de línea de comandos **-Quiet** como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="533db-116">To suppress all output from this program, use the **-quiet** command-line option as follows.</span></span>

<span data-ttu-id="533db-117">**FhManagew.exe-limpieza** de *edad* **-Quiet**</span><span class="sxs-lookup"><span data-stu-id="533db-117">**FhManagew.exe -cleanup** *age* **-quiet**</span></span>

## <a name="examples"></a><span data-ttu-id="533db-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="533db-118">Examples</span></span>



| <span data-ttu-id="533db-119">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="533db-119">Example</span></span>                                                                                                                                                                                                      | <span data-ttu-id="533db-120">Descripción</span><span class="sxs-lookup"><span data-stu-id="533db-120">Description</span></span>                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="533db-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe-Cleanup 30**</span><span class="sxs-lookup"><span data-stu-id="533db-121"><span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**</span></span><br/>                                 | <span data-ttu-id="533db-122">Elimine todas las versiones de archivo que tengan más de un mes.</span><span class="sxs-lookup"><span data-stu-id="533db-122">Delete all file versions that are older than one month.</span></span><br/>                        |
| <span data-ttu-id="533db-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Cleanup 365-Quiet**</span><span class="sxs-lookup"><span data-stu-id="533db-123"><span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**</span></span><br/> | <span data-ttu-id="533db-124">Elimine todas las versiones de archivo que tengan más de un año y supriman todos los resultados.</span><span class="sxs-lookup"><span data-stu-id="533db-124">Delete all file versions that are older than one year and suppress all output.</span></span><br/> |



 

 

 




