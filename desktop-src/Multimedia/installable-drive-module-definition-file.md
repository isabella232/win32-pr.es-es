---
title: Archivo de Module-Definition de unidad instalable
description: Archivo de Module-Definition de unidad instalable
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- Controladores instalables, archivos de definición de módulo
- Controladores instalables, archivos DEF
- Controladores nstallable, función DriverProc
- DriverProc función)
- archivos de definición de módulos
- DEF (archivos)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077641"
---
# <a name="installable-drive-module-definition-file"></a><span data-ttu-id="2d945-109">Archivo de Module-Definition de unidad instalable</span><span class="sxs-lookup"><span data-stu-id="2d945-109">Installable Drive Module-Definition File</span></span>

<span data-ttu-id="2d945-110">La definición de módulo (. DEF) de un controlador instalable nombra el controlador, exporta la función [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) y define una descripción del controlador.</span><span class="sxs-lookup"><span data-stu-id="2d945-110">The module-definition (.DEF) file of an installable driver names the driver, exports the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function, and defines a driver description.</span></span> <span data-ttu-id="2d945-111">En el ejemplo siguiente se muestra un archivo de definición de módulo típico para un controlador instalable:</span><span class="sxs-lookup"><span data-stu-id="2d945-111">The following example shows a typical module-definition file for an installable driver:</span></span>


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



<span data-ttu-id="2d945-112">Algunas aplicaciones de instalación pueden abrir el controlador y recuperar la línea de descripción que se va a usar al instalar el controlador.</span><span class="sxs-lookup"><span data-stu-id="2d945-112">Some installation applications may open the driver and retrieve the description line to use when installing the driver.</span></span> <span data-ttu-id="2d945-113">Para seguir siendo compatible con estas aplicaciones de instalación, la línea de descripción debe tener este formato:</span><span class="sxs-lookup"><span data-stu-id="2d945-113">To remain compatible with these installation applications, the description line should have this form:</span></span>

<span data-ttu-id="2d945-114">  *Alias* \[ de descripción,*alias* \] ... **:\* \* * texto*</span><span class="sxs-lookup"><span data-stu-id="2d945-114">**DESCRIPTION**  *alias*\[,*alias*\]...\**:\*\*\*text*</span></span>

<span data-ttu-id="2d945-115">El *alias* especifica un nombre único para el controlador que las aplicaciones pueden usar para abrir el controlador.</span><span class="sxs-lookup"><span data-stu-id="2d945-115">The *alias* specifies a unique name for the driver that applications can use to open the driver.</span></span> <span data-ttu-id="2d945-116">El alias también sirve como nombre de valor asociado al controlador en el registro.</span><span class="sxs-lookup"><span data-stu-id="2d945-116">The alias also serves as the value name associated with the driver in the registry.</span></span> <span data-ttu-id="2d945-117">Varios alias se separan mediante comas.</span><span class="sxs-lookup"><span data-stu-id="2d945-117">Multiple aliases are separated by commas.</span></span> <span data-ttu-id="2d945-118">El *texto* describe el propósito del controlador.</span><span class="sxs-lookup"><span data-stu-id="2d945-118">The *text* describes the purpose of the driver.</span></span>

 

 