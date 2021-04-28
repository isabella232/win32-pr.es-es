---
description: Manifiesto de aplicación
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifiesto de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c52b8eb2af87c271151be3d7989f50b2903084
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088593"
---
# <a name="application-manifest"></a><span data-ttu-id="5c7bc-103">Manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="5c7bc-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="5c7bc-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="5c7bc-104">Affected Platforms</span></span>

<span data-ttu-id="5c7bc-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c7bc-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="5c7bc-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="5c7bc-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="5c7bc-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="5c7bc-107">Feature Impact</span></span>

 <span data-ttu-id="5c7bc-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="5c7bc-108">**Severity** - Low</span></span>  
<span data-ttu-id="5c7bc-109">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="5c7bc-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="5c7bc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c7bc-110">Description</span></span>

<span data-ttu-id="5c7bc-111">Windows 7 presenta una nueva sección en el manifiesto de aplicación denominada "Compatibilidad".</span><span class="sxs-lookup"><span data-stu-id="5c7bc-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="5c7bc-112">Esta sección ayuda a Windows a determinar las versiones de Windows a las que se diseñó una aplicación como destino y permite a Windows proporcionar el comportamiento esperado por la aplicación en función de la versión de Windows de destino de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="5c7bc-113">La sección Compatibilidad permite a Windows proporcionar un nuevo comportamiento al nuevo software creado por el desarrollador y mantener la compatibilidad con el software existente.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="5c7bc-114">Esta sección también ayuda a Windows a ofrecer mayor compatibilidad en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="5c7bc-115">Por ejemplo, una aplicación que declara compatibilidad solo para Windows 7 en la sección Compatibilidad seguirá recibiendo el comportamiento de Windows 7 en la versión futura de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="5c7bc-116">Demostración del cambio</span><span class="sxs-lookup"><span data-stu-id="5c7bc-116">Manifestation of Change</span></span>

<span data-ttu-id="5c7bc-117">Las aplicaciones sin una sección Compatibilidad de su manifiesto recibirán el comportamiento de Windows Vista de forma predeterminada en Windows 7 y versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="5c7bc-118">Tenga en cuenta que Windows XP y Windows Vista omiten esta sección de manifiesto y no tiene ningún impacto en ellos.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="5c7bc-119">Los siguientes componentes de Windows proporcionan un comportamiento divergente en función de la sección Compatibilidad de Windows 7:</span><span class="sxs-lookup"><span data-stu-id="5c7bc-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="5c7bc-120">**Grupo de subprocesos predeterminado de RPC**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="5c7bc-121">**Windows 7:** Para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC cambió al grupo de subprocesos nt (grupo predeterminado).</span><span class="sxs-lookup"><span data-stu-id="5c7bc-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="5c7bc-122">Para Windows Vista, RPC usaba un grupo de subprocesos privado.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="5c7bc-123">En el caso de los archivos binarios compilados para Win7, se usa el grupo predeterminado</span><span class="sxs-lookup"><span data-stu-id="5c7bc-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="5c7bc-124">Si se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API de RPC, se usa el grupo de subprocesos privado \_ (comportamiento de Vista)</span><span class="sxs-lookup"><span data-stu-id="5c7bc-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="5c7bc-125">Si se llama a I RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo \_ predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="5c7bc-126">**Windows Vista (valor predeterminado):** En el caso de los archivos binarios compilados para Windows Vista y versiones siguientes, se usa el grupo privado.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="5c7bc-127">**Bloqueo de DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="5c7bc-128">**Windows 7:** Las aplicaciones manifestadas para Windows 7 no pueden llamar a Lock API en DDRAW para bloquear el búfer de vídeo de escritorio principal.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="5c7bc-129">Si lo hace, se producirá un error y se devolverá el puntero **NULL** para la principal.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="5c7bc-130">Este comportamiento se aplica incluso si Administrador de ventanas de escritorio Composition no está activado.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="5c7bc-131">Las aplicaciones compatibles con Windows 7 no deben bloquear el búfer de vídeo principal que se va a representar.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="5c7bc-132">**Windows Vista (valor predeterminado):** Las aplicaciones podrán adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="5c7bc-133">La ejecución de la aplicación se desactiva Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="5c7bc-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="5c7bc-135">**Windows 7:** Se impide que las aplicaciones manifestadas para Windows 7 realicen Blt en el búfer de vídeo de escritorio principal sin una ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="5c7bc-136">Si lo hace, se producirá un error y el área Blt no se representará.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="5c7bc-137">Windows aplica este comportamiento incluso si no se activa Administrador de ventanas de escritorio Composition.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="5c7bc-138">Las aplicaciones compatibles con Windows 7 deben ir a una ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="5c7bc-139">**Windows Vista (valor predeterminado):** Las aplicaciones deben poder ir a la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="5c7bc-140">La ejecución de esta aplicación desactiva el Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="5c7bc-141">**GetOverlappedResult API**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="5c7bc-142">**Windows 7:** Resuelve una condición de carrera en la que una aplicación multiproceso mediante GetOverlappedResult puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función vuelva prematuramente.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="5c7bc-143">**Windows Vista (valor predeterminado):** Proporciona el comportamiento con la condición de carrera de la que las aplicaciones pueden tener una dependencia.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="5c7bc-144">Las aplicaciones que quieran evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señalen, llamar a GetOverlappedResult con bWait == **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="5c7bc-145">**Asistente para la compatibilidad de programas (PCA)**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="5c7bc-146">**Windows 7:** La sección Aplicaciones con compatibilidad no obtiene la mitigación de PCA.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="5c7bc-147">**Windows Vista (valor predeterminado):** Las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en determinadas circunstancias tendrán la mitigación de PCA.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="5c7bc-148">Para más información, consulte la sección de referencia.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="5c7bc-149">Aprovechamiento de las funcionalidades de características</span><span class="sxs-lookup"><span data-stu-id="5c7bc-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="5c7bc-150">Actualice el manifiesto de aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="5c7bc-151">En la sección se describen las adiciones al manifiesto:</span><span class="sxs-lookup"><span data-stu-id="5c7bc-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="5c7bc-152">**Espacio de nombres:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span><span class="sxs-lookup"><span data-stu-id="5c7bc-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="5c7bc-153">**Nombre de sección:** Compatibilidad (nueva sección)</span><span class="sxs-lookup"><span data-stu-id="5c7bc-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="5c7bc-154">**SupportedOS:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos compatibles son:</span><span class="sxs-lookup"><span data-stu-id="5c7bc-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="5c7bc-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: este es el valor predeterminado para el contexto de conmutación por recuperación.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="5c7bc-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="5c7bc-157">Microsoft generará y publicará GUID para futuras versiones de Windows según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="5c7bc-158">A continuación se muestra un ejemplo de un manifiesto actualizado.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="5c7bc-159">Los nombres de atributo y etiqueta del manifiesto de aplicación distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?> 
  <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
    <compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
      <application> 
        <!--The ID below indicates application support for Windows Vista --> 
          <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates application support for Windows 7 --> 
          <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/> 
      </application> 
    </compatibility>
  </assembly>
```



<span data-ttu-id="5c7bc-160">El valor de agregar GUID para ambos sistemas operativos en el ejemplo anterior es proporcionar compatibilidad de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="5c7bc-161">Las aplicaciones que admiten ambas plataformas no necesitarán manifiestos independientes para cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="5c7bc-162">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="5c7bc-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="5c7bc-163">Pruebe la aplicación con la nueva sección de compatibilidad y asegúrese de que la aplicación funciona correctamente `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` con el comportamiento más reciente de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="5c7bc-164">Pruebe la aplicación con la nueva sección de compatibilidad y (o sin esta sección por completo) para asegurarse de que la aplicación funciona correctamente con los comportamientos de `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` Windows Vista en Windows 7</span><span class="sxs-lookup"><span data-stu-id="5c7bc-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="5c7bc-165">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="5c7bc-165">Known Issues</span></span>

<span data-ttu-id="5c7bc-166">**Error de coincidencia de contexto** Una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="5c7bc-167">**Solución** Hay actualizaciones disponibles para corregir esto en todas las versiones compatibles basadas en x64 de Windows 7 y Windows Server 2008 R2, así como para todas las versiones compatibles basadas en Itanium de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="5c7bc-168">Vaya a la página Soporte técnico de Microsoft de [KB 978637:](https://support.microsoft.com/kb/978637) una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o de Windows Server 2008 R2 para obtener más detalles y descargar la versión correcta para el sistema.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="5c7bc-169">**Diagnóstico de volcado de memoria bloqueado**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="5c7bc-170">**Solución** Vaya a la página Soporte técnico de Microsoft de [KB 976038:](https://support.microsoft.com/kb/976038) Las excepciones que se inician desde una aplicación que se ejecuta en una versión de 64 bits de Windows se omiten para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="5c7bc-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="5c7bc-171">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="5c7bc-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="5c7bc-172">**QueryActCtxW (Función)**</span><span class="sxs-lookup"><span data-stu-id="5c7bc-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="5c7bc-173">[Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="5c7bc-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="5c7bc-174">Manifiestos de aplicación para aplicaciones Windows</span><span class="sxs-lookup"><span data-stu-id="5c7bc-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="5c7bc-175">Administrador de ventanas de escritorio (DWM)</span><span class="sxs-lookup"><span data-stu-id="5c7bc-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="5c7bc-176">Actualización de la discrepancia de contexto</span><span class="sxs-lookup"><span data-stu-id="5c7bc-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
