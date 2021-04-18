---
description: .
ms.assetid: f022374d-ea3f-477f-9b59-3188b775ed64
title: Manifiesto de aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4fd1ae8a9f66dafbe65a3db09dd014dbef31e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717131"
---
# <a name="application-manifest"></a><span data-ttu-id="381cc-103">Manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="381cc-103">Application Manifest</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="381cc-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="381cc-104">Affected Platforms</span></span>

<span data-ttu-id="381cc-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="381cc-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="381cc-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="381cc-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="381cc-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="381cc-107">Feature Impact</span></span>

 <span data-ttu-id="381cc-108">**Gravedad** baja</span><span class="sxs-lookup"><span data-stu-id="381cc-108">**Severity** - Low</span></span>  
<span data-ttu-id="381cc-109">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="381cc-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="381cc-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="381cc-110">Description</span></span>

<span data-ttu-id="381cc-111">Windows 7 incluye una nueva sección en el manifiesto de aplicación denominada "compatibilidad".</span><span class="sxs-lookup"><span data-stu-id="381cc-111">Windows 7 introduces a new section in the application manifest called "Compatibility."</span></span> <span data-ttu-id="381cc-112">En esta sección se ayuda a Windows a determinar las versiones de Windows a las que se diseñó una aplicación y se permite a Windows proporcionar el comportamiento que espera la aplicación en función de la versión de Windows de destino de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="381cc-112">This section helps Windows determine the versions of Windows that an application was designed to target, and enables Windows to provide the behavior that the application expects based on the version of Windows that the application targeted.</span></span>

<span data-ttu-id="381cc-113">La sección de compatibilidad permite a Windows proporcionar un nuevo comportamiento al nuevo software creado por el desarrollador, a la vez que mantiene la compatibilidad con el software existente.</span><span class="sxs-lookup"><span data-stu-id="381cc-113">The Compatibility section allows Windows to provide new behavior to new developer-created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="381cc-114">Esta sección también ayuda a Windows a ofrecer mayor compatibilidad en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="381cc-114">This section also helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="381cc-115">Por ejemplo, una aplicación que declare solo compatibilidad con Windows 7 en la sección de compatibilidad seguirá recibiendo el comportamiento de Windows 7 en una versión futura de Windows.</span><span class="sxs-lookup"><span data-stu-id="381cc-115">For example, an application declaring support only for Windows 7 in the Compatibility section will continue to receive Windows 7 behavior in future version of Windows.</span></span>

## <a name="manifestation-of-change"></a><span data-ttu-id="381cc-116">Manifiesto de cambio</span><span class="sxs-lookup"><span data-stu-id="381cc-116">Manifestation of Change</span></span>

<span data-ttu-id="381cc-117">Las aplicaciones sin una sección de compatibilidad en su manifiesto recibirán el comportamiento de Windows Vista de forma predeterminada en Windows 7 y versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="381cc-117">Applications without a Compatibility section in their manifest will receive Windows Vista behavior by default on Windows 7 and future Windows versions.</span></span> <span data-ttu-id="381cc-118">Tenga en cuenta que Windows XP y Windows Vista omiten esta sección del manifiesto y no tienen ningún impacto en ellos.</span><span class="sxs-lookup"><span data-stu-id="381cc-118">Note that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="381cc-119">Los siguientes componentes de Windows proporcionan un comportamiento divergente basado en la sección de compatibilidad de Windows 7:</span><span class="sxs-lookup"><span data-stu-id="381cc-119">The following Windows components provide divergent behavior based on the Compatibility section in Windows 7:</span></span>

<span data-ttu-id="381cc-120">**Grupo de subprocesos predeterminado de RPC**</span><span class="sxs-lookup"><span data-stu-id="381cc-120">**RPC Default Thread Pool**</span></span>

-   <span data-ttu-id="381cc-121">**Windows 7:** Para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC ha cambiado al grupo de subprocesos de NT (grupo predeterminado).</span><span class="sxs-lookup"><span data-stu-id="381cc-121">**Windows 7:** To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="381cc-122">En Windows Vista, RPC usaba un grupo de subprocesos privados.</span><span class="sxs-lookup"><span data-stu-id="381cc-122">For Windows Vista, RPC used a private thread pool.</span></span>
    -   <span data-ttu-id="381cc-123">Para los archivos binarios compilados para Win7, se usa el grupo predeterminado</span><span class="sxs-lookup"><span data-stu-id="381cc-123">For binaries compiled for Win7 the default pool is used</span></span>
    -   <span data-ttu-id="381cc-124">Si \_ se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API de RPC, se usa el grupo de subprocesos privados (comportamiento de vista)</span><span class="sxs-lookup"><span data-stu-id="381cc-124">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior)</span></span>
    -   <span data-ttu-id="381cc-125">Si \_ se llama a RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="381cc-125">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported</span></span>
-   <span data-ttu-id="381cc-126">**Windows Vista (valor predeterminado):** Para los archivos binarios compilados para Windows Vista y versiones anteriores, se usa el grupo privado.</span><span class="sxs-lookup"><span data-stu-id="381cc-126">**Windows Vista (default):** For binaries compiled for Windows Vista and below, the private pool is used.</span></span>

<span data-ttu-id="381cc-127">**Bloqueo DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="381cc-127">**DirectDraw Lock**</span></span>

-   <span data-ttu-id="381cc-128">**Windows 7:** Las aplicaciones con manifiesto para Windows 7 no pueden llamar a la API de bloqueo en DDRAW para bloquear el búfer de vídeo del escritorio primario.</span><span class="sxs-lookup"><span data-stu-id="381cc-128">**Windows 7:** Applications manifested for Windows 7 cannot call Lock API in DDRAW to lock the primary Desktop video buffer.</span></span> <span data-ttu-id="381cc-129">Si lo hace, se producirá un error y se devolverá el puntero **null** para la principal.</span><span class="sxs-lookup"><span data-stu-id="381cc-129">Doing so will result in error, and **NULL** pointer for the primary will be returned.</span></span> <span data-ttu-id="381cc-130">Este comportamiento se aplica incluso si Administrador de ventanas de escritorio composición no está activada.</span><span class="sxs-lookup"><span data-stu-id="381cc-130">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="381cc-131">Las aplicaciones compatibles con Windows 7 no deben bloquear el búfer de vídeo principal para que se represente.</span><span class="sxs-lookup"><span data-stu-id="381cc-131">Windows 7 compatible applications must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="381cc-132">**Windows Vista (valor predeterminado):** Las aplicaciones podrán adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="381cc-132">**Windows Vista (default):** Applications will be able to acquire a lock on the primary video buffer as legacy applications depend on this behavior.</span></span> <span data-ttu-id="381cc-133">La ejecución de la aplicación desactiva Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="381cc-133">Running the application turns off Desktop Window Manager.</span></span>

<span data-ttu-id="381cc-134">**Transferencia de bloque de bits de DirectDraw (BLT) a principal sin ventana de recorte**</span><span class="sxs-lookup"><span data-stu-id="381cc-134">**DirectDraw Bit Block Transfer (Blt) to Primary without Clipping Window**</span></span>

-   <span data-ttu-id="381cc-135">**Windows 7:** Las aplicaciones con manifiesto para Windows 7 no pueden realizar la ejecución de BLT en el búfer de vídeo de escritorio primario sin una ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="381cc-135">**Windows 7:** Applications manifested for Windows 7 are prevented from performing Blt's to the primary Desktop video buffer without a clipping window.</span></span> <span data-ttu-id="381cc-136">Si lo hace, se producirá un error y el área BLT no se representará.</span><span class="sxs-lookup"><span data-stu-id="381cc-136">Doing so will result in error and the Blt area will not be rendered.</span></span> <span data-ttu-id="381cc-137">Windows aplica este comportamiento incluso si no activa Administrador de ventanas de escritorio composición.</span><span class="sxs-lookup"><span data-stu-id="381cc-137">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="381cc-138">Las aplicaciones compatibles con Windows 7 deben tener BLT en una ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="381cc-138">Windows 7 compatible applications must Blt to a clipping window.</span></span>
-   <span data-ttu-id="381cc-139">**Windows Vista (valor predeterminado):** Las aplicaciones deben ser capaces de iniciar sesión en la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="381cc-139">**Windows Vista (default):** Applications must be able to Blt to the primary without a clipping window as legacy applications depend on this behavior.</span></span> <span data-ttu-id="381cc-140">Al ejecutar esta aplicación, se desactiva el Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="381cc-140">Running this application turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="381cc-141">**API de GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="381cc-141">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="381cc-142">**Windows 7:** Resuelve una condición de carrera en la que una aplicación multiproceso que usa GetOverlappedResult puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función devuelva prematuramente.</span><span class="sxs-lookup"><span data-stu-id="381cc-142">**Windows 7:** Resolves a race condition where a multithreaded app using GetOverlappedResult can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="381cc-143">**Windows Vista (valor predeterminado):** Proporciona el comportamiento con la condición de carrera en la que las aplicaciones pueden tener una dependencia.</span><span class="sxs-lookup"><span data-stu-id="381cc-143">**Windows Vista (default):** Provides the behavior with the race condition that applications may have a dependency on.</span></span> <span data-ttu-id="381cc-144">Las aplicaciones que quieran evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señalice, llamar a GetOverlappedResult con bWait = = **false**.</span><span class="sxs-lookup"><span data-stu-id="381cc-144">Applications wishing to avoid this race prior to the Windows 7 behavior should wait on the overlapped event and when signaled, call GetOverlappedResult with bWait == **FALSE**.</span></span>

<span data-ttu-id="381cc-145">**Asistente para la compatibilidad de programas (PCA)**</span><span class="sxs-lookup"><span data-stu-id="381cc-145">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="381cc-146">**Windows 7:** En la sección aplicaciones con compatibilidad no se obtiene la mitigación del PCA.</span><span class="sxs-lookup"><span data-stu-id="381cc-146">**Windows 7:** Applications with Compatibility section will not get the PCA mitigation.</span></span>
-   <span data-ttu-id="381cc-147">**Windows Vista (valor predeterminado):** Las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en algunas circunstancias específicas obtendrán la mitigación del PCA.</span><span class="sxs-lookup"><span data-stu-id="381cc-147">**Windows Vista (default):** Applications that fail to install properly or crash during runtime under some specific circumstances will get the PCA mitigation.</span></span> <span data-ttu-id="381cc-148">Para obtener más información, consulte la sección de referencia.</span><span class="sxs-lookup"><span data-stu-id="381cc-148">For more details, see the reference section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="381cc-149">Aprovechar las capacidades de características</span><span class="sxs-lookup"><span data-stu-id="381cc-149">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="381cc-150">Actualice el manifiesto de aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="381cc-150">Update the application manifest with the latest Compatibility information for operating system support.</span></span> <span data-ttu-id="381cc-151">En la sección se describen las adiciones al manifiesto:</span><span class="sxs-lookup"><span data-stu-id="381cc-151">The section describes the additions to the manifest:</span></span>

-   <span data-ttu-id="381cc-152">**Espacio de nombres:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="381cc-152">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

-   <span data-ttu-id="381cc-153">**Nombre de sección:** Compatibilidad (nueva sección)</span><span class="sxs-lookup"><span data-stu-id="381cc-153">**Section Name:** Compatibility (new section)</span></span>

-   <span data-ttu-id="381cc-154">**Compatibles:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos admitidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="381cc-154">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

    -   <span data-ttu-id="381cc-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} para Windows Vista: este es el valor predeterminado para el contexto de Switchback.</span><span class="sxs-lookup"><span data-stu-id="381cc-155">{e2011457-1546-43c5-a5fe-008deee3d3f0} for Windows Vista: This is the default value for the switchback context.</span></span>
    -   <span data-ttu-id="381cc-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} para Windows 7: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="381cc-156">{35138b9a-5d96-4fbd-8e2d-a2440225f93a} for Windows 7: Applications that set this value in the application manifest get the Windows 7 behavior.</span></span>

    > [!Note]  
    > <span data-ttu-id="381cc-157">Microsoft generará y publicará GUID para futuras versiones de Windows según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="381cc-157">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

     

<span data-ttu-id="381cc-158">El siguiente es un ejemplo de manifiesto actualizado.</span><span class="sxs-lookup"><span data-stu-id="381cc-158">The following is an example of an updated manifest.</span></span>

> [!Note]  
> <span data-ttu-id="381cc-159">Los nombres de atributo y etiqueta en el manifiesto de aplicación distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="381cc-159">The attribute and tag names in the application manifest are case sensitive.</span></span>

 


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



<span data-ttu-id="381cc-160">El valor de agregar GUID para ambos sistemas operativos en el ejemplo anterior es proporcionar compatibilidad de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="381cc-160">The value of adding GUIDs for both operating systems in the above example is to provide down-level support.</span></span> <span data-ttu-id="381cc-161">Las aplicaciones que admiten ambas plataformas no necesitarán manifiestos independientes para cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="381cc-161">Applications that support both platforms would not need separate manifests for each platform.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="381cc-162">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="381cc-162">Compatibility, Performance, Reliability, and Usability Testing</span></span>

1.  <span data-ttu-id="381cc-163">Pruebe la aplicación con la nueva sección de compatibilidad y `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` para asegurarse de que la aplicación funciona correctamente con el comportamiento más reciente de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="381cc-163">Test the application with the new compatibility section and `SupportedOS ID ={35138b9a-5d96-4fbd-8e2d-a2440225f93a}` to ensure that the application works properly using the latest Windows 7 behavior</span></span>
2.  <span data-ttu-id="381cc-164">Pruebe la aplicación con la nueva sección de compatibilidad y `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (o sin esta sección completamente) para asegurarse de que la aplicación funciona correctamente con los comportamientos de Windows Vista en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="381cc-164">Test the application with the new compatibility section and `SupportedOS ID ={e2011457-1546-43c5-a5fe-008deee3d3f0}` (or without this section entirely) to ensure that the application works properly using the Windows Vista behaviors on Windows 7</span></span>

## <a name="known-issues"></a><span data-ttu-id="381cc-165">Problemas conocidos</span><span class="sxs-lookup"><span data-stu-id="381cc-165">Known Issues</span></span>

<span data-ttu-id="381cc-166">Error de **coincidencia de contexto** Una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="381cc-166">**Context Mismatch** An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of either Windows 7 or Windows Server 2008 R2.</span></span>

<span data-ttu-id="381cc-167">**Solución** de Hay actualizaciones disponibles para corregir este fin en todas las versiones compatibles basadas en x64 de Windows 7 y Windows Server 2008 R2, así como para todas las versiones compatibles basadas en Itanium de Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="381cc-167">**Solution** Updates are available to correct this for all supported x64-based versions of Windows 7 and Windows Server 2008 R2, as well as for all supported Itanium-based versions of Windows Server 2008 R2.</span></span> <span data-ttu-id="381cc-168">Vaya a la página de Soporte técnico de Microsoft de [KB 978637: una aplicación se ejecuta en un contexto de Windows Vista en lugar de en un contexto de Windows 7 en un equipo que ejecuta una edición x64 de Windows 7 o Windows Server 2008 R2](https://support.microsoft.com/kb/978637) para obtener más detalles y descargar la versión correcta del sistema.</span><span class="sxs-lookup"><span data-stu-id="381cc-168">Go to the Microsoft Support page for [KB 978637: An application runs in a Windows Vista context instead of in a Windows 7 context on a computer that is running an x64 edition of Windows 7 or of Windows Server 2008 R2](https://support.microsoft.com/kb/978637) for additional details and to download the correct version for your system.</span></span>

<span data-ttu-id="381cc-169">**Diagnóstico de volcado de bloqueo bloqueado**</span><span class="sxs-lookup"><span data-stu-id="381cc-169">**Crash dump diagnosis blocked**</span></span>

<span data-ttu-id="381cc-170">**Solución** de Vaya a la página de Soporte técnico de Microsoft de [KB 976038: las excepciones que se inician desde una aplicación que se ejecuta en una versión de Windows de 64 bits se omiten](https://support.microsoft.com/kb/976038) para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="381cc-170">**Solution** Go to the Microsoft Support page for [KB 976038: Exceptions that are thrown from an application that runs in a 64-bit version of Windows are ignored](https://support.microsoft.com/kb/976038) for additional details.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="381cc-171">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="381cc-171">Links to Other Resources</span></span>

-   [<span data-ttu-id="381cc-172">**QueryActCtxW función)**</span><span class="sxs-lookup"><span data-stu-id="381cc-172">**QueryActCtxW Function**</span></span>](/windows/win32/api/winbase/nf-winbase-queryactctxw)
-   <span data-ttu-id="381cc-173">[Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="381cc-173">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="381cc-174">Manifiestos de aplicación para aplicaciones Windows</span><span class="sxs-lookup"><span data-stu-id="381cc-174">Application manifests for Windows applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="381cc-175">Administrador de ventanas de escritorio (DWM)</span><span class="sxs-lookup"><span data-stu-id="381cc-175">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="381cc-176">Actualización de coincidencia de contexto</span><span class="sxs-lookup"><span data-stu-id="381cc-176">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)

 

 
