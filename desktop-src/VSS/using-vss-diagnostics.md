---
description: Vsdiagview y Vssagent son herramientas que puede usar para solucionar problemas de aplicaciones VSS. Tenga en cuenta que estas herramientas se incluyen en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Uso de diagnósticos de VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696484"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="db6ec-103">Uso de diagnósticos de VSS</span><span class="sxs-lookup"><span data-stu-id="db6ec-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="db6ec-104">Vsdiagview y Vssagent son herramientas que puede usar para solucionar problemas de aplicaciones VSS.</span><span class="sxs-lookup"><span data-stu-id="db6ec-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="db6ec-105">Estas herramientas se incluyen en el kit de desarrollo de software (SDK) de Microsoft Windows para Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="db6ec-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="db6ec-106">Puede descargar la Windows SDK desde [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="db6ec-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="db6ec-107">En la instalación de Windows SDK, estas herramientas se pueden encontrar en `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (para Windows de 64 bits) y `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (para windows de 32 bits).</span><span class="sxs-lookup"><span data-stu-id="db6ec-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="db6ec-108">Recopilación de datos</span><span class="sxs-lookup"><span data-stu-id="db6ec-108">Gathering Data</span></span>

<span data-ttu-id="db6ec-109">Puede recopilar datos mediante el comando Vssagent.</span><span class="sxs-lookup"><span data-stu-id="db6ec-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="db6ec-110">**Para recopilar datos mediante Vssagent**</span><span class="sxs-lookup"><span data-stu-id="db6ec-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="db6ec-111">Para recopilar datos desde la línea de comandos, use el comando Vssagent de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="db6ec-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="db6ec-112">**vssagent-Gather** *XmlFileName \* \* *. XML**</span><span class="sxs-lookup"><span data-stu-id="db6ec-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="db6ec-113">Para ver el archivo de salida, vea la sección siguiente visualización de datos.</span><span class="sxs-lookup"><span data-stu-id="db6ec-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="db6ec-114">Ver datos</span><span class="sxs-lookup"><span data-stu-id="db6ec-114">Viewing Data</span></span>

<span data-ttu-id="db6ec-115">La aplicación Vsdiagview se puede usar para ver los datos que se recopilaron con el comando Vssagent.</span><span class="sxs-lookup"><span data-stu-id="db6ec-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="db6ec-116">Vsdiagview muestra la siguiente información acerca del equipo:</span><span class="sxs-lookup"><span data-stu-id="db6ec-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="db6ec-117">Información sobre el equipo, como la versión del sistema operativo, la memoria total disponible y la velocidad de la CPU</span><span class="sxs-lookup"><span data-stu-id="db6ec-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="db6ec-118">Los nombres y números de versión de los archivos binarios de VSS</span><span class="sxs-lookup"><span data-stu-id="db6ec-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="db6ec-119">Los nombres y las propiedades de los dispositivos de disco y volumen</span><span class="sxs-lookup"><span data-stu-id="db6ec-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="db6ec-120">Los nombres y las propiedades de las aplicaciones COM+</span><span class="sxs-lookup"><span data-stu-id="db6ec-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="db6ec-121">Los nombres de los registros de eventos que se pueden usar para diagnosticar problemas de VSS</span><span class="sxs-lookup"><span data-stu-id="db6ec-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="db6ec-122">Los nombres de los escritores de VSS y los eventos que controlan</span><span class="sxs-lookup"><span data-stu-id="db6ec-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="db6ec-123">Información sobre otros archivos del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="db6ec-123">Information about other operating system files</span></span>

<span data-ttu-id="db6ec-124">**Para ver los datos mediante Vsdiagview**</span><span class="sxs-lookup"><span data-stu-id="db6ec-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="db6ec-125">En el menú Archivo, elija **abrir** para buscar un archivo.</span><span class="sxs-lookup"><span data-stu-id="db6ec-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="db6ec-126">(La ubicación predeterminada es C: \\ vssdiag).</span><span class="sxs-lookup"><span data-stu-id="db6ec-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="db6ec-127">Haga clic en **abrir** para ver los datos.</span><span class="sxs-lookup"><span data-stu-id="db6ec-127">Click **Open** to view the data.</span></span>

 

 



