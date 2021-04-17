---
description: .
ms.assetid: f1ac375a-3f08-49cd-8752-6f55db24a60c
title: Montón tolerante a errores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349c8c3d6d066de3d563880c169c8dde2e062370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697781"
---
# <a name="fault-tolerant-heap"></a><span data-ttu-id="f07a8-103">Montón tolerante a errores</span><span class="sxs-lookup"><span data-stu-id="f07a8-103">Fault Tolerant Heap</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f07a8-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="f07a8-104">Affected Platforms</span></span>

<span data-ttu-id="f07a8-105">**Clientes-** Windows 7</span><span class="sxs-lookup"><span data-stu-id="f07a8-105">**Clients -** Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="f07a8-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="f07a8-106">Feature Impact</span></span>

 <span data-ttu-id="f07a8-107">**Gravedad:** Medio</span><span class="sxs-lookup"><span data-stu-id="f07a8-107">**Severity -** Medium</span></span>  
<span data-ttu-id="f07a8-108">**Frecuencia:** Habilita</span><span class="sxs-lookup"><span data-stu-id="f07a8-108">**Frequency -** Low</span></span>  


## <a name="description"></a><span data-ttu-id="f07a8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f07a8-109">Description</span></span>

<span data-ttu-id="f07a8-110">El montón tolerante a errores (FTH) es un subsistema de Windows 7 responsable de supervisar los bloqueos de la aplicación y aplicar de forma autónoma mitigaciones para evitar bloqueos futuros en cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="f07a8-110">The Fault Tolerant Heap (FTH) is a subsystem of Windows 7 responsible for monitoring application crashes and autonomously applying mitigations to prevent future crashes on a per application basis.</span></span> <span data-ttu-id="f07a8-111">Para la gran mayoría de los usuarios, FTH funcionará sin necesidad de intervención o cambio por su parte.</span><span class="sxs-lookup"><span data-stu-id="f07a8-111">For the vast majority of users, FTH will function with no need for intervention or change on their part.</span></span> <span data-ttu-id="f07a8-112">Sin embargo, en algunos casos, es posible que los desarrolladores de aplicaciones y los evaluadores de software deban invalidar el comportamiento predeterminado de este sistema.</span><span class="sxs-lookup"><span data-stu-id="f07a8-112">However, in some cases, application developers and software testers may need to override the default behavior of this system.</span></span>

## <a name="solution"></a><span data-ttu-id="f07a8-113">Solución</span><span class="sxs-lookup"><span data-stu-id="f07a8-113">Solution</span></span>

<span data-ttu-id="f07a8-114">**Ver la actividad del montón tolerante a errores**</span><span class="sxs-lookup"><span data-stu-id="f07a8-114">**Viewing Fault Tolerant Heap activity**</span></span>

<span data-ttu-id="f07a8-115">El montón de tolerancia a errores registra información cuando el servicio se inicia, detiene o inicia la mitigación de problemas de una nueva aplicación.</span><span class="sxs-lookup"><span data-stu-id="f07a8-115">Fault Tolerant Heap logs information when the service starts, stops, or starts mitigating problems for a new application.</span></span> <span data-ttu-id="f07a8-116">Para ver la información, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="f07a8-116">To view this information, follow these steps:</span></span>

1.  <span data-ttu-id="f07a8-117">Haga clic en el menú Inicio.</span><span class="sxs-lookup"><span data-stu-id="f07a8-117">Click the Start menu.</span></span>
2.  <span data-ttu-id="f07a8-118">Haga clic con el botón secundario en **equipo** y haga clic en **administrar**.</span><span class="sxs-lookup"><span data-stu-id="f07a8-118">Right-click **Computer** and click **Manage**.</span></span>
3.  <span data-ttu-id="f07a8-119">Haga clic en **visor de eventos**  >  **registros de aplicaciones y servicios**  >  **Microsoft**  >  **Windows > tolerante a errores-montón**</span><span class="sxs-lookup"><span data-stu-id="f07a8-119">Click **Event Viewer** > **Applications and Services Logs** > **Microsoft** > **Windows > Fault-Tolerant-Heap**</span></span>
4.  <span data-ttu-id="f07a8-120">Ver eventos de FTH.</span><span class="sxs-lookup"><span data-stu-id="f07a8-120">View FTH Events.</span></span>

<span data-ttu-id="f07a8-121">Los eventos de detención e inicio del servicio no contienen datos adicionales.</span><span class="sxs-lookup"><span data-stu-id="f07a8-121">The service stop and start events contain no additional data.</span></span> <span data-ttu-id="f07a8-122">El evento habilitado para FTH contiene el identificador de proceso (PID), el nombre de la imagen de proceso y la hora de inicio de la instancia de proceso.</span><span class="sxs-lookup"><span data-stu-id="f07a8-122">The FTH Enabled event contains the Process ID (PID), the process image name, and the process instance start time.</span></span>

<span data-ttu-id="f07a8-123">**Deshabilitar el montón tolerante a errores**</span><span class="sxs-lookup"><span data-stu-id="f07a8-123">**Disabling Fault Tolerant Heap**</span></span>

<span data-ttu-id="f07a8-124">**PRECAUCIÓN** Pueden producirse problemas graves si modifica incorrectamente el registro mediante el editor del registro o mediante otro método.</span><span class="sxs-lookup"><span data-stu-id="f07a8-124">**Caution** Serious problems may occur if you modify the registry incorrectly by using Registry Editor or by using another method.</span></span> <span data-ttu-id="f07a8-125">Estos problemas pueden requerir la reinstalación del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f07a8-125">These problems may require you to reinstall the operating system.</span></span> <span data-ttu-id="f07a8-126">Microsoft no brinda ninguna garantía de que se puedan solucionar estos problemas.</span><span class="sxs-lookup"><span data-stu-id="f07a8-126">Microsoft cannot guarantee that these problems can be solved.</span></span> <span data-ttu-id="f07a8-127">Modifique el registro bajo su responsabilidad.</span><span class="sxs-lookup"><span data-stu-id="f07a8-127">Modify the registry at your own risk.</span></span>  
 <span data-ttu-id="f07a8-128">Para deshabilitar completamente el montón tolerante a errores en un sistema, establezca el valor de REG \_ DWORD **HKLM \\ software \\ Microsoft \\ FTH \\ habilitado** en **0**.</span><span class="sxs-lookup"><span data-stu-id="f07a8-128">To disable Fault Tolerant Heap entirely on a system, set the REG\_DWORD value **HKLM\\Software\\Microsoft\\FTH\\Enabled** to **0**.</span></span>

<span data-ttu-id="f07a8-129">Después de cambiar este valor, reinicie el sistema.</span><span class="sxs-lookup"><span data-stu-id="f07a8-129">After changing this value, restart the system.</span></span> <span data-ttu-id="f07a8-130">FTH ya no se activará para las nuevas aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="f07a8-130">FTH will no longer activate for new applications.</span></span>

<span data-ttu-id="f07a8-131">**Restablecer la lista de aplicaciones a las que hace seguimiento FTH**</span><span class="sxs-lookup"><span data-stu-id="f07a8-131">**Resetting the list of applications tracked by FTH**</span></span>

<span data-ttu-id="f07a8-132">El montón tolerante a errores se administra automáticamente y se detiene de forma autónoma en caso de que las mitigaciones no sean eficaces para una aplicación determinada.</span><span class="sxs-lookup"><span data-stu-id="f07a8-132">Fault Tolerant heap is self-managing and will autonomously stop applying in the case that mitigations are not effective for a given application.</span></span> <span data-ttu-id="f07a8-133">Sin embargo, si necesita restablecer la lista de aplicaciones para las que FTH está mitigando problemas (por ejemplo, si está probando una aplicación y necesita reproducir un bloqueo que FTH está mitigando), puede ejecutar el siguiente comando desde un símbolo del sistema con privilegios elevados:  **Rundll32.exe fthsvc.dll, FthSysprepSpecialize**</span><span class="sxs-lookup"><span data-stu-id="f07a8-133">However, if you need to reset the list of applications for which FTH is mitigating problems (for example, if you are testing an application and need to reproduce a crash that FTH is mitigating), you can run the following command from an elevated command prompt:  **Rundll32.exe fthsvc.dll,FthSysprepSpecialize**</span></span>  
<span data-ttu-id="f07a8-134">**PRECAUCIÓN** Al ejecutar este comando, se borrarán todas las aplicaciones de FTH, por lo que las aplicaciones que actualmente funcionan correctamente pueden empezar a bloquearse de nuevo después de ejecutar este comando.</span><span class="sxs-lookup"><span data-stu-id="f07a8-134">**Caution** Running this command will clear all FTH applications, so applications that are currently functioning properly may begin to crash again after running this command.</span></span>  

 

 



