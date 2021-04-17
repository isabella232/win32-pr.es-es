---
description: .
ms.assetid: 355abd0e-928e-442e-a724-855d9dd946fc
title: Prácticas recomendadas para la eficiencia energética
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a9980d199e2d95c6dbd01c642a1f00f45e584c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697780"
---
# <a name="best-practices-for-energy-efficiency"></a><span data-ttu-id="548aa-103">Prácticas recomendadas para la eficiencia energética</span><span class="sxs-lookup"><span data-stu-id="548aa-103">Best Practices for Energy Efficiency</span></span>

## <a name="platform"></a><span data-ttu-id="548aa-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="548aa-104">Platform</span></span>

 <span data-ttu-id="548aa-105">**Clientes** : Windows XP Windows \| vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="548aa-105">**Clients** – Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="description"></a><span data-ttu-id="548aa-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="548aa-106">Description</span></span>

<span data-ttu-id="548aa-107">Los equipos portátiles basados en Windows deben cumplir con los requisitos normativos de eficiencia energética, como los del programa de Estados Unidos Energy Star de la Agencia de protección ambiental (EPA).</span><span class="sxs-lookup"><span data-stu-id="548aa-107">Windows-based laptops must meet energy efficiency regulatory requirements such as those of the United States Environmental Protection Agency (EPA) Energy Star program.</span></span> <span data-ttu-id="548aa-108">Además, las encuestas han demostrado que la mayor duración de la batería sigue siendo lo que los consumidores más desean y necesitan en los equipos portátiles.</span><span class="sxs-lookup"><span data-stu-id="548aa-108">Furthermore, surveys have shown that longer battery life continues to be what consumers most want and need in laptops.</span></span> <span data-ttu-id="548aa-109">Para satisfacer las demandas de los consumidores, los equipos portátiles de Windows deben avanzar continuamente en las áreas siguientes:</span><span class="sxs-lookup"><span data-stu-id="548aa-109">To meet consumer demands, Windows laptops must continually advance in the following areas:</span></span>

-   <span data-ttu-id="548aa-110">Eficiencia energética en todos los escenarios de uso, como inactivos, cargas de trabajo de productividad, reproducción de DVD y medios y pruebas comparativas del sector</span><span class="sxs-lookup"><span data-stu-id="548aa-110">Energy efficiency in all usage scenarios, including idle, productivity workloads, DVD and media playback, and industry benchmarks</span></span>
-   <span data-ttu-id="548aa-111">Duración de la batería del PC móvil: para plataformas de hardware y para Windows</span><span class="sxs-lookup"><span data-stu-id="548aa-111">Mobile PC battery life—for hardware platforms and for Windows</span></span>

<span data-ttu-id="548aa-112">La plataforma de Windows es muy confiable y permite un rendimiento rápido y sin interrupción.</span><span class="sxs-lookup"><span data-stu-id="548aa-112">The Windows platform is highly reliable and enables fast on-and-off performance.</span></span> <span data-ttu-id="548aa-113">Sin embargo, las extensiones proporcionadas con sistemas de PC móviles, como los servicios, las applets de la bandeja del sistema, los controladores y otro software, pueden afectar significativamente al rendimiento, la confiabilidad y la eficacia energética.</span><span class="sxs-lookup"><span data-stu-id="548aa-113">However, extensions provided with mobile PC systems, such as services, system tray applets, drivers, and other software, can significantly affect performance, reliability, and energy efficiency.</span></span>

<span data-ttu-id="548aa-114">La eficiencia energética es un problema complejo, con factores afectados por y que afectan a todos los elementos del ecosistema de PC.</span><span class="sxs-lookup"><span data-stu-id="548aa-114">Energy efficiency is a complex problem, with factors affected by and affecting all elements of the PC ecosystem.</span></span> <span data-ttu-id="548aa-115">Las pequeñas mejoras en varios escenarios pueden mejorar la eficacia de la energía, pero una sola aplicación, dispositivo o característica del sistema de bajo rendimiento puede aumentar considerablemente el consumo energético.</span><span class="sxs-lookup"><span data-stu-id="548aa-115">Small enhancements across multiple scenarios can improve energy efficiency, but a single poorly performing application, device, or system feature can increase energy consumption significantly.</span></span>

<span data-ttu-id="548aa-116">El hardware y los dispositivos constituyen la base de la eficacia energética.</span><span class="sxs-lookup"><span data-stu-id="548aa-116">Hardware and devices form the foundation for energy efficiency.</span></span> <span data-ttu-id="548aa-117">Sin embargo, el software de aplicación y servicio también debe ser eficaz para permitir que el sistema alcance la duración óptima de la batería.</span><span class="sxs-lookup"><span data-stu-id="548aa-117">However, application and service software must also be efficient to allow the system to achieve optimal battery life.</span></span> <span data-ttu-id="548aa-118">Cada componente de software del sistema, incluido el sistema operativo y las aplicaciones y servicios de valor agregado, debe cumplir las directrices básicas de eficiencia.</span><span class="sxs-lookup"><span data-stu-id="548aa-118">Each software component on the system, including the operating system and value-added applications and services, must conform to basic efficiency guidelines.</span></span> <span data-ttu-id="548aa-119">Una sola aplicación o servicio con un comportamiento incorrecto puede eliminar cualquier mejora de la eficacia energética que el procesador, los dispositivos o el hardware de la plataforma más recientes alcanzaron.</span><span class="sxs-lookup"><span data-stu-id="548aa-119">A single misbehaving application or service can eliminate any energy efficiency gains that the latest processor, devices, or platform hardware achieved.</span></span> <span data-ttu-id="548aa-120">Para obtener información más detallada acerca de la duración de la batería y la eficiencia energética, consulte la [Guía de soluciones](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)de batería.</span><span class="sxs-lookup"><span data-stu-id="548aa-120">For more detailed information regarding battery life and energy efficiency please refer to the [Battery Life Solutions Guide](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#).</span></span>

<span data-ttu-id="548aa-121">Los principales problemas y componentes que afectan a la duración de la batería en un PC móvil son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="548aa-121">The principle issues and components that affect battery life in a mobile PC are:</span></span>

<span data-ttu-id="548aa-122">**Características de la batería**</span><span class="sxs-lookup"><span data-stu-id="548aa-122">**Battery Characteristics**</span></span>

-   <span data-ttu-id="548aa-123">El tamaño, el tipo y la calidad de la capacidad de la batería afectan a la duración de la batería</span><span class="sxs-lookup"><span data-stu-id="548aa-123">Size, type, and quality of battery capacity affect battery life</span></span>
-   <span data-ttu-id="548aa-124">Cuanto mayor sea la batería, mayor será la fuente de alimentación.</span><span class="sxs-lookup"><span data-stu-id="548aa-124">The larger the battery, the greater the power supply</span></span>
-   <span data-ttu-id="548aa-125">Las baterías mayores son más caras y más pesadas. los usuarios prefieren sistemas más claros</span><span class="sxs-lookup"><span data-stu-id="548aa-125">Larger batteries are more expensive and heavier; users prefer lighter systems</span></span>

<span data-ttu-id="548aa-126">**Componentes de hardware**</span><span class="sxs-lookup"><span data-stu-id="548aa-126">**Hardware Components**</span></span>

-   <span data-ttu-id="548aa-127">Frecuencia y profundidad en las que el hardware puede entrar en Estados de energía inferiores</span><span class="sxs-lookup"><span data-stu-id="548aa-127">Frequency and depth to which hardware can enter lower power states</span></span>
-   <span data-ttu-id="548aa-128">Compatibilidad de hardware con Estados de energía inferiores</span><span class="sxs-lookup"><span data-stu-id="548aa-128">Hardware support of lower power states</span></span>
-   <span data-ttu-id="548aa-129">Optimización del controlador para la eficiencia energética</span><span class="sxs-lookup"><span data-stu-id="548aa-129">Driver optimization for energy efficiency</span></span>

<span data-ttu-id="548aa-130">**Sistema operativo: administración de energía dirigida**</span><span class="sxs-lookup"><span data-stu-id="548aa-130">**Operating System–Directed Power Management**</span></span>

-   <span data-ttu-id="548aa-131">Eficiencia del código de Windows en lugar de una carga frente a mientras está inactivo</span><span class="sxs-lookup"><span data-stu-id="548aa-131">Efficiency of Windows code while under a load versus while idle</span></span>
-   <span data-ttu-id="548aa-132">Nivel de cooperación de todos los componentes con la administración de energía dirigida a Windows</span><span class="sxs-lookup"><span data-stu-id="548aa-132">Cooperation level of all components with Windows-directed power management</span></span>
-   <span data-ttu-id="548aa-133">Configuración adecuada del sistema operativo para optimizar la administración de energía mediante la configuración de la Directiva de energía</span><span class="sxs-lookup"><span data-stu-id="548aa-133">Proper configuration of the operating system to optimize for power management through power policy settings</span></span>

<span data-ttu-id="548aa-134">**Software y servicios de aplicaciones**</span><span class="sxs-lookup"><span data-stu-id="548aa-134">**Application Software and Services**</span></span>

-   <span data-ttu-id="548aa-135">Eficacia de las aplicaciones, los controladores y los servicios mientras se encuentran en una carga frente a mientras están inactivos</span><span class="sxs-lookup"><span data-stu-id="548aa-135">Efficiency of applications, drivers, and services while under a load versus while idle</span></span>
-   <span data-ttu-id="548aa-136">Nivel de cooperación de las aplicaciones con la administración de energía dirigida a Windows</span><span class="sxs-lookup"><span data-stu-id="548aa-136">Cooperation level of applications with Windows–directed power management</span></span>
-   <span data-ttu-id="548aa-137">Asignación de software del sistema o de los dispositivos para entrar en Estados inactivos de baja energía</span><span class="sxs-lookup"><span data-stu-id="548aa-137">Software allowance of the system or devices to enter into low-power idle states</span></span>

<span data-ttu-id="548aa-138">Un único componente de aplicación o servicio puede impedir que un sistema presente una duración óptima de la batería.</span><span class="sxs-lookup"><span data-stu-id="548aa-138">A single application or service component can prevent a system from realizing optimal battery life.</span></span> <span data-ttu-id="548aa-139">Aunque Windows proporciona muchas opciones de configuración de energía, el software preinstalado o la configuración de la Directiva de energía en muchos sistemas no están optimizados para la plataforma de hardware del host.</span><span class="sxs-lookup"><span data-stu-id="548aa-139">Although Windows provides many power configuration options, preinstalled software or power policy settings on many systems are not optimized for the host hardware platform.</span></span>

<span data-ttu-id="548aa-140">Un método común para evaluar el impacto en la batería del software preinstalado es comparar el consumo de energía del sistema con una instalación limpia de Windows frente a una instalación de Windows que incluye software y servicios de valor añadido.</span><span class="sxs-lookup"><span data-stu-id="548aa-140">A common method for evaluating the battery-life impact of preinstalled software is to compare the power consumption of the system with a clean installation of Windows versus a Windows installation that includes value-added software and services.</span></span> <span data-ttu-id="548aa-141">Aunque una instalación limpia no representa la plataforma típica que los OEM envían a los clientes, la comparación del consumo de energía puede proporcionar información sobre la eficacia energética del software preinstalado.</span><span class="sxs-lookup"><span data-stu-id="548aa-141">Although a clean installation does not represent the typical platform that OEMs ship to customers, the power consumption comparison can provide insight into the energy-efficiency of preinstalled software.</span></span>

## <a name="best-practices"></a><span data-ttu-id="548aa-142">Prácticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="548aa-142">Best Practices</span></span>

<span data-ttu-id="548aa-143">Para asegurarse de que la aplicación está optimizada en las plataformas de Windows, siga estas prácticas recomendadas al diseñar aplicaciones o servicios:</span><span class="sxs-lookup"><span data-stu-id="548aa-143">To ensure that your application is optimized on Windows platforms, follow these best practices when you design applications or services:</span></span>

-   <span data-ttu-id="548aa-144">**Evitar el uso de temporizadores periódicos de alta resolución**</span><span class="sxs-lookup"><span data-stu-id="548aa-144">**Avoid use of high-resolution periodic timers**</span></span>

<dl> <span data-ttu-id="548aa-145">Usar temporizadores periódicos de alta resolución (</span><span class="sxs-lookup"><span data-stu-id="548aa-145">Using high-resolution periodic timers (</span></span><10 ms) reduces the efficiency of processor power-management technologies.  
</dl>

-   <span data-ttu-id="548aa-146">**Invertir en optimizaciones de rendimiento**</span><span class="sxs-lookup"><span data-stu-id="548aa-146">**Invest in performance optimizations**</span></span>

<dl> <span data-ttu-id="548aa-147">Cada optimización de rendimiento es una optimización de la duración de la batería.</span><span class="sxs-lookup"><span data-stu-id="548aa-147">Every performance optimization is a battery life optimization.</span></span> <span data-ttu-id="548aa-148">Las reducciones en los recursos necesarios, como el uso de menos tiempo de procesador o el procesamiento por lotes o las lecturas de disco de agrupación en clústeres, permiten que el hardware del sistema se vuelva inactivo y escriba modos de baja energía.</span><span class="sxs-lookup"><span data-stu-id="548aa-148">Reductions in required resources, such as using less processor time or batching/clustering disk reads, allow system hardware to become idle and enter low-power modes.</span></span>  
</dl>

-   <span data-ttu-id="548aa-149">**Ajustar a la Directiva de energía de usuario**</span><span class="sxs-lookup"><span data-stu-id="548aa-149">**Adjust to user power policy**</span></span>

<dl> <span data-ttu-id="548aa-150">Windows Vista y versiones posteriores facilitan al usuario la elección del ahorro de energía general o el comportamiento del rendimiento del sistema.</span><span class="sxs-lookup"><span data-stu-id="548aa-150">Windows Vista and later make it easy for the user to choose the overall power-savings or performance behavior of the system.</span></span> <span data-ttu-id="548aa-151">La aplicación debe responder a los cambios en la Directiva de energía y reducir el uso de recursos o aumentar el rendimiento en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="548aa-151">Your application should respond to changes in power policy and reduce resource usage or increase performance accordingly.</span></span> <span data-ttu-id="548aa-152">Por ejemplo, una aplicación debe deshabilitar la actividad en segundo plano como la indexación o el análisis del sistema cuando el usuario ha seleccionado un plan de energía de ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="548aa-152">For example, an application should disable background activity such as indexing or system scanning when the user has selected a Power Saver power plan.</span></span>  
</dl>

-   <span data-ttu-id="548aa-153">**Reducir el uso de recursos cuando el sistema tiene energía de batería**</span><span class="sxs-lookup"><span data-stu-id="548aa-153">**Reduce resource usage when the system is on battery power**</span></span>

<dl> <span data-ttu-id="548aa-154">La aplicación debe reducir el uso de recursos, como la frecuencia de actualización en segundo plano, cuando el sistema tiene energía de batería.</span><span class="sxs-lookup"><span data-stu-id="548aa-154">Your application should reduce its resource usage - such as background update frequency - when the system is on battery power.</span></span>  
</dl>

-   <span data-ttu-id="548aa-155">**No representar en la pantalla cuando está desactivada**</span><span class="sxs-lookup"><span data-stu-id="548aa-155">**Do not render to the display when it is off**</span></span>

<dl> <span data-ttu-id="548aa-156">La pantalla del sistema podría estar desactivada para el ahorro de energía.</span><span class="sxs-lookup"><span data-stu-id="548aa-156">The system display might be off for power savings.</span></span> <span data-ttu-id="548aa-157">La aplicación no debe llevar a cabo una representación de gráficos innecesaria cuando la pantalla está desactivada, ya que esto desperdicia recursos del sistema y energía.</span><span class="sxs-lookup"><span data-stu-id="548aa-157">Your application should not perform unnecessary graphics rendering when the display is off because this wastes system resources and power.</span></span>  
</dl>

-   <span data-ttu-id="548aa-158">**Evite el sondeo y el giro en bucles estrechos**</span><span class="sxs-lookup"><span data-stu-id="548aa-158">**Avoid polling and spinning in tight loops**</span></span>

<dl> <span data-ttu-id="548aa-159">El uso intensivo del procesador reduce la eficacia de las tecnologías de administración de energía del procesador, como Estados inactivos del procesador y Estados de rendimiento del procesador.</span><span class="sxs-lookup"><span data-stu-id="548aa-159">Heavy processor usage reduces the effectiveness of processor power-management technologies such as processor idle states and processor performance states.</span></span>  
</dl>

-   <span data-ttu-id="548aa-160">**No evitar que el sistema desactive la pantalla o el ralentí en suspensión**</span><span class="sxs-lookup"><span data-stu-id="548aa-160">**Do not prevent the system from turning off the display or idling to sleep**</span></span>

<dl> <span data-ttu-id="548aa-161">La aplicación debe hacer solicitudes de energía sensatas con la API de SetThreadExecutionState.</span><span class="sxs-lookup"><span data-stu-id="548aa-161">Your application should make judicious power requests with the SetThreadExecutionState API.</span></span> <span data-ttu-id="548aa-162">El sistema debe realizar estas solicitudes solo cuando las operaciones críticas deben retrasar el apagado del sistema o entrar en suspensión automáticamente.</span><span class="sxs-lookup"><span data-stu-id="548aa-162">The system should make these requests only when critical operations must delay the system from powering off the display or automatically entering sleep.</span></span>  
</dl>

-   <span data-ttu-id="548aa-163">**Respuesta a eventos comunes de administración de energía**</span><span class="sxs-lookup"><span data-stu-id="548aa-163">**Respond to common power-management events**</span></span>

<dl> <span data-ttu-id="548aa-164">La aplicación debe registrarse y responder a los eventos comunes de administración de energía, como los cambios de origen de alimentación del sistema y las notificaciones de encendido y apagado de la pantalla.</span><span class="sxs-lookup"><span data-stu-id="548aa-164">Your application should register for and respond to common power-management events, such as system power-source changes and power-on and power-off notifications for the display.</span></span>  
</dl>

-   <span data-ttu-id="548aa-165">**No habilite el registro de depuración de forma predeterminada; usar el seguimiento de eventos para Windows en su lugar**</span><span class="sxs-lookup"><span data-stu-id="548aa-165">**Do not enable debug logging by default; use Event Tracing for Windows instead**</span></span>

<dl> <span data-ttu-id="548aa-166">El registro de depuración periódico puede impedir la desactivación del disco.</span><span class="sxs-lookup"><span data-stu-id="548aa-166">Periodic debug logging can prevent disk spin-down.</span></span>  
</dl>

## <a name="links-to-other-resources"></a><span data-ttu-id="548aa-167">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="548aa-167">Links to Other Resources</span></span>

-   [<span data-ttu-id="548aa-168">Guía de soluciones de batería</span><span class="sxs-lookup"><span data-stu-id="548aa-168">Battery Life Solutions Guide</span></span>](https://docs.microsoft.com/windows-hardware/design/component-guidelines/battery-and-charging#)
-   [<span data-ttu-id="548aa-169">Portal de eficiencia energética</span><span class="sxs-lookup"><span data-stu-id="548aa-169">Energy Efficiency Portal</span></span>](https://www.microsoft.com/whdc/system/pnppwr/mobilepwr.mspx)
-   [<span data-ttu-id="548aa-170">Kit de herramientas de rendimiento de Windows</span><span class="sxs-lookup"><span data-stu-id="548aa-170">Windows Performance Toolkit</span></span>](https://www.microsoft.com/whdc/system/sysperf/perftools.mspx)

 

 



