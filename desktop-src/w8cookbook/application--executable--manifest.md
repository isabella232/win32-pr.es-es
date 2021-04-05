---
title: Manifiesto de aplicación (ejecutable)
description: Manifiesto de aplicación (ejecutable)
ms.assetid: F46F33A6-0B2F-4086-9C6D-4AD43C26BCD3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6f5a1d26af4b8ac6314655013ed56275bf7d73
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/01/2020
ms.locfileid: "104078497"
---
# <a name="app-executable-manifest"></a><span data-ttu-id="2f261-103">Manifiesto de aplicación (ejecutable)</span><span class="sxs-lookup"><span data-stu-id="2f261-103">App (executable) manifest</span></span>

## <a name="platforms"></a><span data-ttu-id="2f261-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="2f261-104">Platforms</span></span>

<span data-ttu-id="2f261-105">**Clientes** : Windows 8</span><span class="sxs-lookup"><span data-stu-id="2f261-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="2f261-106">**Servidores** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2f261-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="2f261-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f261-107">Description</span></span>

<span data-ttu-id="2f261-108">La sección de compatibilidad del manifiesto de la aplicación (ejecutable) introducida en Windows ayuda al sistema operativo a determinar las versiones de Windows a las que se diseñó una aplicación como destino.</span><span class="sxs-lookup"><span data-stu-id="2f261-108">The compatibility section of the app (executable) manifest introduced in Windows helps the operating system determine the versions of Windows an app was designed to target.</span></span> <span data-ttu-id="2f261-109">Además, el manifiesto de la aplicación permite que Windows proporcione el comportamiento que espera la aplicación en función de la versión de Windows a la que se dirige la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f261-109">Additionally, the app manifest enables Windows to provide the behavior that the app expects based on the version of Windows that the app targeted.</span></span>

<span data-ttu-id="2f261-110">La sección de compatibilidad del manifiesto permite que Windows proporcione un nuevo comportamiento al software recién creado a la vez que mantiene la compatibilidad con el software existente.</span><span class="sxs-lookup"><span data-stu-id="2f261-110">The compatibility section of the manifest allows Windows to provide new behavior to newly created software while maintaining the compatibility for existing software.</span></span> <span data-ttu-id="2f261-111">En esta sección también se ayuda a Windows a ofrecer mayor compatibilidad en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="2f261-111">This section helps Windows deliver greater compatibility in future versions of Windows as well.</span></span> <span data-ttu-id="2f261-112">Por ejemplo, una aplicación que solo admita Windows 8 en la sección de compatibilidad seguirá recibiendo el comportamiento de Windows 8 en versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="2f261-112">For example, an app declaring support for only Windows 8 in the compatibility section will continue to receive Windows 8 behavior in future versions of Windows.</span></span>

## <a name="manifestation"></a><span data-ttu-id="2f261-113">Manifestación</span><span class="sxs-lookup"><span data-stu-id="2f261-113">Manifestation</span></span>

<span data-ttu-id="2f261-114">Las aplicaciones sin una sección de compatibilidad en el manifiesto tendrán el comportamiento de Windows Vista de forma predeterminada en Windows 7 y Windows 8 y versiones futuras de Windows.</span><span class="sxs-lookup"><span data-stu-id="2f261-114">Apps without a compatibility section in their manifest will have Windows Vista behavior by default on Windows 7 and Windows 8 and future Windows versions.</span></span> <span data-ttu-id="2f261-115">Tenga en cuenta que Windows XP y Windows Vista omiten esta sección del manifiesto y no tienen ningún impacto en ellos.</span><span class="sxs-lookup"><span data-stu-id="2f261-115">Be aware that Windows XP and Windows Vista ignore this manifest section and it has no impact on them.</span></span>

<span data-ttu-id="2f261-116">Estos componentes de Windows proporcionan un comportamiento divergente basado en la sección de compatibilidad:</span><span class="sxs-lookup"><span data-stu-id="2f261-116">These Windows components provide divergent behavior based on the compatibility section:</span></span>

<span data-ttu-id="2f261-117">**Grupo de subprocesos predeterminado de llamada a procedimiento remoto (RPC)**</span><span class="sxs-lookup"><span data-stu-id="2f261-117">**Remote procedure call (RPC) default thread pool**</span></span>

-   <span data-ttu-id="2f261-118">Windows 8 y Windows 7: para mejorar la escalabilidad y reducir los recuentos de subprocesos, RPC ha cambiado al grupo de subprocesos de NT (grupo predeterminado).</span><span class="sxs-lookup"><span data-stu-id="2f261-118">Windows 8 and Windows 7: To improve scalability and reduce thread counts, RPC switched to the NT thread pool (default pool).</span></span> <span data-ttu-id="2f261-119">En Windows Vista, RPC usaba un grupo de subprocesos privados:</span><span class="sxs-lookup"><span data-stu-id="2f261-119">For Windows Vista, RPC used a private thread pool:</span></span>

    -   <span data-ttu-id="2f261-120">Para los archivos binarios compilados para Windows 7 y versiones posteriores de Windows, se usa el grupo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="2f261-120">For binaries compiled for Windows 7 and later versions of Windows, the default pool is used.</span></span>
    -   <span data-ttu-id="2f261-121">Si \_ se llama a I RpcMgmtEnableDedicatedThreadPool antes de llamar a cualquier API de RPC, se usa el grupo de subprocesos privados (comportamiento de vista).</span><span class="sxs-lookup"><span data-stu-id="2f261-121">If I\_RpcMgmtEnableDedicatedThreadPool is called before any RPC API is called, the private thread pool is used (Vista behavior).</span></span>
    -   <span data-ttu-id="2f261-122">Si \_ se llama a RpcMgmtEnableDedicatedThreadPool después de una llamada RPC, se usa el grupo predeterminado, I \_ RpcMgmtEnableDedicatedThreadPool devuelve el error 1764 y no se admite la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="2f261-122">If I\_RpcMgmtEnableDedicatedThreadPool is called after an RPC call, the default pool is used, I\_RpcMgmtEnableDedicatedThreadPool returns the error 1764, and the requested operation is not supported.</span></span>

-   <span data-ttu-id="2f261-123">Windows Vista (valor predeterminado): para los archivos binarios compilados para Windows Vista y versiones anteriores de Windows, se usa el grupo privado.</span><span class="sxs-lookup"><span data-stu-id="2f261-123">Windows Vista (default): For binaries compiled for Windows Vista and earlier versions of Windows, the private pool is used.</span></span>

<span data-ttu-id="2f261-124">**Bloqueo DirectDraw**</span><span class="sxs-lookup"><span data-stu-id="2f261-124">**DirectDraw lock**</span></span>

-   <span data-ttu-id="2f261-125">Windows 8 y Windows 7: las aplicaciones con manifiesto para Windows 7 y versiones posteriores del sistema operativo no pueden llamar a la API de bloqueo en DDRAW para bloquear el búfer de vídeo del escritorio primario. Si lo hace, se producirá un error y se devolverá un puntero nulo para el principal.</span><span class="sxs-lookup"><span data-stu-id="2f261-125">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of the operating system cannot call Lock API in DDRAW to lock the primary desktop video buffer; doing so will result in an error, and a NULL pointer for the primary is returned.</span></span> <span data-ttu-id="2f261-126">Este comportamiento se aplica incluso si Administrador de ventanas de escritorio composición no está activada.</span><span class="sxs-lookup"><span data-stu-id="2f261-126">This behavior is enforced even if Desktop Window Manager Composition is not turned on.</span></span> <span data-ttu-id="2f261-127">Las aplicaciones con compatibilidad declarada para Windows 7 y versiones posteriores no deben bloquear el búfer de vídeo primario para que se represente.</span><span class="sxs-lookup"><span data-stu-id="2f261-127">Apps with compatibility declared for Windows 7 and later must not lock the primary video buffer to render.</span></span>
-   <span data-ttu-id="2f261-128">Windows Vista (valor predeterminado): las aplicaciones pueden adquirir un bloqueo en el búfer de vídeo principal, ya que las aplicaciones heredadas dependen de este comportamiento. la ejecución de la aplicación desactiva Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f261-128">Windows Vista (default): Apps can acquire a lock on the primary video buffer, as legacy apps depend on this behavior; running the app turns off Desktop Window Manager.</span></span>

<span data-ttu-id="2f261-129">**Transferencia de bloque de bits de DirectDraw (bitblt) a principal sin ventana de recorte**</span><span class="sxs-lookup"><span data-stu-id="2f261-129">**DirectDraw bit-block transfer (bitblt) to primary without clipping window**</span></span>

-   <span data-ttu-id="2f261-130">Windows 8 y Windows 7: las aplicaciones con manifiesto para Windows 7 y versiones posteriores de Windows no pueden realizar una operación bitblt en el búfer de vídeo de escritorio primario sin una ventana de recorte. Si lo hace, se producirá un error y el área de bitblt no se representará.</span><span class="sxs-lookup"><span data-stu-id="2f261-130">Windows 8 and Windows 7: Apps manifested for Windows 7 and later versions of Windows are prevented from performing a bitblt to the primary Desktop video buffer without a clipping window; doing so results in an error and the bitblt area will not be rendered.</span></span> <span data-ttu-id="2f261-131">Windows aplica este comportamiento incluso si no activa Administrador de ventanas de escritorio composición.</span><span class="sxs-lookup"><span data-stu-id="2f261-131">Windows enforces this behavior even if you do not turn on Desktop Window Manager Composition.</span></span> <span data-ttu-id="2f261-132">Las aplicaciones con compatibilidad declarada para Windows 7 y versiones posteriores deben ejecutar bitblt en una ventana de recorte.</span><span class="sxs-lookup"><span data-stu-id="2f261-132">Apps with compatibility declared for Windows 7 and later must perform a bitblt to a clipping window.</span></span>
-   <span data-ttu-id="2f261-133">Windows Vista (valor predeterminado): las aplicaciones deben ser capaces de ejecutar bitblt en la principal sin una ventana de recorte, ya que las aplicaciones heredadas dependen de este comportamiento. al ejecutar esta aplicación, se desactiva el Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="2f261-133">Windows Vista (default): Apps must be able to perform a bitblt to the primary without a clipping window, as legacy apps depend on this behavior; running this app turns off the Desktop Window Manager.</span></span>

<span data-ttu-id="2f261-134">**API de GetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="2f261-134">**GetOverlappedResult API**</span></span>

-   <span data-ttu-id="2f261-135">Windows 8 y Windows 7: resuelve una condición de carrera en la que una aplicación multiproceso que usa **GetOverlappedResult** puede devolver sin restablecer el evento en la estructura superpuesta, lo que hace que la siguiente llamada a esta función devuelva prematuramente.</span><span class="sxs-lookup"><span data-stu-id="2f261-135">Windows 8 and Windows 7: Resolves a race condition where a multithreaded app using **GetOverlappedResult** can return without resetting the event in the overlapped structure, causing the next call to this function to return prematurely.</span></span>
-   <span data-ttu-id="2f261-136">Windows Vista (valor predeterminado): proporciona el comportamiento con la condición de carrera en la que las aplicaciones pueden tener una dependencia.</span><span class="sxs-lookup"><span data-stu-id="2f261-136">Windows Vista (default): Provides the behavior with the race condition that apps might have a dependency on.</span></span> <span data-ttu-id="2f261-137">Las aplicaciones que deben evitar esta carrera antes del comportamiento de Windows 7 deben esperar en el evento superpuesto y, cuando se señalice, llamar a GetOverlappedResult con bWait = = FALSE.</span><span class="sxs-lookup"><span data-stu-id="2f261-137">Apps that must avoid this race prior to the Windows 7 behavior should wait on the overlapped event and, when signaled, call GetOverlappedResult with bWait == FALSE.</span></span>

<span data-ttu-id="2f261-138">**Estado de los temas de Shell en el modo de contraste alto**</span><span class="sxs-lookup"><span data-stu-id="2f261-138">**Shell themes status in high contrast mode**</span></span>

-   <span data-ttu-id="2f261-139">Windows 8: devuelve el estado real de los Estados de en el modo de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="2f261-139">Windows 8: Returns the real theming status for when in high contrast mode.</span></span>
-   <span data-ttu-id="2f261-140">Windows 7: devuelve como no disponible en el modo de contraste alto porque DWM todavía está activado.</span><span class="sxs-lookup"><span data-stu-id="2f261-140">Windows 7: Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>
-   <span data-ttu-id="2f261-141">Windows Vista (valor predeterminado): devuelve como no disponible en el modo de contraste alto porque DWM todavía está activado.</span><span class="sxs-lookup"><span data-stu-id="2f261-141">Windows Vista (default): Returns theming as unavailable when in high contrast mode because DWM is still on.</span></span>

<span data-ttu-id="2f261-142">**Shell iPersistFile:: Save (método)**</span><span class="sxs-lookup"><span data-stu-id="2f261-142">**Shell iPersistFile::Save method**</span></span>

-   <span data-ttu-id="2f261-143">Windows 8: CShellLink:: Save ahora determina si se llama al controlador IPersistFile con un argumento de ruta de acceso relativa y produce un error en la llamada si es.</span><span class="sxs-lookup"><span data-stu-id="2f261-143">Windows 8: CShellLink::Save now determines if the IPersistFile handler is called with a relative path argument and fails the call if it is.</span></span>

    <span data-ttu-id="2f261-144">La [documentación pública](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) que describe este comportamiento indica que el argumento de ruta de acceso debe ser una ruta de acceso absoluta:</span><span class="sxs-lookup"><span data-stu-id="2f261-144">The [public documentation](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) describing this behavior indicates that path argument has to be an absolute path:</span></span>

-   <span data-ttu-id="2f261-145">Windows 7 y versiones anteriores (valor predeterminado): CShellLink:: Save no determina si el controlador iPersistFile envía una comprobación de ruta de acceso relativa y permite que las aplicaciones sigan trabajando con rutas de acceso absolutas o relativas.</span><span class="sxs-lookup"><span data-stu-id="2f261-145">Windows 7 and earlier (default): CShellLink::Save does not determine if the iPersistFile handler sends a relative path check and allows apps to continue working with absolute or relative paths.</span></span>

<span data-ttu-id="2f261-146">**Asistente para la compatibilidad de programas (PCA)**</span><span class="sxs-lookup"><span data-stu-id="2f261-146">**Program Compatibility Assistant (PCA)**</span></span>

-   <span data-ttu-id="2f261-147">Windows 8: las aplicaciones con la sección de compatibilidad no obtienen la mitigación del PCA.</span><span class="sxs-lookup"><span data-stu-id="2f261-147">Windows 8: Apps with the compatibility section do not get the PCA mitigation.</span></span>
-   <span data-ttu-id="2f261-148">Windows 7: se realiza un seguimiento de las aplicaciones con la sección de compatibilidad para detectar posibles problemas de compatibilidad con los cambios de Windows 8 (descritos en este documento).</span><span class="sxs-lookup"><span data-stu-id="2f261-148">Windows 7: Apps with the compatibility section are tracked for potential compatibility issues for Windows 8 changes (described in this document).</span></span>
-   <span data-ttu-id="2f261-149">Windows Vista (valor predeterminado): las aplicaciones que no se instalan correctamente o se bloquean durante el tiempo de ejecución en algunas circunstancias específicas obtienen la mitigación del PCA.</span><span class="sxs-lookup"><span data-stu-id="2f261-149">Windows Vista (default): Apps that fail to install properly or crash during runtime under some specific circumstances get the PCA mitigation.</span></span> <span data-ttu-id="2f261-150">Para obtener más información, consulte la sección de recursos.</span><span class="sxs-lookup"><span data-stu-id="2f261-150">For more info, see the Resources section.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="2f261-151">Aprovechar las capacidades de características</span><span class="sxs-lookup"><span data-stu-id="2f261-151">Leveraging feature capabilities</span></span>

<span data-ttu-id="2f261-152">Actualice el manifiesto de la aplicación con la información de compatibilidad más reciente para la compatibilidad con el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="2f261-152">Update the app manifest with the latest compatibility info for operating system support.</span></span> <span data-ttu-id="2f261-153">En esta sección se describen las adiciones al manifiesto:</span><span class="sxs-lookup"><span data-stu-id="2f261-153">This section describes the additions to the manifest:</span></span>

<span data-ttu-id="2f261-154">**Espacio de nombres:** Compatibility. v1 (xmlns = "urn: schemas-microsoft-com: Compatibility. v1" >)</span><span class="sxs-lookup"><span data-stu-id="2f261-154">**Namespace:** Compatibility.v1 (xmlns="urn:schemas-microsoft-com:compatibility.v1">)</span></span>

<span data-ttu-id="2f261-155">**Nombre de sección:** Compatibilidad (nueva sección)</span><span class="sxs-lookup"><span data-stu-id="2f261-155">**Section name:** Compatibility (new section)</span></span>

<span data-ttu-id="2f261-156">**Compatibles:** GUID del sistema operativo compatible: los GUID que se asignan a los sistemas operativos admitidos son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2f261-156">**SupportedOS:** GUID of supported operating system - The GUIDs that map to the supported operating systems are:</span></span>

-   <span data-ttu-id="2f261-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span><span class="sxs-lookup"><span data-stu-id="2f261-157">{e2011457-1546-43c5-a5fe-008deee3d3f0}</span></span>

    <span data-ttu-id="2f261-158">en **Windows Vista**: este es el valor predeterminado para el contexto Switchback</span><span class="sxs-lookup"><span data-stu-id="2f261-158">for **Windows Vista**: This is the default value for the switchback context</span></span>

-   <span data-ttu-id="2f261-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span><span class="sxs-lookup"><span data-stu-id="2f261-159">{35138b9a-5d96-4fbd-8e2d-a2440225f93a}</span></span>

    <span data-ttu-id="2f261-160">en **Windows 7**: las aplicaciones que establecen este valor en el manifiesto de la aplicación obtienen el comportamiento de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2f261-160">for **Windows 7**: Apps that set this value in the app manifest get the Windows 7 behavior</span></span>

-   <span data-ttu-id="2f261-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span><span class="sxs-lookup"><span data-stu-id="2f261-161">{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}</span></span>

    <span data-ttu-id="2f261-162">para **Windows 8**: las aplicaciones que establecen este valor en el manifiesto de aplicación obtienen el comportamiento de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f261-162">for **Windows 8**: Apps that set this value in the application manifest get the Windows 8 behavior</span></span>

<span data-ttu-id="2f261-163">Microsoft generará y publicará GUID para futuras versiones de Windows según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="2f261-163">Microsoft will generate and post GUIDs for future Windows versions as needed.</span></span>

<span data-ttu-id="2f261-164">Un ejemplo XML de un manifiesto actualizado:</span><span class="sxs-lookup"><span data-stu-id="2f261-164">An XML example of an updated manifest:</span></span>

> [!Note]  
> <span data-ttu-id="2f261-165">Los nombres de atributo y etiqueta en el manifiesto de la aplicación distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="2f261-165">The attribute and tag names in the app manifest are case sensitive.</span></span>

 


```XML
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"> 
<compatibility xmlns="urn:schemas-microsoft-com:compatibility.v1"> 
    <application> 
        <!--The ID below indicates app support for Windows Vista -->
        <supportedOS Id="{e2011457-1546-43c5-a5fe-008deee3d3f0}"/> 
        <!--The ID below indicates app support for Windows 7 -->
        <supportedOS Id="{35138b9a-5d96-4fbd-8e2d-a2440225f93a}"/>
        <!--The ID below indicates app support for Windows 8 -->
        <supportedOS Id="{4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38}"/>
    </application> 
</compatibility>
</assembly>
```



<span data-ttu-id="2f261-166">Los GUID de todos los sistemas operativos en el ejemplo anterior proporcionan compatibilidad de nivel inferior.</span><span class="sxs-lookup"><span data-stu-id="2f261-166">The GUIDs for all the operating systems in the previous example provide down-level support.</span></span> <span data-ttu-id="2f261-167">Las aplicaciones que admiten varias plataformas no necesitan manifiestos independientes para cada plataforma.</span><span class="sxs-lookup"><span data-stu-id="2f261-167">Apps that support multiple platforms do not need separate manifests for each platform.</span></span>

## <a name="tests"></a><span data-ttu-id="2f261-168">Pruebas</span><span class="sxs-lookup"><span data-stu-id="2f261-168">Tests</span></span>

<span data-ttu-id="2f261-169">Una aplicación puede especificar varios identificadores de sistema operativo compatibles.</span><span class="sxs-lookup"><span data-stu-id="2f261-169">An app can specify multiple supported operating system IDs.</span></span> <span data-ttu-id="2f261-170">Debe agregar un identificador de sistema operativo compatible Si ha probado o está realizando pruebas en el sistema operativo de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2f261-170">You should add a supported operating system ID if you have tested, or are in the process of testing, the app on that operating system.</span></span> <span data-ttu-id="2f261-171">Windows Vista y versiones anteriores del sistema operativo no prestan atención a estas entradas.</span><span class="sxs-lookup"><span data-stu-id="2f261-171">Windows Vista and prior operating system versions do not pay attention to these entries.</span></span> <span data-ttu-id="2f261-172">A partir de Windows 7, Windows elegirá el GUID de versión más alto del manifiesto hasta la versión de Windows en ejecución y proporcionará el soporte técnico de la aplicación en ese nivel.</span><span class="sxs-lookup"><span data-stu-id="2f261-172">Starting with Windows 7, Windows will choose the highest version GUID in the manifest up to the running Windows version, and give the app support at that level.</span></span> <span data-ttu-id="2f261-173">Para comprobar que la aplicación funciona con la nueva sección compatibilidad del manifiesto de la aplicación:</span><span class="sxs-lookup"><span data-stu-id="2f261-173">To verify that the app works with the new app manifest compatibility section:</span></span>

1.  <span data-ttu-id="2f261-174">Pruebe la aplicación con la nueva sección de compatibilidad y el ID. de Supported = {4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} para asegurarse de que la aplicación funciona correctamente con el comportamiento más reciente de Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2f261-174">Test the app with the new compatibility section and SupportedOS ID = { 4a2f28e3-53b9-4441-ba9c-d69d4a4a6e38} to ensure that the app works properly using the latest Windows 8 behavior.</span></span>
2.  <span data-ttu-id="2f261-175">Pruebe la aplicación con la nueva sección de compatibilidad y el ID. de Supported = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} para asegurarse de que la aplicación funciona correctamente con el comportamiento de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2f261-175">Test the app with the new compatibility section and SupportedOS ID = {35138b9a-5d96-4fbd-8e2d-a2440225f93a} to ensure that the app works properly using the Windows 7 behavior.</span></span>
3.  <span data-ttu-id="2f261-176">Pruebe la aplicación con la nueva sección de compatibilidad y el ID. de Supported = {e2011457-1546-43c5-a5fe-008deee3d3f0} para asegurarse de que la aplicación funciona correctamente con el comportamiento de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2f261-176">Test the app with the new compatibility section and SupportedOS ID = {e2011457-1546-43c5-a5fe-008deee3d3f0} to ensure that the app works properly using the Windows Vista behavior.</span></span>

## <a name="resources"></a><span data-ttu-id="2f261-177">Recursos</span><span class="sxs-lookup"><span data-stu-id="2f261-177">Resources</span></span>

-   [<span data-ttu-id="2f261-178">QueryActCtxW función)</span><span class="sxs-lookup"><span data-stu-id="2f261-178">QueryActCtxW Function</span></span>](../sbscs/application-manifests.md)
-   <span data-ttu-id="2f261-179">[Manifiesto de UAC](/previous-versions/bb756929(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="2f261-179">[UAC manifest](/previous-versions/bb756929(v=msdn.10))</span></span>
-   [<span data-ttu-id="2f261-180">Manifiestos de aplicación para aplicaciones Windows</span><span class="sxs-lookup"><span data-stu-id="2f261-180">Application Manifests for Windows Applications</span></span>](../sbscs/application-manifests.md)
-   [<span data-ttu-id="2f261-181">Administrador de ventanas de escritorio (DWM)</span><span class="sxs-lookup"><span data-stu-id="2f261-181">Desktop Window Manager (DWM)</span></span>](../dwm/dwm-overview.md)
-   [<span data-ttu-id="2f261-182">Actualización de coincidencia de contexto</span><span class="sxs-lookup"><span data-stu-id="2f261-182">Context Mismatch Update</span></span>](https://support.microsoft.com/kb/978637)
-   <span data-ttu-id="2f261-183">[Asistente para la compatibilidad de programas](/previous-versions/bb756937(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="2f261-183">[Program Compatibility Assistant](/previous-versions/bb756937(v=msdn.10))</span></span>

 

 