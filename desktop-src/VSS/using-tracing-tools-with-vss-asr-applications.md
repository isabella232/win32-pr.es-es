---
description: Puede usar la herramienta Logman para recopilar información de seguimiento de las aplicaciones VSS que usan la recuperación automática del sistema (ASR).
ms.assetid: 872609c8-a123-40a8-96ca-58f34d37f3d8
title: Usar herramientas de seguimiento con aplicaciones ASR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c13eee1c62cd6636eebe5bcfd35bd5abb119645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696487"
---
# <a name="using-tracing-tools-with-asr-applications"></a><span data-ttu-id="f55e2-103">Usar herramientas de seguimiento con aplicaciones ASR</span><span class="sxs-lookup"><span data-stu-id="f55e2-103">Using Tracing Tools with ASR Applications</span></span>

<span data-ttu-id="f55e2-104">Puede usar la herramienta Logman para recopilar información de seguimiento de las aplicaciones VSS que usan la [recuperación automática del sistema (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="f55e2-104">You can use the Logman tool to collect tracing information for VSS applications that use [Automated System Recovery (ASR)](using-vss-automated-system-recovery-for-disaster-recovery.md).</span></span> <span data-ttu-id="f55e2-105">Logman (logman.exe) es un controlador de seguimiento para los eventos de seguimiento y los contadores de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f55e2-105">Logman (logman.exe) is a trace controller for trace events and performance counters.</span></span> <span data-ttu-id="f55e2-106">Se incluye en Windows XP y en versiones posteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="f55e2-106">It is included in Windows XP and later versions of Windows.</span></span> <span data-ttu-id="f55e2-107">O bien, si lo prefiere, puede usar la herramienta tracelog para recopilar la misma información de seguimiento de ASR.</span><span class="sxs-lookup"><span data-stu-id="f55e2-107">Or, if you prefer, you can use the Tracelog tool to collect the same ASR tracing information.</span></span> <span data-ttu-id="f55e2-108">Tracelog se incluye en el kit de controladores de Windows (WDK).</span><span class="sxs-lookup"><span data-stu-id="f55e2-108">Tracelog is included in the Windows Driver Kit (WDK).</span></span>

<span data-ttu-id="f55e2-109">Para usar las herramientas de seguimiento con VSS, consulte [uso de herramientas de seguimiento con VSS](using-tracing-tools-with-vss.md).</span><span class="sxs-lookup"><span data-stu-id="f55e2-109">To use tracing tools with VSS, see [Using Tracing Tools with VSS](using-tracing-tools-with-vss.md).</span></span>

## <a name="using-logman"></a><span data-ttu-id="f55e2-110">Usar Logman</span><span class="sxs-lookup"><span data-stu-id="f55e2-110">Using Logman</span></span>

<span data-ttu-id="f55e2-111">En el procedimiento siguiente se describe cómo usar Logman con la aplicación ASR.</span><span class="sxs-lookup"><span data-stu-id="f55e2-111">The following procedure describes how to use Logman with your ASR application.</span></span>

<span data-ttu-id="f55e2-112">**Para usar Logman con la aplicación ASR**</span><span class="sxs-lookup"><span data-stu-id="f55e2-112">**To use Logman with your ASR application**</span></span>

1.  <span data-ttu-id="f55e2-113">Use el siguiente comando para iniciar el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="f55e2-113">Use the following command to start tracing:</span></span>

    <span data-ttu-id="f55e2-114">**Logman Start ASR-o** *x: \\ \* \* \* ASR. ETL-ETS-p {6407345b-94f2-44c8-b3db-4e076be46816} 0xFF 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="f55e2-114">**logman start asr -o** *x:\\*\*\*asr.etl -ets -p {6407345b-94f2-44c8-b3db-4e076be46816} 0xff 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="f55e2-115">Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f55e2-115">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="f55e2-116">Para obtener el mejor rendimiento, el archivo de registro de seguimiento debe encontrarse en un volumen que no forma parte de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="f55e2-116">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

2.  <span data-ttu-id="f55e2-117">Use el siguiente comando para detener el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="f55e2-117">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="f55e2-118">**Logman detener ASR-ETS**</span><span class="sxs-lookup"><span data-stu-id="f55e2-118">**logman stop asr -ets**</span></span>

<span data-ttu-id="f55e2-119">El archivo de registro de seguimiento es *x: \\* ASR. ETL.</span><span class="sxs-lookup"><span data-stu-id="f55e2-119">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="f55e2-120">Para obtener más información acerca de la herramienta Logman, consulte [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span><span class="sxs-lookup"><span data-stu-id="f55e2-120">For more information about the Logman tool, see [Logman](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc753820(v=ws.11)).</span></span>

## <a name="using-tracelog"></a><span data-ttu-id="f55e2-121">Usar tracelog</span><span class="sxs-lookup"><span data-stu-id="f55e2-121">Using Tracelog</span></span>

<span data-ttu-id="f55e2-122">En el procedimiento siguiente se describe cómo usar tracelog.</span><span class="sxs-lookup"><span data-stu-id="f55e2-122">The following procedure describes how to use Tracelog.</span></span>

<span data-ttu-id="f55e2-123">**Para usar tracelog**</span><span class="sxs-lookup"><span data-stu-id="f55e2-123">**To use Tracelog**</span></span>

1.  <span data-ttu-id="f55e2-124">Cree un archivo de texto denominado ASR. CTL que contenga solo el siguiente texto:</span><span class="sxs-lookup"><span data-stu-id="f55e2-124">Create a text file named asr.ctl that contains only the following text:</span></span>

    <span data-ttu-id="f55e2-125">**6407345b-94f2-44c8-b3db-4e076be46816 ASR**</span><span class="sxs-lookup"><span data-stu-id="f55e2-125">**6407345b-94f2-44c8-b3db-4e076be46816 asr**</span></span>

2.  <span data-ttu-id="f55e2-126">Use el siguiente comando para iniciar el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="f55e2-126">Use the following command to start tracing:</span></span>

    <span data-ttu-id="f55e2-127">**tracelog-Start ASR-f** *x: \\ \* \* \* ASR. ETL-GUID ASR. CTL-Flag 0xFF-LEVEL 0xFF*\*</span><span class="sxs-lookup"><span data-stu-id="f55e2-127">**tracelog -start asr -f** *x:\\*\*\*asr.etl -guid asr.ctl -flag 0xff -level 0xff*\*</span></span>

    > [!Note]  
    > <span data-ttu-id="f55e2-128">Reemplace "x: \\ " con la ruta de acceso al directorio donde desea que se almacene el archivo de registro de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f55e2-128">Replace "x:\\" with the path to the directory where you would like the trace log file to be stored.</span></span> <span data-ttu-id="f55e2-129">Para obtener el mejor rendimiento, el archivo de registro de seguimiento debe encontrarse en un volumen que no forma parte de la instantánea.</span><span class="sxs-lookup"><span data-stu-id="f55e2-129">For best performance, the trace log file should be located on a volume that is not part of the shadow copy.</span></span>

     

3.  <span data-ttu-id="f55e2-130">Use el siguiente comando para detener el seguimiento:</span><span class="sxs-lookup"><span data-stu-id="f55e2-130">Use the following command to stop tracing:</span></span>

    <span data-ttu-id="f55e2-131">**tracelog: detener ASR**</span><span class="sxs-lookup"><span data-stu-id="f55e2-131">**tracelog -stop asr**</span></span>

<span data-ttu-id="f55e2-132">El archivo de registro de seguimiento es *x: \\* ASR. ETL.</span><span class="sxs-lookup"><span data-stu-id="f55e2-132">The trace log file is *x:\\* asr.etl.</span></span>

<span data-ttu-id="f55e2-133">Para obtener más información acerca de la herramienta tracelog, consulte [tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span><span class="sxs-lookup"><span data-stu-id="f55e2-133">For more information about the Tracelog tool, see [Tracelog](https://msdn.microsoft.com/library/ms797927.aspx).</span></span>

 

 
