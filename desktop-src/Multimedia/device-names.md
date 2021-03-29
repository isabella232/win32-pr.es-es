---
title: Nombres de dispositivo
description: Nombres de dispositivo
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104487046"
---
# <a name="device-names"></a><span data-ttu-id="49432-103">Nombres de dispositivo</span><span class="sxs-lookup"><span data-stu-id="49432-103">Device Names</span></span>

<span data-ttu-id="49432-104">Para cada tipo de dispositivo, puede haber varios controladores MCI que compartan el conjunto de comandos pero operen en formatos de datos diferentes.</span><span class="sxs-lookup"><span data-stu-id="49432-104">For each device type, there might be several MCI drivers that share the command set but operate on different data formats.</span></span> <span data-ttu-id="49432-105">Para identificar de forma única un controlador MCI, MCI usa *nombres de dispositivo*.</span><span class="sxs-lookup"><span data-stu-id="49432-105">To uniquely identify an MCI driver, MCI uses *device names*.</span></span>

<span data-ttu-id="49432-106">Los nombres de los dispositivos se identifican en la \[ \] sección MCI del archivo SYSTEM.INI o en la parte adecuada del registro.</span><span class="sxs-lookup"><span data-stu-id="49432-106">Device names are identified either in the \[mci\] section of the SYSTEM.INI file or in the appropriate part of the registry.</span></span> <span data-ttu-id="49432-107">Esta información identifica todos los controladores MCI en Windows.</span><span class="sxs-lookup"><span data-stu-id="49432-107">This information identifies all MCI drivers to Windows.</span></span> <span data-ttu-id="49432-108">Las entradas de la \[ \] sección MCI usan el formato siguiente:</span><span class="sxs-lookup"><span data-stu-id="49432-108">The entries in the \[mci\] section use the following form:</span></span>

<span data-ttu-id="49432-109">*nombre del dispositivo \_ nombre* de  =  *\_ archivo. extensión*</span><span class="sxs-lookup"><span data-stu-id="49432-109">*device\_name* = *driver\_filename.extension*</span></span>

<span data-ttu-id="49432-110">En el ejemplo siguiente se muestra \[ una \] sección típica de mci de SYSTEM.INI:</span><span class="sxs-lookup"><span data-stu-id="49432-110">The following example shows a typical \[mci\] section from SYSTEM.INI:</span></span>


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



<span data-ttu-id="49432-111">Si se instala un controlador MCI con un nombre de dispositivo que ya existe en SYSTEM.INI o en el registro, el sistema anexa un entero al nombre de dispositivo del nuevo controlador y crea un nombre de dispositivo único.</span><span class="sxs-lookup"><span data-stu-id="49432-111">If an MCI driver is installed using a device name that already exists in SYSTEM.INI or the registry, the system appends an integer to the device name of the new driver, creating a unique device name.</span></span> <span data-ttu-id="49432-112">En el ejemplo anterior, se asignaría el nombre de dispositivo "cdaudio1" a un controlador adicional instalado con el nombre de dispositivo "cdaudio".</span><span class="sxs-lookup"><span data-stu-id="49432-112">In the preceding example, an additional driver installed using the "cdaudio" device name would be assigned the device name "cdaudio1".</span></span>

 

 




