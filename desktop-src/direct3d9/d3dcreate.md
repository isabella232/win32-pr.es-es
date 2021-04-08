---
description: Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.
ms.assetid: 91387a2d-3927-4285-a09b-9ce247e6bfdd
title: D3DCREATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14de345d6cb6d164ee5cd3067e1f38ff66d9795d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000701"
---
# <a name="d3dcreate"></a><span data-ttu-id="29f4c-103">D3DCREATE</span><span class="sxs-lookup"><span data-stu-id="29f4c-103">D3DCREATE</span></span>

<span data-ttu-id="29f4c-104">Combinación de una o varias marcas que controlan el comportamiento de creación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29f4c-104">A combination of one or more flags that control the device create behavior.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29f4c-105">#define</span><span class="sxs-lookup"><span data-stu-id="29f4c-105">#define</span></span></td>
<td><span data-ttu-id="29f4c-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="29f4c-106">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-107">D3DCREATE_ADAPTERGROUP_DEVICE</span><span class="sxs-lookup"><span data-stu-id="29f4c-107">D3DCREATE_ADAPTERGROUP_DEVICE</span></span></td>
<td><span data-ttu-id="29f4c-108">La aplicación pide al dispositivo que controle todos los dispositivos que posee este adaptador maestro.</span><span class="sxs-lookup"><span data-stu-id="29f4c-108">Application asks the device to drive all the heads that this master adapter owns.</span></span> <span data-ttu-id="29f4c-109">La marca no es válida en los adaptadores no maestros.</span><span class="sxs-lookup"><span data-stu-id="29f4c-109">The flag is illegal on nonmaster adapters.</span></span> <span data-ttu-id="29f4c-110">Si se establece esta marca, los parámetros de presentación que se pasan a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> deben apuntar a una matriz de <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="29f4c-110">If this flag is set, the presentation parameters passed to <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> should point to an array of <a href="d3dpresent-parameters.md"><strong>D3DPRESENT_PARAMETERS</strong></a>.</span></span> <span data-ttu-id="29f4c-111">El número de elementos de <strong>D3DPRESENT_PARAMETERS</strong> debe ser igual al número de adaptadores definido por el miembro NumberOfAdaptersInGroup de la estructura <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="29f4c-111">The number of elements in <strong>D3DPRESENT_PARAMETERS</strong> should equal the number of adapters defined by the NumberOfAdaptersInGroup member of the <a href="/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a> structure.</span></span> <span data-ttu-id="29f4c-112">El tiempo de ejecución de DirectX asignará cada elemento a cada encabezado en el orden numérico especificado por el miembro AdapterOrdinalInGroup de <strong>D3DCAPS9</strong>.</span><span class="sxs-lookup"><span data-stu-id="29f4c-112">The DirectX runtime will assign each element to each head in the numerical order specified by the AdapterOrdinalInGroup member of <strong>D3DCAPS9</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="29f4c-113">D3DCREATE_DISABLE_DRIVER_MANAGEMENT</span></span></td>
<td><span data-ttu-id="29f4c-114">Direct3D administrará los recursos en lugar del controlador.</span><span class="sxs-lookup"><span data-stu-id="29f4c-114">Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="29f4c-115">No se producirá un error en las llamadas de Direct3D para los errores de recursos, como la memoria de vídeo insuficiente.</span><span class="sxs-lookup"><span data-stu-id="29f4c-115">Direct3D calls will not fail for resource errors such as insufficient video memory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span><span class="sxs-lookup"><span data-stu-id="29f4c-116">D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX</span></span></td>
<td><span data-ttu-id="29f4c-117">Como D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D administrará los recursos en lugar del controlador.</span><span class="sxs-lookup"><span data-stu-id="29f4c-117">Like D3DCREATE_DISABLE_DRIVER_MANAGEMENT, Direct3D will manage resources instead of the driver.</span></span> <span data-ttu-id="29f4c-118">A diferencia de D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX devolverá errores para condiciones como la memoria de vídeo insuficiente.</span><span class="sxs-lookup"><span data-stu-id="29f4c-118">Unlike D3DCREATE_DISABLE_DRIVER_MANAGEMENT, D3DCREATE_DISABLE_DRIVER_MANAGEMENT_EX will return errors for conditions such as insufficient video memory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-119">D3DCREATE_DISABLE_PRINTSCREEN</span><span class="sxs-lookup"><span data-stu-id="29f4c-119">D3DCREATE_DISABLE_PRINTSCREEN</span></span></td>
<td><span data-ttu-id="29f4c-120">Hace que el tiempo de ejecución no registre las teclas de PrintScreen, Ctrl-Printscreen y Alt-Printscreen para capturar el escritorio o el contenido de la ventana.</span><span class="sxs-lookup"><span data-stu-id="29f4c-120">Causes the runtime not register hotkeys for Printscreen, Ctrl-Printscreen and Alt-Printscreen to capture the desktop or window content.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29f4c-121">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="29f4c-121">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="29f4c-122">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="29f4c-122">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-123">D3DCREATE_DISABLE_PSGP_THREADING</span><span class="sxs-lookup"><span data-stu-id="29f4c-123">D3DCREATE_DISABLE_PSGP_THREADING</span></span></td>
<td><span data-ttu-id="29f4c-124">Restrinja el cálculo al subproceso de la aplicación principal.</span><span class="sxs-lookup"><span data-stu-id="29f4c-124">Restrict computation to the main application thread.</span></span> <span data-ttu-id="29f4c-125">Si no se establece la marca, el runtime puede realizar el procesamiento de vértices de software y otros cálculos en el subproceso de trabajo para mejorar el rendimiento en sistemas de varios procesadores.</span><span class="sxs-lookup"><span data-stu-id="29f4c-125">If the flag is not set, the runtime may perform software vertex processing and other computations in worker thread to improve performance on multi-processor systems.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29f4c-126">Diferencias entre Windows XP y Windows Vista:</span><span class="sxs-lookup"><span data-stu-id="29f4c-126">Differences between Windows XP and Windows Vista:</span></span><br/> <span data-ttu-id="29f4c-127">Esta marca está disponible en Windows Vista, Windows Server 2008 y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="29f4c-127">This flag is available on Windows Vista, Windows Server 2008, and Windows 7.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-128">D3DCREATE_ENABLE_PRESENTSTATS</span><span class="sxs-lookup"><span data-stu-id="29f4c-128">D3DCREATE_ENABLE_PRESENTSTATS</span></span></td>
<td><span data-ttu-id="29f4c-129">Habilita la recopilación de estadísticas presentes en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29f4c-129">Enables the gathering of present statistics on the device.</span></span> <span data-ttu-id="29f4c-130">Las llamadas a <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> devolverán datos válidos.</span><span class="sxs-lookup"><span data-stu-id="29f4c-130">Calls to <a href="/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)"><strong>GetPresentStatistics</strong></a> will return valid data.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29f4c-131">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="29f4c-131">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="29f4c-132">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="29f4c-132">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-133">D3DCREATE_FPU_PRESERVE</span><span class="sxs-lookup"><span data-stu-id="29f4c-133">D3DCREATE_FPU_PRESERVE</span></span></td>
<td><span data-ttu-id="29f4c-134">Establezca la precisión para los cálculos de punto flotante de Direct3D en la precisión utilizada por el subproceso que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="29f4c-134">Set the precision for Direct3D floating-point calculations to the precision used by the calling thread.</span></span> <span data-ttu-id="29f4c-135">Si no se especifica esta marca, Direct3D toma como valor predeterminado el modo de redondeo de precisión sencilla por dos motivos:</span><span class="sxs-lookup"><span data-stu-id="29f4c-135">If you do not specify this flag, Direct3D defaults to single-precision round-to-nearest mode for two reasons:</span></span>
<ul>
<li><span data-ttu-id="29f4c-136">El modo de doble precisión reducirá el rendimiento de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="29f4c-136">Double-precision mode will reduce Direct3D performance.</span></span></li>
<li><span data-ttu-id="29f4c-137">Algunas partes de Direct3D suponen que las excepciones de la unidad de punto flotante se enmascaran; al desenmascarar estas excepciones, se puede producir un comportamiento indefinido.</span><span class="sxs-lookup"><span data-stu-id="29f4c-137">Portions of Direct3D assume floating-point unit exceptions are masked; unmasking these exceptions may result in undefined behavior.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="29f4c-138">D3DCREATE_HARDWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="29f4c-139">Especifica el procesamiento de vértices de hardware.</span><span class="sxs-lookup"><span data-stu-id="29f4c-139">Specifies hardware vertex processing.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-140">D3DCREATE_MIXED_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="29f4c-140">D3DCREATE_MIXED_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="29f4c-141">Especifica el procesamiento de vértices mixtos (tanto de software como de hardware).</span><span class="sxs-lookup"><span data-stu-id="29f4c-141">Specifies mixed (both software and hardware) vertex processing.</span></span> <span data-ttu-id="29f4c-142">En Windows 10, versión 1607 y versiones posteriores, no se recomienda el uso de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="29f4c-142">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="29f4c-143">Vea D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="29f4c-143">See D3DCREATE_SOFTWARE_VERTEXPROCESSING.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span><span class="sxs-lookup"><span data-stu-id="29f4c-144">D3DCREATE_SOFTWARE_VERTEXPROCESSING</span></span></td>
<td><span data-ttu-id="29f4c-145">Especifica el procesamiento de vértices de software.</span><span class="sxs-lookup"><span data-stu-id="29f4c-145">Specifies software vertex processing.</span></span> <span data-ttu-id="29f4c-146">En Windows 10, versión 1607 y versiones posteriores, no se recomienda el uso de esta configuración.</span><span class="sxs-lookup"><span data-stu-id="29f4c-146">For Windows 10, version 1607 and later, use of this setting is not recommended.</span></span> <span data-ttu-id="29f4c-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span><span class="sxs-lookup"><span data-stu-id="29f4c-147">Use D3DCREATE_HARDWARE_VERTEXPROCESSING.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="29f4c-148">A menos que no esté disponible el procesamiento de vértices de hardware, no se recomienda el uso del procesamiento de vértices de software en Windows 10, versión 1607 (y versiones posteriores), ya que la eficacia del procesamiento de vértices de software se redujo considerablemente al mejorar la seguridad de la implementación.</span><span class="sxs-lookup"><span data-stu-id="29f4c-148">Unless hardware vertex processing is not available, the usage of software vertex processing is not recommended in Windows 10, version 1607 (and later versions) because the efficiency of software vertex processing was significantly reduced while improving the security of the implementation.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-149">D3DCREATE_MULTITHREADED</span><span class="sxs-lookup"><span data-stu-id="29f4c-149">D3DCREATE_MULTITHREADED</span></span></td>
<td><span data-ttu-id="29f4c-150">Indica que la aplicación solicita a Direct3D que sea segura para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="29f4c-150">Indicates that the application requests Direct3D to be multithread safe.</span></span> <span data-ttu-id="29f4c-151">Esto hace que un subproceso de Direct3D tome posesión de su <a href="/windows/desktop/Sync/critical-section-objects">sección crítica</a> global con mayor frecuencia, lo que puede reducir el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="29f4c-151">This makes a Direct3D thread take ownership of its global <a href="/windows/desktop/Sync/critical-section-objects">critical section</a> more frequently, which can degrade performance.</span></span> <span data-ttu-id="29f4c-152">Si una aplicación procesa los mensajes de ventana en un subproceso mientras realiza llamadas a la API de Direct3D en otro, la aplicación debe usar esta marca al crear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="29f4c-152">If an application processes window messages in one thread while making Direct3D API calls in another, the application must use this flag when creating the device.</span></span> <span data-ttu-id="29f4c-153">Esta ventana también se debe destruir antes de descargar d3d9.dll.</span><span class="sxs-lookup"><span data-stu-id="29f4c-153">This window must also be destroyed before unloading d3d9.dll.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-154">D3DCREATE_NOWINDOWCHANGES</span><span class="sxs-lookup"><span data-stu-id="29f4c-154">D3DCREATE_NOWINDOWCHANGES</span></span></td>
<td><span data-ttu-id="29f4c-155">Indica que Direct3D no debe modificar la ventana de foco de ningún modo.</span><span class="sxs-lookup"><span data-stu-id="29f4c-155">Indicates that Direct3D must not alter the focus window in any way.</span></span>
<div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="29f4c-156">Si se establece esta marca, la aplicación debe admitir todos los eventos de administración de foco, como ALT + TAB y eventos de clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="29f4c-156">If this flag is set, the application must fully support all focus management events, such as ALT+TAB and mouse click events.</span></span>
</blockquote>
</div>
<div>
 
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="29f4c-157">D3DCREATE_PUREDEVICE</span><span class="sxs-lookup"><span data-stu-id="29f4c-157">D3DCREATE_PUREDEVICE</span></span></td>
<td><span data-ttu-id="29f4c-158">Especifica que Direct3D no admite llamadas Get \* para cualquier elemento que se pueda almacenar en bloques de estado.</span><span class="sxs-lookup"><span data-stu-id="29f4c-158">Specifies that Direct3D does not support Get\* calls for anything that can be stored in state blocks.</span></span> <span data-ttu-id="29f4c-159">También indica a Direct3D que no proporcione ningún servicio de emulación para el procesamiento de vértices.</span><span class="sxs-lookup"><span data-stu-id="29f4c-159">It also tells Direct3D not to provide any emulation services for vertex processing.</span></span> <span data-ttu-id="29f4c-160">Esto significa que si el dispositivo no admite el procesamiento de vértices, la aplicación solo puede usar vértices posteriores transformados.</span><span class="sxs-lookup"><span data-stu-id="29f4c-160">This means that if the device does not support vertex processing, then the application can use only post-transformed vertices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="29f4c-161">D3DCREATE_SCREENSAVER</span><span class="sxs-lookup"><span data-stu-id="29f4c-161">D3DCREATE_SCREENSAVER</span></span></td>
<td><span data-ttu-id="29f4c-162">Permite protectores de pantalla durante una aplicación de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29f4c-162">Allows screensavers during a fullscreen application.</span></span> <span data-ttu-id="29f4c-163">Sin esta marca, Direct3D deshabilitará los protectores de pantalla mientras la aplicación que realiza la llamada sea pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="29f4c-163">Without this flag, Direct3D will disable screensavers for as long as the calling application is fullscreen.</span></span> <span data-ttu-id="29f4c-164">Si la aplicación que realiza la llamada ya es un protector de la aplicación, esta marca no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="29f4c-164">If the calling application is already a screensaver, this flag has no effect.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="29f4c-165">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="29f4c-165">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="29f4c-166">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="29f4c-166">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="29f4c-167">D3DCREATE \_ hardware \_ VERTEXPROCESSING, D3DCREATE \_ Mixed \_ VERTEXPROCESSING y D3DCREATE \_ software \_ VERTEXPROCESSING son marcas mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="29f4c-167">D3DCREATE\_HARDWARE\_VERTEXPROCESSING, D3DCREATE\_MIXED\_VERTEXPROCESSING, and D3DCREATE\_SOFTWARE\_VERTEXPROCESSING are mutually exclusive flags.</span></span> <span data-ttu-id="29f4c-168">Se debe especificar al menos una de estas marcas de procesamiento de vértices al llamar a [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span><span class="sxs-lookup"><span data-stu-id="29f4c-168">At least one of these vertex processing flags must be specified when calling [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice).</span></span>

## <a name="constant-information"></a><span data-ttu-id="29f4c-169">Información constante</span><span class="sxs-lookup"><span data-stu-id="29f4c-169">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="29f4c-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29f4c-170">Header</span></span>                   | <span data-ttu-id="29f4c-171">D3D9. h</span><span class="sxs-lookup"><span data-stu-id="29f4c-171">D3D9.h</span></span>     |
| <span data-ttu-id="29f4c-172">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="29f4c-172">Minimum operating system</span></span> | <span data-ttu-id="29f4c-173">Windows 98</span><span class="sxs-lookup"><span data-stu-id="29f4c-173">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="29f4c-174">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="29f4c-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29f4c-175">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="29f4c-175">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
