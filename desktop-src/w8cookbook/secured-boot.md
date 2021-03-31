---
title: Antimalware de inicio temprano
description: Antimalware de inicio temprano
ms.assetid: 4064CD44-FC50-48DE-8490-F592ED21CB7E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c3e51d7fb009ffa0e85a59990b321fb38ad196
ms.sourcegitcommit: a93d3abaf4d6d45a6f0b87faed3f576b222b1745
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "104083520"
---
# <a name="early-launch-antimalware"></a><span data-ttu-id="91cb8-103">Antimalware de inicio temprano</span><span class="sxs-lookup"><span data-stu-id="91cb8-103">Early launch antimalware</span></span>

## <a name="platforms"></a><span data-ttu-id="91cb8-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="91cb8-104">Platforms</span></span>

 <span data-ttu-id="91cb8-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="91cb8-105">**Clients** - Windows 8</span></span>  
<span data-ttu-id="91cb8-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="91cb8-106">**Servers** - Windows Server 2012</span></span>  

## <a name="description"></a><span data-ttu-id="91cb8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="91cb8-107">Description</span></span>

<span data-ttu-id="91cb8-108">A medida que el software antimalware (AM) es mejor y mejor en la detección de malware en tiempo de ejecución, los atacantes también se están volviendo mejor en la creación de rootkits que pueden ocultarse de la detección.</span><span class="sxs-lookup"><span data-stu-id="91cb8-108">As antimalware (AM) software has become better and better at detecting runtime malware, attackers are also becoming better at creating rootkits that can hide from detection.</span></span> <span data-ttu-id="91cb8-109">La detección de malware que se inicia al principio del ciclo de arranque es un desafío que la mayoría de los proveedores de AM se direccionan diligentemente.</span><span class="sxs-lookup"><span data-stu-id="91cb8-109">Detecting malware that starts early in the boot cycle is a challenge that most AM vendors address diligently.</span></span> <span data-ttu-id="91cb8-110">Normalmente, crean hackers del sistema que no son compatibles con el sistema operativo host y, en realidad, pueden poner el equipo en un estado inestable.</span><span class="sxs-lookup"><span data-stu-id="91cb8-110">Typically, they create system hacks that are not supported by the host operating system and can actually result in placing the computer in an unstable state.</span></span> <span data-ttu-id="91cb8-111">Hasta este punto, Windows no ha proporcionado una buena forma de que AM detecte y resuelva estas amenazas de arranque iniciales.</span><span class="sxs-lookup"><span data-stu-id="91cb8-111">Up to this point, Windows has not provided a good way for AM to detect and resolve these early boot threats.</span></span>

<span data-ttu-id="91cb8-112">Windows 8 presenta una nueva característica denominada arranque seguro, que protege la configuración de arranque de Windows y los componentes, y carga un controlador antimalware de inicio temprano (ELAM).</span><span class="sxs-lookup"><span data-stu-id="91cb8-112">Windows 8 introduces a new feature called Secure Boot, which protects the Windows boot configuration and components, and loads an Early Launch Anti-malware (ELAM) driver.</span></span> <span data-ttu-id="91cb8-113">Este controlador se inicia antes que otros controladores de arranque y habilita la evaluación de esos controladores y ayuda al kernel de Windows a decidir si deben inicializarse.</span><span class="sxs-lookup"><span data-stu-id="91cb8-113">This driver starts before other boot-start drivers and enables the evaluation of those drivers and helps the Windows kernel decide whether they should be initialized.</span></span>

## <a name="manifestation"></a><span data-ttu-id="91cb8-114">Manifestación</span><span class="sxs-lookup"><span data-stu-id="91cb8-114">Manifestation</span></span>

<span data-ttu-id="91cb8-115">Al iniciarse primero por el kernel, ELAM se asegura de que se inicie antes que cualquier software de terceros y, por lo tanto, puede detectar malware en el proceso de arranque e impedir que se inicialice.</span><span class="sxs-lookup"><span data-stu-id="91cb8-115">By being launched first by the kernel, ELAM is ensured to be launched before any third-party software, and is therefore able to detect malware in the boot process and prevent it from initializing.</span></span>

## <a name="mitigation"></a><span data-ttu-id="91cb8-116">Mitigación</span><span class="sxs-lookup"><span data-stu-id="91cb8-116">Mitigation</span></span>

<span data-ttu-id="91cb8-117">Los controladores de arranque se inicializan en función de la clasificación que se devuelve desde el controlador ELAM según una directiva de inicialización.</span><span class="sxs-lookup"><span data-stu-id="91cb8-117">Boot drivers are initialized based on the classification that is returned from the ELAM driver according to an initialization policy.</span></span> <span data-ttu-id="91cb8-118">De forma predeterminada, la Directiva inicializa controladores conocidos y desconocidos, pero no inicializará controladores no válidos conocidos.</span><span class="sxs-lookup"><span data-stu-id="91cb8-118">By default, the policy initializes known good and unknown drivers, but will not initialize known bad drivers.</span></span> <span data-ttu-id="91cb8-119">Un administrador del sistema puede especificar una directiva personalizada a través de directiva de grupo que puede impedir que los controladores desconocidos se inicialicen o puedan habilitar los controladores que son críticos para el proceso de arranque, pero que se han alterado, el arranque se ha modificado.</span><span class="sxs-lookup"><span data-stu-id="91cb8-119">A system administrator can specify a custom policy through Group Policy that can prevent unknown drivers from initializing or can enable drivers that are critical to the boot process, but have been tampered with, boot to be initialized.</span></span>

## <a name="solution"></a><span data-ttu-id="91cb8-120">Solución</span><span class="sxs-lookup"><span data-stu-id="91cb8-120">Solution</span></span>

<span data-ttu-id="91cb8-121">Un controlador ELAM debe registrarse para que las devoluciones de llamada de kernel obtengan información acerca de cada controlador de inicio de arranque mientras se está inicializando.</span><span class="sxs-lookup"><span data-stu-id="91cb8-121">An ELAM driver must register for kernel callbacks to get info about each boot-start driver as it is initializing.</span></span> <span data-ttu-id="91cb8-122">El controlador ELAM puede devolver una clasificación para cada controlador.</span><span class="sxs-lookup"><span data-stu-id="91cb8-122">The ELAM driver can then return a classification for each driver.</span></span> <span data-ttu-id="91cb8-123">Estas funciones son necesarias:</span><span class="sxs-lookup"><span data-stu-id="91cb8-123">These functions are required:</span></span>

-   [<span data-ttu-id="91cb8-124">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="91cb8-124">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="91cb8-125">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="91cb8-125">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)

<span data-ttu-id="91cb8-126">También se puede registrar un controlador ELAM para las devoluciones de llamada del registro.</span><span class="sxs-lookup"><span data-stu-id="91cb8-126">An ELAM driver can also register for registry callbacks.</span></span> <span data-ttu-id="91cb8-127">Al hacerlo, se habilita el controlador ELAM para inspeccionar los datos de configuración que usa cada controlador de inicio de arranque.</span><span class="sxs-lookup"><span data-stu-id="91cb8-127">Doing so enables the ELAM driver to inspect the configuration data that is used by each boot-start driver.</span></span> <span data-ttu-id="91cb8-128">El controlador ELAM puede, a continuación, bloquear o modificar los datos antes de que los usen los controladores de inicio de arranque, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="91cb8-128">The ELAM driver can then block or modify the data before it is used by the boot-start drivers, if necessary.</span></span> <span data-ttu-id="91cb8-129">Estas funciones son necesarias:</span><span class="sxs-lookup"><span data-stu-id="91cb8-129">These functions are required:</span></span>

-   [<span data-ttu-id="91cb8-130">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="91cb8-130">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="91cb8-131">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="91cb8-131">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)

<span data-ttu-id="91cb8-132">Para obtener más información sobre los requisitos del controlador de ELAM y el uso de la API, vea [antimalware de inicio temprano](/windows-hardware/drivers/install/early-launch-antimalware).</span><span class="sxs-lookup"><span data-stu-id="91cb8-132">For more details about ELAM driver requirements and API usage, see [Early Launch Antimalware](/windows-hardware/drivers/install/early-launch-antimalware).</span></span>

## <a name="tests"></a><span data-ttu-id="91cb8-133">Pruebas</span><span class="sxs-lookup"><span data-stu-id="91cb8-133">Tests</span></span>

<span data-ttu-id="91cb8-134">Los controladores de ELAM deben estar firmados especialmente por Microsoft para asegurarse de que los inicia el kernel de Windows en las primeras fases del proceso de arranque.</span><span class="sxs-lookup"><span data-stu-id="91cb8-134">ELAM drivers must be specially signed by Microsoft to ensure they are started by the Windows kernel early in the boot process.</span></span> <span data-ttu-id="91cb8-135">Para obtener la firma, los controladores de ELAM deben pasar un conjunto de pruebas de certificación para comprobar el rendimiento y el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="91cb8-135">To get the signature, ELAM drivers must pass a set of certification tests to verify performance and other behavior.</span></span> <span data-ttu-id="91cb8-136">Estas pruebas se incluyen en el kit de certificación de hardware de Windows.</span><span class="sxs-lookup"><span data-stu-id="91cb8-136">These tests are included in the Windows Hardware Certification Kit.</span></span>

## <a name="resources"></a><span data-ttu-id="91cb8-137">Recursos</span><span class="sxs-lookup"><span data-stu-id="91cb8-137">Resources</span></span>

-   [<span data-ttu-id="91cb8-138">Antimalware de inicio temprano</span><span class="sxs-lookup"><span data-stu-id="91cb8-138">Early Launch Antimalware</span></span>](/windows-hardware/drivers/install/early-launch-antimalware)
-   [<span data-ttu-id="91cb8-139">CmRegisterCallbackEx</span><span class="sxs-lookup"><span data-stu-id="91cb8-139">CmRegisterCallbackEx</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmregistercallbackex)
-   [<span data-ttu-id="91cb8-140">CmUnRegisterCallback</span><span class="sxs-lookup"><span data-stu-id="91cb8-140">CmUnRegisterCallback</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-cmunregistercallback)
-   [<span data-ttu-id="91cb8-141">IoRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="91cb8-141">IoRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-ioregisterbootdrivercallback)
-   [<span data-ttu-id="91cb8-142">IoUnRegisterBootDriverCallback</span><span class="sxs-lookup"><span data-stu-id="91cb8-142">IoUnRegisterBootDriverCallback</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-iounregisterbootdrivercallback)
-   [<span data-ttu-id="91cb8-143">Certificación de hardware con el kit de certificación de hardware de Windows presentación de la Conferencia de compilación</span><span class="sxs-lookup"><span data-stu-id="91cb8-143">Certifying hardware with the Windows Hardware Certification Kit Build Conference presentation</span></span>](https://channel9.msdn.com/events/BUILD/BUILD2011/HW-659T)
-   [<span data-ttu-id="91cb8-144">Descargar kits y herramientas</span><span class="sxs-lookup"><span data-stu-id="91cb8-144">Download Kits and Tools</span></span>](https://msdn.microsoft.com/windows/hardware/br259105)

 

 
