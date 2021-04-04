---
title: Aplicaciones de inicio
description: Aplicaciones de inicio
ms.assetid: 3519CB52-A6EC-4819-87FE-C144801BDD9F
keywords:
- aplicación de inicio
- Tarea en segundo plano
- Tecla ejecutar
- RunOnce
- carpeta de inicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a12f01dac073712512206a5c432561b4a0b75e
ms.sourcegitcommit: 46376be61d3fa308f9b1a06d7e2fa122a39755af
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2020
ms.locfileid: "103797122"
---
# <a name="startup-apps"></a><span data-ttu-id="4545c-108">Aplicaciones de inicio</span><span class="sxs-lookup"><span data-stu-id="4545c-108">Startup apps</span></span>

## <a name="platform"></a><span data-ttu-id="4545c-109">Plataforma</span><span class="sxs-lookup"><span data-stu-id="4545c-109">Platform</span></span>

<span data-ttu-id="4545c-110">**Clientes**   de   Windows 8</span><span class="sxs-lookup"><span data-stu-id="4545c-110">**Clients**   Windows 8</span></span>  


## <a name="description"></a><span data-ttu-id="4545c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="4545c-111">Description</span></span>

<span data-ttu-id="4545c-112">Una de las grandes e///////////////////////////////////////////</span><span class="sxs-lookup"><span data-stu-id="4545c-112">One of the big bets with Windows is the ability to light up various form factors, from the traditional desktops and laptops to low-powered tablets.</span></span> <span data-ttu-id="4545c-113">Para asegurarse de que nuestros clientes mutuos tengan una gran experiencia en cualquier factor de forma que elijan con Windows, dos métricas de éxito clave que deben abordarse son una mayor duración de la batería y una excelente capacidad de respuesta del equipo.</span><span class="sxs-lookup"><span data-stu-id="4545c-113">To ensure that our mutual customers have a great experience on any form factor they choose with Windows, two key success metrics that need to be addressed are increased battery life and excellent PC responsiveness.</span></span> <span data-ttu-id="4545c-114">Para lograrlo, se han realizado mejoras en varias áreas de Windows, como el ciclo de vida de proceso, los Estados de suspensión y las aplicaciones de inicio (aplicaciones con inicio automatizado después del arranque de la máquina).</span><span class="sxs-lookup"><span data-stu-id="4545c-114">In order to achieve these, improvements have been made in multiple areas of Windows including process life cycle, sleep states and startup apps (apps with automated launch after machine boot).</span></span> <span data-ttu-id="4545c-115">En este tema se resaltan algunos de los impactos que tienen las aplicaciones de inicio en un dispositivo Windows y se proporciona orientación a los desarrolladores (ISV/IHV) y los OEM para que reconsideren los patrones de uso de las aplicaciones de inicio con el fin de mejorar la duración de la batería y la capacidad de respuesta de nuestros clientes mutuos.</span><span class="sxs-lookup"><span data-stu-id="4545c-115">This topic highlights some of the impacts that startup apps have on a Windows device, and provides guidance to developers (ISV/IHV) and OEMs to rethink the usage patterns of startup apps in order to improve battery life and responsiveness for our mutual customers.</span></span> <span data-ttu-id="4545c-116">También describe los cambios en Windows que ponen a los usuarios en el control de cómo determinar qué aplicaciones de inicio realmente se ejecutan.</span><span class="sxs-lookup"><span data-stu-id="4545c-116">It also describes the changes in Windows that put users in control of determining which of the startup apps actually get to execute.</span></span>

<span data-ttu-id="4545c-117">Las aplicaciones de la tienda Windows están diseñadas para cumplir con los nuevos estándares de consumo de la batería y capacidad de respuesta, y Windows administra su ciclo de vida mediante su suspensión o terminación.</span><span class="sxs-lookup"><span data-stu-id="4545c-117">Windows Store apps are designed to adhere to new standards of battery consumption and responsiveness, and Windows manages their life cycle by suspending and/or terminating them.</span></span> <span data-ttu-id="4545c-118">Sin embargo, las aplicaciones de escritorio diseñadas para versiones anteriores de Windows no se han diseñado necesariamente para conservar la duración de la batería o son sensibles a la actividad del usuario, y pueden afectar a la capacidad de respuesta del sistema (por ejemplo, cuando una aplicación envía un latido de 1 segundo normal para comprobar si hay actualizaciones, o preasigna la memoria por delante en caso de que la necesite).</span><span class="sxs-lookup"><span data-stu-id="4545c-118">However, desktop apps designed for prior Windows versions have not necessarily been designed to preserve battery life or be sensitive to user activity, and can affect system responsiveness (for example, when an app sends a regular 1-second heartbeat to check for updates, or pre-allocates memory upfront in case it needs it later).</span></span> <span data-ttu-id="4545c-119">Esto puede crear una experiencia deficiente para el usuario que adquiere un equipo con Windows Tablet PC con una larga esperanza de duración de la batería y semanas de espera, pero detecta la duración de la batería de Tablet PC no logra estos objetivos.</span><span class="sxs-lookup"><span data-stu-id="4545c-119">This can create a poor experience for the user who buys a Windows tablet PC with a long battery life expectancy and weeks of standby, but discovers the tablet s battery life does not achieve these goals.</span></span> <span data-ttu-id="4545c-120">Además, dado que las aplicaciones de inicio se ejecutan en segundo plano, el número de aplicaciones que se ejecutan en el sistema puede ser mucho mayor de lo que el usuario es consciente y que afecta a la capacidad de respuesta del sistema.</span><span class="sxs-lookup"><span data-stu-id="4545c-120">Also, since startup apps run in the background, the number of apps running on the system can be significantly more than what the user is aware of and affect system responsiveness.</span></span> <span data-ttu-id="4545c-121">Las aplicaciones de inicio se clasifican para incluir las que aprovechan estos mecanismos para iniciarse:</span><span class="sxs-lookup"><span data-stu-id="4545c-121">Startup apps are classified to include those leveraging these mechanisms to start:</span></span>

-   <span data-ttu-id="4545c-122">Ejecutar claves del registro (nodos HKLM, HKCU, WOW64 incluidos)</span><span class="sxs-lookup"><span data-stu-id="4545c-122">Run registry keys (HKLM, HKCU, wow64 nodes included)</span></span>
-   <span data-ttu-id="4545c-123">Claves del registro de RunOnce</span><span class="sxs-lookup"><span data-stu-id="4545c-123">RunOnce registry keys</span></span>
-   <span data-ttu-id="4545c-124">Carpetas de inicio en el menú Inicio para cada usuario y ubicación pública</span><span class="sxs-lookup"><span data-stu-id="4545c-124">Startup folders under the start menu for per user and public locations</span></span>

<span data-ttu-id="4545c-125">Se ha agregado una nueva funcionalidad a Windows para garantizar que los usuarios finales siempre controlen las aplicaciones que se ejecutan en sus sistemas.</span><span class="sxs-lookup"><span data-stu-id="4545c-125">New functionality has been added to Windows to ensure that end users are always in control of the apps that run on their systems.</span></span> <span data-ttu-id="4545c-126">En la pestaña Inicio del administrador de tareas se muestra una lista de aplicaciones de inicio, junto con controles que permiten a los usuarios deshabilitar las aplicaciones de inicio.</span><span class="sxs-lookup"><span data-stu-id="4545c-126">The Startup tab in Task Manager shows a list of startup apps, along with controls that allow users to disable startup apps.</span></span> <span data-ttu-id="4545c-127">Para ayudar a los usuarios a determinar qué deshabilitar, el administrador de tareas muestra una medida de cada impacto de la aplicación de inicio.</span><span class="sxs-lookup"><span data-stu-id="4545c-127">To help users determine what to disable, Task Manager displays a measure of each startup app s impact.</span></span> <span data-ttu-id="4545c-128">El impacto se calcula en función del uso de la CPU y del disco de la aplicación en el inicio.</span><span class="sxs-lookup"><span data-stu-id="4545c-128">Impact is assessed based on an app s CPU and disk usage at startup.</span></span> <span data-ttu-id="4545c-129">Los valores de impacto se determinan aplicando estos criterios:</span><span class="sxs-lookup"><span data-stu-id="4545c-129">Impact values are determined by applying these criteria:</span></span>

-   <span data-ttu-id="4545c-130">**Gran impacto**   Aplicaciones que usan más de un segundo de tiempo de CPU o más de 3 MB de e/s de disco en el inicio</span><span class="sxs-lookup"><span data-stu-id="4545c-130">**High impact**   Apps that use more than 1 second of CPU time or more than 3 MB of disk I/O at startup</span></span>
-   <span data-ttu-id="4545c-131">**Impacto medio**   Aplicaciones que usan 300 ms-1000 ms de tiempo de CPU o 300 KB-3 MB de e/s de disco</span><span class="sxs-lookup"><span data-stu-id="4545c-131">**Medium impact**   Apps that use 300 ms - 1000 ms of CPU time or 300 KB - 3 MB of disk I/O</span></span>
-   <span data-ttu-id="4545c-132">**Impacto bajo**   Aplicaciones que usan menos de 300 ms de tiempo de CPU y menos de 300 KB de e/s de disco</span><span class="sxs-lookup"><span data-stu-id="4545c-132">**Low impact**   Apps that use less than 300 ms of CPU time and less than 300 KB of disk I/O</span></span>

<span data-ttu-id="4545c-133">Microsoft proporciona herramientas para ayudar a los desarrolladores de aplicaciones a evaluar, analizar y tomar medidas para reducir su impacto en el inicio y mejorar la experiencia del usuario.</span><span class="sxs-lookup"><span data-stu-id="4545c-133">Microsoft provides tools to help app developers assess, analyze and take steps to reduce their startup impact and improve the user experience.</span></span> <span data-ttu-id="4545c-134">El kit de evaluación e implementación proporciona la capacidad de ejecutar una evaluación del rendimiento de arranque y medir el impacto de las aplicaciones que se ejecutan en el inicio.</span><span class="sxs-lookup"><span data-stu-id="4545c-134">The Assessment and Deployment Kit provides the ability to run a boot performance assessment and measure the impact of apps that run at startup.</span></span> <span data-ttu-id="4545c-135">Los resultados de la evaluación contienen análisis detallados e información de corrección, si procede, para los componentes de mayor impacto en el inicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="4545c-135">The assessment results contain detailed analysis and remediation info where applicable, for the top-impacting components at Windows startup.</span></span> <span data-ttu-id="4545c-136">Con el analizador de rendimiento de Windows, los desarrolladores de aplicaciones pueden realizar análisis profundos para encontrar la causa raíz del impacto en el rendimiento y mejorar el rendimiento de inicio de Windows.</span><span class="sxs-lookup"><span data-stu-id="4545c-136">Using the Windows Performance Analyzer, app developers can perform deep analysis to find the root cause of the performance impact and improve Windows startup performance.</span></span> <span data-ttu-id="4545c-137">Instale Windows ADK desde [aquí](/previous-versions/windows/hh825494(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="4545c-137">Install the Windows ADK from [here](/previous-versions/windows/hh825494(v=win.10)).</span></span>

## <a name="guidance"></a><span data-ttu-id="4545c-138">Instrucciones</span><span class="sxs-lookup"><span data-stu-id="4545c-138">Guidance</span></span>

<span data-ttu-id="4545c-139">Las aplicaciones de inicio abarcan varias categorías, como se describe en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="4545c-139">Startup apps span multiple categories as described in the table below.</span></span> <span data-ttu-id="4545c-140">Un conjunto de recomendaciones para desarrolladores se asigna a las categorías de aplicaciones de inicio para que se alineen con los cambios funcionales de Windows descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4545c-140">A set of recommendations for developers is mapped to the categories of startup apps to align with the Windows functional changes described above.</span></span>



<span data-ttu-id="4545c-141">Categorías de aplicaciones de inicio</span><span class="sxs-lookup"><span data-stu-id="4545c-141">Startup Apps Categories</span></span>

<span data-ttu-id="4545c-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="4545c-142">Description</span></span>

<span data-ttu-id="4545c-143">Recomendación</span><span class="sxs-lookup"><span data-stu-id="4545c-143">Recommendation</span></span>

<span data-ttu-id="4545c-144">**Actualizadores**</span><span class="sxs-lookup"><span data-stu-id="4545c-144">**Updaters**</span></span>

<span data-ttu-id="4545c-145">Supervisar y actualizar usuarios para actualizaciones en línea</span><span class="sxs-lookup"><span data-stu-id="4545c-145">Monitor and update users for online updates</span></span>

<span data-ttu-id="4545c-146">**Tarea de mantenimiento**</span><span class="sxs-lookup"><span data-stu-id="4545c-146">**Maintenance Task**</span></span>

> [!Note]  
> <span data-ttu-id="4545c-147">Todas las actualizaciones deben ser tareas de mantenimiento, sin requisitos de interacción con la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="4545c-147">All updates should be maintenance tasks, without any UI interaction requirements.</span></span> <span data-ttu-id="4545c-148">Las aplicaciones solo deben actualizarse de modo silencioso y revertir en caso de error</span><span class="sxs-lookup"><span data-stu-id="4545c-148">Apps should just update themselves quietly, and rollback on failure</span></span>

<br/>

<span data-ttu-id="4545c-149">$ {ROWSPAN2} $**asistencia de hardware**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4545c-149">${ROWSPAN2}$**Hardware Assistance**${REMOVE}$</span></span>  

<span data-ttu-id="4545c-150">Puntos de acceso alternativos</span><span class="sxs-lookup"><span data-stu-id="4545c-150">Alternative Access Points</span></span>

<span data-ttu-id="4545c-151">Proporcionar acceso a las características y aplicaciones de Windows a las que se puede acceder a través de otros puntos de acceso de Windows</span><span class="sxs-lookup"><span data-stu-id="4545c-151">Provide access to Windows features and apps that are accessible via other access points in Windows</span></span>

<span data-ttu-id="4545c-152">**Remove**</span><span class="sxs-lookup"><span data-stu-id="4545c-152">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="4545c-153">La clave consiste en reducir las características duplicadas que existen en Windows</span><span class="sxs-lookup"><span data-stu-id="4545c-153">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="4545c-154">Notificadores</span><span class="sxs-lookup"><span data-stu-id="4545c-154">Notifiers</span></span>

<span data-ttu-id="4545c-155">Proporcionar a los usuarios notificaciones acerca de sus dispositivos</span><span class="sxs-lookup"><span data-stu-id="4545c-155">Provide users with notifications regarding their devices</span></span>

<span data-ttu-id="4545c-156">**Remove**</span><span class="sxs-lookup"><span data-stu-id="4545c-156">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="4545c-157">Windows proporciona notificaciones a los usuarios acerca de sus dispositivos</span><span class="sxs-lookup"><span data-stu-id="4545c-157">Windows provides notifications to users about their devices</span></span>

<br/>

<span data-ttu-id="4545c-158">**Iniciadores previos**</span><span class="sxs-lookup"><span data-stu-id="4545c-158">**Pre-launchers**</span></span>

<span data-ttu-id="4545c-159">Algunas de las actividades preliminares necesarias para las aplicaciones se descargan en una aplicación de inicio durante el inicio de sesión del usuario</span><span class="sxs-lookup"><span data-stu-id="4545c-159">Some of preliminary activities needed by apps is offloaded to a startup app during user login</span></span>

<span data-ttu-id="4545c-160">**Remove**</span><span class="sxs-lookup"><span data-stu-id="4545c-160">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="4545c-161">Windows 8 está optimizado para una experiencia rápida para los lanzamientos de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="4545c-161">Windows 8 is optimized for a fast experience for app launches.</span></span>

<br/>

<span data-ttu-id="4545c-162">$ {ROWSPAN4} $**utilidad**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4545c-162">${ROWSPAN4}$**Utility**${REMOVE}$</span></span>  

<span data-ttu-id="4545c-163">Sincronización de PC</span><span class="sxs-lookup"><span data-stu-id="4545c-163">PC Sync</span></span>

<span data-ttu-id="4545c-164">Proporcionar funcionalidad de sincronización en varios sistemas</span><span class="sxs-lookup"><span data-stu-id="4545c-164">Provide sync functionality across multiple systems</span></span>

<span data-ttu-id="4545c-165">**Inicio** (actualizaciones potenciales en la versión beta)</span><span class="sxs-lookup"><span data-stu-id="4545c-165">**Startup** (Potential updates in Beta)</span></span>

<span data-ttu-id="4545c-166">Copia de seguridad y recuperación</span><span class="sxs-lookup"><span data-stu-id="4545c-166">Backup & Recovery</span></span>

<span data-ttu-id="4545c-167">Punto de entrada para guardar y restaurar el estado de los archivos, la configuración o los sistemas completos</span><span class="sxs-lookup"><span data-stu-id="4545c-167">Entry point to save and restore the state of files, settings, or entire systems</span></span>

<span data-ttu-id="4545c-168">**Aplicación de la tienda Windows para interactuar con los usuarios**</span><span class="sxs-lookup"><span data-stu-id="4545c-168">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="4545c-169">Telemetría</span><span class="sxs-lookup"><span data-stu-id="4545c-169">Telemetry</span></span>

<span data-ttu-id="4545c-170">Recopile y envíe información sobre la experiencia del usuario y el entorno</span><span class="sxs-lookup"><span data-stu-id="4545c-170">Collect and send info about the user experience and environment</span></span>

<span data-ttu-id="4545c-171">**Tarea de mantenimiento**</span><span class="sxs-lookup"><span data-stu-id="4545c-171">**Maintenance Task**</span></span>

<span data-ttu-id="4545c-172">Supervisión de equipos</span><span class="sxs-lookup"><span data-stu-id="4545c-172">PC Monitoring</span></span>

<span data-ttu-id="4545c-173">Proporcionar supervisión de estado del sistema no solicitada y notificaciones que dupliquen la funcionalidad de bandeja de entrada existente</span><span class="sxs-lookup"><span data-stu-id="4545c-173">Provide unsolicited system state monitoring and notifications that duplicate existing inbox functionality</span></span>

<span data-ttu-id="4545c-174">**Remove**</span><span class="sxs-lookup"><span data-stu-id="4545c-174">**Remove**</span></span>

> [!Note]  
> <span data-ttu-id="4545c-175">La clave consiste en reducir las características duplicadas que existen en Windows</span><span class="sxs-lookup"><span data-stu-id="4545c-175">The key is to reduce duplicate features that exist in Windows</span></span>

<br/>

<span data-ttu-id="4545c-176">$ {ROWSPAN2} $**Security**$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="4545c-176">${ROWSPAN2}$**Security**${REMOVE}$</span></span>  

<span data-ttu-id="4545c-177">Filtros de & de control parental</span><span class="sxs-lookup"><span data-stu-id="4545c-177">Parental Control & Filters</span></span>

<span data-ttu-id="4545c-178">Aplicar reglas y restricciones establecidas para el acceso y el uso de Internet</span><span class="sxs-lookup"><span data-stu-id="4545c-178">Enforce rules and restrictions established for Internet access and usage</span></span>

<span data-ttu-id="4545c-179">**Startup**</span><span class="sxs-lookup"><span data-stu-id="4545c-179">**Startup**</span></span>

<span data-ttu-id="4545c-180">Configuración y administración</span><span class="sxs-lookup"><span data-stu-id="4545c-180">Configuration & Management</span></span>

<span data-ttu-id="4545c-181">Permitir a los usuarios controlar las opciones de diagnóstico y corrección para la supervisión de la seguridad del sistema notificar a los usuarios de los hallazgos y las acciones de seguridad</span><span class="sxs-lookup"><span data-stu-id="4545c-181">Allow users to control diagnostic and remediation options for system security monitoring Notify users of findings and security actions</span></span>

<span data-ttu-id="4545c-182">**Aplicación de la tienda Windows para interactuar con los usuarios**</span><span class="sxs-lookup"><span data-stu-id="4545c-182">**Windows Store app for interfacing with the users**</span></span>

<span data-ttu-id="4545c-183">**Comunicación & Internet** (im & VoIP)</span><span class="sxs-lookup"><span data-stu-id="4545c-183">**Communication & Internet** (IM & VoIP)</span></span>

<span data-ttu-id="4545c-184">Envío y recepción de mensajes y llamadas</span><span class="sxs-lookup"><span data-stu-id="4545c-184">Send and receive messages and calls</span></span>

<span data-ttu-id="4545c-185">**Aplicación de la tienda Windows**</span><span class="sxs-lookup"><span data-stu-id="4545c-185">**Windows Store app**</span></span>

<span data-ttu-id="4545c-186">**Música & MP3**</span><span class="sxs-lookup"><span data-stu-id="4545c-186">**Music & MP3**</span></span>

<span data-ttu-id="4545c-187">Reproducir, almacenar y administrar música</span><span class="sxs-lookup"><span data-stu-id="4545c-187">Play, store, and manage music</span></span>

<span data-ttu-id="4545c-188">**Aplicación de la tienda Windows**</span><span class="sxs-lookup"><span data-stu-id="4545c-188">**Windows Store app**</span></span>

<span data-ttu-id="4545c-189">**Vídeo de & de fotos**</span><span class="sxs-lookup"><span data-stu-id="4545c-189">**Photo & Video**</span></span>

<span data-ttu-id="4545c-190">Detección, registro, representación, almacenamiento y administración de fotos y vídeos</span><span class="sxs-lookup"><span data-stu-id="4545c-190">Detect, record, render, store and manage photos and videos</span></span>

<span data-ttu-id="4545c-191">**Aplicación de la tienda Windows**</span><span class="sxs-lookup"><span data-stu-id="4545c-191">**Windows Store app**</span></span>

<span data-ttu-id="4545c-192">**Juegos de equipos**</span><span class="sxs-lookup"><span data-stu-id="4545c-192">**PC Gaming**</span></span>

<span data-ttu-id="4545c-193">Iniciar juegos en varios dominios</span><span class="sxs-lookup"><span data-stu-id="4545c-193">Launch games across various domains</span></span>

<span data-ttu-id="4545c-194">**Aplicación de la tienda Windows**</span><span class="sxs-lookup"><span data-stu-id="4545c-194">**Windows Store app**</span></span>

<span data-ttu-id="4545c-195">**& anuncio de venta incremental**</span><span class="sxs-lookup"><span data-stu-id="4545c-195">**Upsell & Advertisement**</span></span>

<span data-ttu-id="4545c-196">Atraer la atención a los productos y servicios disponibles para su compra</span><span class="sxs-lookup"><span data-stu-id="4545c-196">Draw attention to goods and services available for purchase</span></span>

<span data-ttu-id="4545c-197">**Remove**</span><span class="sxs-lookup"><span data-stu-id="4545c-197">**Remove**</span></span>



 

> [!Note]  
> <span data-ttu-id="4545c-198">Las directrices de las aplicaciones de accesibilidad están descubridas por las interacciones directas con los ISV.</span><span class="sxs-lookup"><span data-stu-id="4545c-198">Accessibility apps guidelines are covered by separate direct engagements with ISVs.</span></span> <span data-ttu-id="4545c-199">Consulte [*programación para facilitar el acceso*](../winauto/ease-of-access---assistive-technology-registration.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4545c-199">See [*Programming for Ease of Access*](../winauto/ease-of-access---assistive-technology-registration.md) for details.</span></span>

 

<span data-ttu-id="4545c-200">**Aplicaciones de la Tienda Windows**</span><span class="sxs-lookup"><span data-stu-id="4545c-200">**Windows Store apps**</span></span>

<span data-ttu-id="4545c-201">Las aplicaciones de la tienda Windows mejoran la experiencia del usuario al introducir un espacio de Windows con nuevas coordenadas: un nuevo modelo de aplicación, una nueva interfaz de usuario y una tienda Windows.</span><span class="sxs-lookup"><span data-stu-id="4545c-201">Windows Store apps enhance the user experience by introducing a Windows space with new coordinates: a new app model, a new user interface, and a Windows Store.</span></span> <span data-ttu-id="4545c-202">Estas opciones de lenguaje y presentación están disponibles para desarrollar aplicaciones de la tienda Windows:</span><span class="sxs-lookup"><span data-stu-id="4545c-202">These language and presentation framework options are available for developing Windows Store apps:</span></span>

-   <span data-ttu-id="4545c-203">HTML/JavaScript/CSS</span><span class="sxs-lookup"><span data-stu-id="4545c-203">HTML/JavaScript/CSS</span></span>
-   <span data-ttu-id="4545c-204">XAML/C #</span><span class="sxs-lookup"><span data-stu-id="4545c-204">XAML/C#</span></span>
-   <span data-ttu-id="4545c-205">XAML/C++</span><span class="sxs-lookup"><span data-stu-id="4545c-205">XAML/C++</span></span>

<span data-ttu-id="4545c-206">La información agregada para desarrollar aplicaciones de la tienda Windows está disponible en el [centro de desarrollo de Windows](https://msdn.microsoft.com/windows/apps/).</span><span class="sxs-lookup"><span data-stu-id="4545c-206">Aggregated info for developing Windows Store apps is available at the [Windows Dev Center](https://msdn.microsoft.com/windows/apps/).</span></span>

<span data-ttu-id="4545c-207">Ejemplos:</span><span class="sxs-lookup"><span data-stu-id="4545c-207">Examples:</span></span>

-   <span data-ttu-id="4545c-208">[Desarrollo de juegos de la tienda Windows](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="4545c-208">[Developing Windows Store games](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
-   <span data-ttu-id="4545c-209">[Desarrollo de una aplicación de la tienda Windows que usa medios](/previous-versions/windows/apps/hh465132(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="4545c-209">[Developing Windows Store app that use Media](/previous-versions/windows/apps/hh465132(v=win.10))</span></span>

<span data-ttu-id="4545c-210">**Tareas de mantenimiento automático**</span><span class="sxs-lookup"><span data-stu-id="4545c-210">**Automatic maintenance tasks**</span></span>

<span data-ttu-id="4545c-211">La actividad en segundo plano periódica debe diseñarse como tareas de mantenimiento automático.</span><span class="sxs-lookup"><span data-stu-id="4545c-211">Periodic background activity should be designed as Automatic Maintenance tasks.</span></span> <span data-ttu-id="4545c-212">Se programan en tiempo de inactividad del sistema para aumentar la capacidad de respuesta y la eficiencia energética de los equipos Windows.</span><span class="sxs-lookup"><span data-stu-id="4545c-212">These are scheduled at system idle time to increase the responsiveness and energy efficiency of Windows PCs.</span></span> <span data-ttu-id="4545c-213">Las tareas de mantenimiento pueden crearse y configurarse con una aplicación de escritorio en el momento de la instalación, mediante el SDK de escritorio.</span><span class="sxs-lookup"><span data-stu-id="4545c-213">Maintenance tasks can be created and configured by a desktop app at install time, using the desktop SDK.</span></span> <span data-ttu-id="4545c-214">Consulte el tema de mantenimiento automático que se muestra a continuación para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="4545c-214">See the Automatic Maintenance topic that follows for details.</span></span>

## <a name="resources"></a><span data-ttu-id="4545c-215">Recursos</span><span class="sxs-lookup"><span data-stu-id="4545c-215">Resources</span></span>

-   [<span data-ttu-id="4545c-216">Directrices de accesibilidad</span><span class="sxs-lookup"><span data-stu-id="4545c-216">Accessibility Guidelines</span></span>](../winauto/ease-of-access---assistive-technology-registration.md)
-   [<span data-ttu-id="4545c-217">Centro de desarrollo de Windows</span><span class="sxs-lookup"><span data-stu-id="4545c-217">Windows Dev Center</span></span>](https://msdn.microsoft.com/windows/apps/)
-   <span data-ttu-id="4545c-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="4545c-218">[Windows ADK](/previous-versions/windows/hh825494(v=win.10))</span></span>

 

