---
description: Montón tolerante a errores
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Montón tolerante a errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17ab2630e6dc28cb84604e48be1aa60bf208a97
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088403"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="084ea-103">Montón tolerante a errores</span><span class="sxs-lookup"><span data-stu-id="084ea-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="084ea-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="084ea-104">Affected Platforms</span></span>

<span data-ttu-id="084ea-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="084ea-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="084ea-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="084ea-106">Feature Impact</span></span>

 <span data-ttu-id="084ea-107">**Gravedad:** Medio</span><span class="sxs-lookup"><span data-stu-id="084ea-107">**Severity -** Medium</span></span>  
<span data-ttu-id="084ea-108">**Frecuencia:** Bajo</span><span class="sxs-lookup"><span data-stu-id="084ea-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="084ea-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="084ea-109">Description</span></span>

<span data-ttu-id="084ea-110">El montón tolerante a errores (FTH) es un subsistema de Windows 7 responsable de supervisar los bloqueos de aplicaciones y aplicar de forma autónoma mitigaciones para evitar futuros bloqueos por aplicación.</span><span class="sxs-lookup"><span data-stu-id="084ea-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="084ea-111">Para la gran mayoría de los usuarios, FTH funcionará sin necesidad de intervención ni cambio por su parte.</span><span class="sxs-lookup"><span data-stu-id="084ea-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="084ea-112">Sin embargo, en algunos casos, es posible que los desarrolladores de aplicaciones y evaluadores de software necesiten invalidar el comportamiento predeterminado de este sistema.</span><span class="sxs-lookup"><span data-stu-id="084ea-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="084ea-113">Solución</span><span class="sxs-lookup"><span data-stu-id="084ea-113">Solution</span></span>

<span data-ttu-id="084ea-114">**Visualización de la actividad del montón tolerante a errores**</span><span class="sxs-lookup"><span data-stu-id="084ea-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="084ea-115">El montón tolerante a errores registra información cuando el servicio se inicia, detiene o inicia la mitigación de problemas de una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="084ea-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="084ea-116">Para ver la información, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="084ea-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="084ea-117">Haga clic en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="084ea-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="084ea-118">Haga clic con el botón **derecho en Equipo** y haga clic en **Administrar.**</span><span class="sxs-lookup"><span data-stu-id="084ea-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="084ea-119">Haga **clic Visor de eventos** registros de aplicaciones y  >  **servicios** de  >  **Microsoft** Windows > montón  >  **tolerante a errores**</span><span class="sxs-lookup"><span data-stu-id="084ea-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="084ea-120">Ver eventos FTH.</span><span class="sxs-lookup"><span data-stu-id="084ea-120">View FTH Events.</span></span>

<span data-ttu-id="084ea-121">Los eventos de detención e inicio del servicio no contienen datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="084ea-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="084ea-122">El evento FTH Enabled contiene el identificador de proceso (PID), el nombre de la imagen de proceso y la hora de inicio de la instancia de proceso.</span><span class="sxs-lookup"><span data-stu-id="084ea-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="084ea-123">**Deshabilitar el montón tolerante a errores**</span><span class="sxs-lookup"><span data-stu-id="084ea-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="084ea-124">**Precaución** Pueden producirse problemas graves si modifica incorrectamente el Registro mediante el Editor del Registro o mediante otro método.</span><span class="sxs-lookup"><span data-stu-id="084ea-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="084ea-125">Estos problemas pueden requerir que vuelva a instalar el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="084ea-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="084ea-126">Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas.</span><span class="sxs-lookup"><span data-stu-id="084ea-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="084ea-127">Modifique el registro bajo su responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="084ea-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="084ea-128">Para deshabilitar el montón tolerante a errores completamente en un sistema, establezca el valor REG \_ DWORD **HKLM \\ Software Microsoft \\ \\ FTH \\ Enabled** en **0**.</span><span class="sxs-lookup"><span data-stu-id="084ea-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="084ea-129">Después de cambiar este valor, reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="084ea-129">After changing this value, restart the system.</span></span> <span data-ttu-id="084ea-130">FTH ya no se activará para las nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="084ea-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="084ea-131">**Restablecer la lista de aplicaciones de las que realiza un seguimiento FTH**</span><span class="sxs-lookup"><span data-stu-id="084ea-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="084ea-132">El montón tolerante a errores se administra automáticamente y dejará de aplicarse de forma autónoma en caso de que las mitigaciones no sean eficaces para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="084ea-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="084ea-133">Sin embargo, si necesita restablecer la lista de aplicaciones para las que FTH está mitigando problemas (por ejemplo, si está probando una aplicación y necesita reproducir un bloqueo que FTH está mitigando), puede ejecutar el siguiente comando desde un símbolo del sistema con privilegios elevados:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="084ea-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="084ea-134">**Precaución** Al ejecutar este comando se borrarán todas las aplicaciones FTH, por lo que las aplicaciones que funcionan correctamente pueden empezar a bloquearse de nuevo después de ejecutar este comando.</span><span class="sxs-lookup"><span data-stu-id="084ea-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



