---
description: Constantes usadas por \_ los parámetros D3DPRESENT.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3b7fe950a6fe09425aa47a79ce8f803eb81298
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705287"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="ce68b-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="ce68b-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="ce68b-104">Constantes usadas por [**\_ los parámetros D3DPRESENT**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="ce68b-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-105">#define</span><span class="sxs-lookup"><span data-stu-id="ce68b-105">#define</span></span></td>
<td><span data-ttu-id="ce68b-106">Value</span><span class="sxs-lookup"><span data-stu-id="ce68b-106">Value</span></span></td>
<td><span data-ttu-id="ce68b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ce68b-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce68b-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="ce68b-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="ce68b-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ce68b-109">0x00000004</span></span></td>
<td><span data-ttu-id="ce68b-110">Recortar un blit de <a href="/windows/desktop/api"><strong>presentación</strong></a> de ventana en el área de cliente de la ventana, dentro del área de pantalla monitor del adaptador de vídeo que creó el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ce68b-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="ce68b-111">D3DPRESENTFLAG_DEVICECLIP no es válido con D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="ce68b-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce68b-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="ce68b-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="ce68b-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ce68b-113">0x00000002</span></span></td>
<td><span data-ttu-id="ce68b-114">Establezca esta marca cuando se cree el dispositivo o la cadena de intercambio para habilitar la descartación del búfer z.</span><span class="sxs-lookup"><span data-stu-id="ce68b-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="ce68b-115">Si se establece esta marca, el contenido del búfer de estarcido de profundidad no será válido después de llamar a <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente.</span><span class="sxs-lookup"><span data-stu-id="ce68b-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="ce68b-116">Descartar los datos del búfer z puede aumentar el rendimiento y depende del controlador.</span><span class="sxs-lookup"><span data-stu-id="ce68b-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="ce68b-117">El tiempo de ejecución de depuración exigirá el descarting al borrar el búfer z en algún valor constante después de llamar a <a href="/windows/desktop/api"><strong>present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente.</span><span class="sxs-lookup"><span data-stu-id="ce68b-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="ce68b-118">Descartar los datos del búfer z no es válido para todos los formatos de bloqueos, D3DFMT_D16_LOCKABLE y D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="ce68b-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="ce68b-119">Cualquier uso de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> que especifique un formato de bloqueable y un descartado de búfer z producirá un error.</span><span class="sxs-lookup"><span data-stu-id="ce68b-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="ce68b-120">Para obtener más información acerca de los formatos, vea <a href="d3dformat.md">D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="ce68b-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce68b-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="ce68b-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="ce68b-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ce68b-122">0x00000001</span></span></td>
<td><span data-ttu-id="ce68b-123">Establezca esta marca si la aplicación requiere la capacidad de bloquear el búfer de reserva directamente.</span><span class="sxs-lookup"><span data-stu-id="ce68b-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="ce68b-124">Tenga en cuenta que los búferes de reserva no se pueden bloquear a menos que la aplicación especifique D3DPRESENTFLAG_LOCKABLE_BACKBUFFER al llamar a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>RESET</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="ce68b-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="ce68b-125">Los búferes de reserva que se bloquean incurren en un costo de rendimiento en algunas configuraciones de hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="ce68b-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="ce68b-126">La realización de una operación de bloqueo (o el uso de <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> para escribir) en el búfer de reserva de bloqueos reduce el rendimiento en muchas tarjetas.</span><span class="sxs-lookup"><span data-stu-id="ce68b-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="ce68b-127">En este caso, considere la posibilidad de usar triángulos con textura para trasladar datos al búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="ce68b-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-128">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-129">En Direct3D9Ex no se puede establecer esta marca si el valor de D3DSWAPEFFECT es D3DSWAPEFFECT_FLIPEX, ya que el modelo de volteo permite al Administrador de ventanas de escritorio tener acceso al búfer de reserva de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="ce68b-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="ce68b-130">Una superficie compartida entre procesos no debe estar bloqueada.</span><span class="sxs-lookup"><span data-stu-id="ce68b-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce68b-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="ce68b-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="ce68b-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ce68b-132">0x00000020</span></span></td>
<td><span data-ttu-id="ce68b-133">Los monitores girados se controlan automáticamente con una copia giratoria durante la presentación, lo que no es muy eficaz.</span><span class="sxs-lookup"><span data-stu-id="ce68b-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="ce68b-134">Esta marca significa que la aplicación realizará su propia rotación de pantalla.</span><span class="sxs-lookup"><span data-stu-id="ce68b-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-135">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-136">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="ce68b-137">Las aplicaciones pueden lograr su propia rotación posiblemente mediante una matriz de vistas girada.</span><span class="sxs-lookup"><span data-stu-id="ce68b-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="ce68b-138">Los métodos <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> y <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> deben usarse para buscar el valor de rotación actual.</span><span class="sxs-lookup"><span data-stu-id="ce68b-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="ce68b-139">Los parámetros de ancho y alto del búfer de reserva de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> y <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> deben usar la orientación horizontal, mientras que la estructura del modo de presentación de pantalla completa debe ser la misma que la devuelta desde <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (es decir, el ancho y el alto se intercambian cuando giran 90 y 270 grados).</span><span class="sxs-lookup"><span data-stu-id="ce68b-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="ce68b-140">Cuando se usa el bloqueo en destinos de representación girados, las suposiciones de la esquina superior izquierda ya no tienen el valor true, el destino de representación SURFACE_DESC permanecerá horizontal (como lo implican los parámetros de creación) y la ventana de GDI, las coordenadas del mouse, y tal necesidad de traducirse correctamente cuando se usa con el destino de representación y la escena de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="ce68b-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce68b-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="ce68b-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="ce68b-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ce68b-142">0x00000040</span></span></td>
<td><span data-ttu-id="ce68b-143">Use esta marca para especificar cualquier modo de presentación sin formato enumerado por el adaptador de pantalla, aunque Direct3D haya indicado que el modo no es válido.</span><span class="sxs-lookup"><span data-stu-id="ce68b-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="ce68b-144">La aplicación debe implementar esto de forma sólida en caso de que el modo deseado realmente no sea válido.</span><span class="sxs-lookup"><span data-stu-id="ce68b-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-145">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-146">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce68b-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="ce68b-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="ce68b-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ce68b-148">0x00000010</span></span></td>
<td><span data-ttu-id="ce68b-149">Esta es una sugerencia para el controlador que los búferes de reserva contendrán datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ce68b-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce68b-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="ce68b-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="ce68b-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ce68b-151">0x00000080</span></span></td>
<td><span data-ttu-id="ce68b-152">Especifica si la superposición es RGB de intervalo completo o de intervalo limitado.</span><span class="sxs-lookup"><span data-stu-id="ce68b-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="ce68b-153">Al establecer esta marca, se indica RGB de intervalo limitado.</span><span class="sxs-lookup"><span data-stu-id="ce68b-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="ce68b-154">En el intervalo de RGB limitado, el intervalo RGB se comprime de forma que 16:16:16 sea negro y 235:235:235 sea blanco.</span><span class="sxs-lookup"><span data-stu-id="ce68b-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-155">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-156">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce68b-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="ce68b-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="ce68b-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ce68b-158">0x00000100</span></span></td>
<td><span data-ttu-id="ce68b-159">Especifica si la superposición es BT. 601 o BT. 709.</span><span class="sxs-lookup"><span data-stu-id="ce68b-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="ce68b-160">La configuración de esta marca indica BT. 709, para TV de alta definición (HDTV).</span><span class="sxs-lookup"><span data-stu-id="ce68b-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-161">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-162">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce68b-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="ce68b-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="ce68b-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ce68b-164">0x00000200</span></span></td>
<td><span data-ttu-id="ce68b-165">Especifica si la superposición es el YCbCr convencional o la extensión YCbCr extendida (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="ce68b-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="ce68b-166">Al establecer esta marca, se indica el YCbCr extendido (xvYCC).</span><span class="sxs-lookup"><span data-stu-id="ce68b-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-167">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-168">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ce68b-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="ce68b-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="ce68b-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="ce68b-170">0x00000400</span></span></td>
<td><span data-ttu-id="ce68b-171">Al establecer esta marca, se indica que intercambio contiene contenido protegido y hace que el tiempo de ejecución restrinja automáticamente el acceso a intercambio para que solo el administrador de Windows de escritorio (DWM) pueda usar intercambio.</span><span class="sxs-lookup"><span data-stu-id="ce68b-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-172">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-173">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ce68b-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="ce68b-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="ce68b-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="ce68b-175">0x00000800</span></span></td>
<td><span data-ttu-id="ce68b-176">Al establecer esta marca, se indica que el controlador debe restringir el acceso a los recursos compartidos que se crean para la interacción de DWM.</span><span class="sxs-lookup"><span data-stu-id="ce68b-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="ce68b-177">El autor de la llamada debe crear un canal autenticado con el controlador.</span><span class="sxs-lookup"><span data-stu-id="ce68b-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="ce68b-178">A continuación, el controlador debe permitir el acceso a los procesos que intenten abrir esos recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="ce68b-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ce68b-179">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="ce68b-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="ce68b-180">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="ce68b-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="ce68b-181">[**\_ Los parámetros D3DPRESENT**](d3dpresent-parameters.md)usan estas constantes.</span><span class="sxs-lookup"><span data-stu-id="ce68b-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="ce68b-182">Información constante</span><span class="sxs-lookup"><span data-stu-id="ce68b-182">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="ce68b-183">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ce68b-183">Header</span></span>                   | <span data-ttu-id="ce68b-184">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="ce68b-184">d3d9types.h</span></span> |
| <span data-ttu-id="ce68b-185">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="ce68b-185">Minimum operating system</span></span> | <span data-ttu-id="ce68b-186">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ce68b-186">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ce68b-187">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ce68b-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce68b-188">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="ce68b-188">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




