---
description: Constantes usadas por D3DPRESENT \_ PARAMETERS.
ms.assetid: 1294171e-b3f6-4264-8411-b69427cefe7b
title: D3DPRESENTFLAG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 578d41119980719e69b9eb0e502c025414018f73
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343100"
---
# <a name="d3dpresentflag"></a><span data-ttu-id="c27f8-103">D3DPRESENTFLAG</span><span class="sxs-lookup"><span data-stu-id="c27f8-103">D3DPRESENTFLAG</span></span>

<span data-ttu-id="c27f8-104">Constantes utilizadas por [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c27f8-104">Constants used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-105">#Definir</span><span class="sxs-lookup"><span data-stu-id="c27f8-105">#define</span></span></td>
<td><span data-ttu-id="c27f8-106">Valor</span><span class="sxs-lookup"><span data-stu-id="c27f8-106">Value</span></span></td>
<td><span data-ttu-id="c27f8-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="c27f8-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c27f8-108">D3DPRESENTFLAG_DEVICECLIP</span><span class="sxs-lookup"><span data-stu-id="c27f8-108">D3DPRESENTFLAG_DEVICECLIP</span></span></td>
<td><span data-ttu-id="c27f8-109">0x00000004</span><span class="sxs-lookup"><span data-stu-id="c27f8-109">0x00000004</span></span></td>
<td><span data-ttu-id="c27f8-110">Recorte una ventana <a href="/windows/desktop/api"><strong>Presente</strong></a> blit en el área de cliente de la ventana, dentro del área de pantalla del monitor del adaptador de vídeo que creó el dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c27f8-110">Clip a windowed <a href="/windows/desktop/api"><strong>Present</strong></a> blit into the window client area, within the monitor screen area of the video adapter that created the Direct3D device.</span></span> <span data-ttu-id="c27f8-111">D3DPRESENTFLAG_DEVICECLIP no es válido con D3DSWAPEFFECT_FLIPEX.</span><span class="sxs-lookup"><span data-stu-id="c27f8-111">D3DPRESENTFLAG_DEVICECLIP is not valid with D3DSWAPEFFECT_FLIPEX.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c27f8-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span><span class="sxs-lookup"><span data-stu-id="c27f8-112">D3DPRESENTFLAG_DISCARD_DEPTHSTENCIL</span></span></td>
<td><span data-ttu-id="c27f8-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="c27f8-113">0x00000002</span></span></td>
<td><span data-ttu-id="c27f8-114">Establezca esta marca cuando se cree el dispositivo o la cadena de intercambio para habilitar el descarte de búfer z.</span><span class="sxs-lookup"><span data-stu-id="c27f8-114">Set this flag when the device or swap chain is created to enable z-buffer discarding.</span></span> <span data-ttu-id="c27f8-115">Si se establece esta marca, el contenido del búfer de galería de símbolos de profundidad no será válido después de llamar a <a href="/windows/desktop/api"><strong>Present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente.</span><span class="sxs-lookup"><span data-stu-id="c27f8-115">If this flag is set, the contents of the depth stencil buffer will be invalid after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span> <span data-ttu-id="c27f8-116">Descartar los datos del búfer z puede aumentar el rendimiento y depende del controlador.</span><span class="sxs-lookup"><span data-stu-id="c27f8-116">Discarding z-buffer data can increase performance and is driver dependent.</span></span> <span data-ttu-id="c27f8-117">El tiempo de ejecución de depuración aplicará el descarte borrando el búfer z en algún valor constante después de llamar a <a href="/windows/desktop/api"><strong>Present</strong></a>o <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> con una superficie de profundidad diferente.</span><span class="sxs-lookup"><span data-stu-id="c27f8-117">The debug runtime will enforce discarding by clearing the z-buffer to some constant value after calling either <a href="/windows/desktop/api"><strong>Present</strong></a>, or <a href="/windows/desktop/api"><strong>SetDepthStencilSurface</strong></a> with a different depth surface.</span></span><br/> <span data-ttu-id="c27f8-118">Descartar los datos del búfer z no es posible para todos los formatos que se pueden bloquear, D3DFMT_D16_LOCKABLE y D3DFMT_D32F_LOCKABLE.</span><span class="sxs-lookup"><span data-stu-id="c27f8-118">Discarding z-buffer data is illegal for all lockable formats, D3DFMT_D16_LOCKABLE and D3DFMT_D32F_LOCKABLE.</span></span> <span data-ttu-id="c27f8-119">Se producirá un error en cualquier uso <a href="/windows/desktop/api"><strong>de CreateDevice</strong></a> que especifique un formato que se puede bloquear y el descarte del búfer z.</span><span class="sxs-lookup"><span data-stu-id="c27f8-119">Any use of <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> specifying a lockable format and z-buffer discarding will fail.</span></span> <span data-ttu-id="c27f8-120">Para obtener más información sobre los formatos, <a href="d3dformat.md">vea D3DFORMAT</a>.</span><span class="sxs-lookup"><span data-stu-id="c27f8-120">For more information about formats, see <a href="d3dformat.md">D3DFORMAT</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c27f8-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span><span class="sxs-lookup"><span data-stu-id="c27f8-121">D3DPRESENTFLAG_LOCKABLE_BACKBUFFER</span></span></td>
<td><span data-ttu-id="c27f8-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="c27f8-122">0x00000001</span></span></td>
<td><span data-ttu-id="c27f8-123">Establezca esta marca si la aplicación requiere la capacidad de bloquear el búfer de reserva directamente.</span><span class="sxs-lookup"><span data-stu-id="c27f8-123">Set this flag if the application requires the ability to lock the back buffer directly.</span></span> <span data-ttu-id="c27f8-124">Tenga en cuenta que los búferes de reserva no se pueden bloquear a menos que la aplicación D3DPRESENTFLAG_LOCKABLE_BACKBUFFER al llamar a <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> o <a href="/windows/desktop/api"><strong>Restablecer</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c27f8-124">Note that back buffers are not lockable unless the application specifies D3DPRESENTFLAG_LOCKABLE_BACKBUFFER when calling <a href="/windows/desktop/api"><strong>CreateDevice</strong></a> or <a href="/windows/desktop/api"><strong>Reset</strong></a>.</span></span> <span data-ttu-id="c27f8-125">Los búferes de reserva que se pueden bloquear incurren en un costo de rendimiento en algunas configuraciones de hardware gráfico.</span><span class="sxs-lookup"><span data-stu-id="c27f8-125">Lockable back buffers incur a performance cost on some graphics hardware configurations.</span></span> <span data-ttu-id="c27f8-126">La realización de una operación de bloqueo (o el uso <a href="/windows/desktop/api"><strong>de UpdateSurface</strong></a> para escribir) en el búfer de reserva que se puede bloquear reduce el rendimiento en muchas tarjetas.</span><span class="sxs-lookup"><span data-stu-id="c27f8-126">Performing a lock operation (or using <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> to write) on the lockable back buffer decreases performance on many cards.</span></span> <span data-ttu-id="c27f8-127">En este caso, considere la posibilidad de usar triángulos con textura para mover datos al búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="c27f8-127">In this case, consider using textured triangles to move data to the back buffer.</span></span><br/> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-128">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-129">En Direct3D9Ex, esta marca no se puede establecer si D3DSWAPEFFECT es D3DSWAPEFFECT_FLIPEX, ya que el modelo de volteo permite que el Administrador de ventanas de escritorio acceda al búfer de reserva de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="c27f8-129">In Direct3D9Ex this flag cannot be set if the D3DSWAPEFFECT is D3DSWAPEFFECT_FLIPEX, since the flip model enables the Desktop Window Manager to access an application's back buffer.</span></span> <span data-ttu-id="c27f8-130">No se debe bloquear una superficie compartida entre procesos.</span><span class="sxs-lookup"><span data-stu-id="c27f8-130">A cross-process shared-surface should not be locked.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c27f8-131">D3DPRESENTFLAG_NOAUTOROTATE</span><span class="sxs-lookup"><span data-stu-id="c27f8-131">D3DPRESENTFLAG_NOAUTOROTATE</span></span></td>
<td><span data-ttu-id="c27f8-132">0x00000020</span><span class="sxs-lookup"><span data-stu-id="c27f8-132">0x00000020</span></span></td>
<td><span data-ttu-id="c27f8-133">Los monitores girados se controlan automáticamente con una copia rotativa durante la presentación, lo que no es muy eficaz.</span><span class="sxs-lookup"><span data-stu-id="c27f8-133">Rotated monitors are handled automatically with a rotating copy during presentation, which is not very efficient.</span></span> <span data-ttu-id="c27f8-134">Esta marca significa que la aplicación realizará su propia rotación de pantalla.</span><span class="sxs-lookup"><span data-stu-id="c27f8-134">This flag means the application will perform it's own display rotation.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-135">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-135">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-136">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-136">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="c27f8-137">Las aplicaciones pueden lograr su propia rotación posiblemente mediante una matriz de vista girada.</span><span class="sxs-lookup"><span data-stu-id="c27f8-137">Applications can achieve their own rotation possibly by using a rotated view matrix.</span></span> <span data-ttu-id="c27f8-138">Los <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>métodos GetDisplayModeEx</strong></a> <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>y GetAdapterDisplayModeEx</strong></a> deben usarse para buscar la configuración de rotación actual.</span><span class="sxs-lookup"><span data-stu-id="c27f8-138">The methods <a href="/windows/desktop/api/D3D9/nf-d3d9-idirect3dswapchain9ex-getdisplaymodeex"><strong>GetDisplayModeEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-getadapterdisplaymodeex"><strong>GetAdapterDisplayModeEx</strong></a> should be used to to find the current rotation setting.</span></span> <span data-ttu-id="c27f8-139">Los parámetros Ancho y Alto del búfer de reserva de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> y <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> deben usar orientación horizontal, mientras que la estructura del modo de presentación de pantalla completa debe ser la misma que la que se devuelve de <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (es decir, el ancho y el alto se intercambian cuando se giran 90 y 270 grados).</span><span class="sxs-lookup"><span data-stu-id="c27f8-139">The backbuffer Width and Height parameters in <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex"><strong>CreateDeviceEx</strong></a> and <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex"><strong>ResetEx</strong></a> must be use landscape orientation, while the fullscreen display mode structure should be the same as what is returned from <a href="/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-enumadaptermodesex"><strong>EnumAdapterModesEx</strong></a> (i.e. Width and Height are swapped when rotated 90 and 270 degrees).</span></span></p>
<p><span data-ttu-id="c27f8-140">Cuando se usa Bloquear en destinos de representación girados, las suposiciones de la esquina superior izquierda ya no son verdaderas, el destino de representación SURFACE_DESC permanecerá horizontal (como implícito en los parámetros de creación) y la ventana GDI, las coordenadas del mouse y tales deben traducirse correctamente cuando se usen con el destino y la escena de representación de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c27f8-140">When using Lock on rotated render targets, upper-left corner assumptions no longer hold true, the render target SURFACE_DESC will remain landscape (as implied by the creation parameters), and GDI window, mouse coordinates, and such need to be properly translated when used with the Direct3D render target and scene.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c27f8-141">D3DPRESENTFLAG_UNPRUNEDMODE</span><span class="sxs-lookup"><span data-stu-id="c27f8-141">D3DPRESENTFLAG_UNPRUNEDMODE</span></span></td>
<td><span data-ttu-id="c27f8-142">0x00000040</span><span class="sxs-lookup"><span data-stu-id="c27f8-142">0x00000040</span></span></td>
<td><span data-ttu-id="c27f8-143">Use esta marca para especificar cualquier modo de presentación RAW enumerado por el adaptador de pantalla, aunque Direct3D pueda haber indicado que el modo no es válido.</span><span class="sxs-lookup"><span data-stu-id="c27f8-143">Use this flag to specify any RAW display mode enumerated by the display adapter even though Direct3D may have indicated the mode is invalid.</span></span> <span data-ttu-id="c27f8-144">La aplicación debe implementar esto de una manera sólida en caso de que el modo deseado no sea realmente válido.</span><span class="sxs-lookup"><span data-stu-id="c27f8-144">The application should implement this in a robust manner in case the desired mode really is invalid.</span></span> 
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-145">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-145">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-146">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-146">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c27f8-147">D3DPRESENTFLAG_VIDEO</span><span class="sxs-lookup"><span data-stu-id="c27f8-147">D3DPRESENTFLAG_VIDEO</span></span></td>
<td><span data-ttu-id="c27f8-148">0x00000010</span><span class="sxs-lookup"><span data-stu-id="c27f8-148">0x00000010</span></span></td>
<td><span data-ttu-id="c27f8-149">Se trata de una sugerencia para el controlador de que los búferes de reserva contendrán datos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c27f8-149">This is a hint to the driver that the back buffers will contain video data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c27f8-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span><span class="sxs-lookup"><span data-stu-id="c27f8-150">D3DPRESENTFLAG_OVERLAY_LIMITEDRGB</span></span></td>
<td><span data-ttu-id="c27f8-151">0x00000080</span><span class="sxs-lookup"><span data-stu-id="c27f8-151">0x00000080</span></span></td>
<td><span data-ttu-id="c27f8-152">Especifica si la superposición es RGB de intervalo completo o RGB de intervalo limitado.</span><span class="sxs-lookup"><span data-stu-id="c27f8-152">Specifies whether the overlay is full range RGB or limited range RGB.</span></span> <span data-ttu-id="c27f8-153">Establecer esta marca indica un intervalo rgb limitado.</span><span class="sxs-lookup"><span data-stu-id="c27f8-153">Setting this flag indicates limited range RGB.</span></span> <span data-ttu-id="c27f8-154">En el rango limitado RGB, el intervalo RGB se comprime de forma que 16:16:16 es negro y 235:235:235 es blanco.</span><span class="sxs-lookup"><span data-stu-id="c27f8-154">In limited range RGB, the RGB range is compressed such that 16:16:16 is black and 235:235:235 is white.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-155">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-155">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-156">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-156">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c27f8-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span><span class="sxs-lookup"><span data-stu-id="c27f8-157">D3DPRESENTFLAG_OVERLAY_YCbCr_BT709</span></span></td>
<td><span data-ttu-id="c27f8-158">0x00000100</span><span class="sxs-lookup"><span data-stu-id="c27f8-158">0x00000100</span></span></td>
<td><span data-ttu-id="c27f8-159">Especifica si la superposición es BT.601 o BT.709.</span><span class="sxs-lookup"><span data-stu-id="c27f8-159">Specifies whether the overlay is BT.601 or BT.709.</span></span> <span data-ttu-id="c27f8-160">Si se establece esta marca, se indica BT.709, para televisión de alta definición (BT).</span><span class="sxs-lookup"><span data-stu-id="c27f8-160">Setting this flag indicates BT.709, for high-definition TV (HDTV).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-161">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-161">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-162">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-162">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c27f8-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span><span class="sxs-lookup"><span data-stu-id="c27f8-163">D3DPRESENTFLAG_OVERLAY_YCbCr_xvYCC</span></span></td>
<td><span data-ttu-id="c27f8-164">0x00000200</span><span class="sxs-lookup"><span data-stu-id="c27f8-164">0x00000200</span></span></td>
<td><span data-ttu-id="c27f8-165">Especifica si la superposición es YCbCr convencional o YCbCr extendido (sipYCC).</span><span class="sxs-lookup"><span data-stu-id="c27f8-165">Specifies whether the overlay is conventional YCbCr or extended YCbCr (xvYCC).</span></span> <span data-ttu-id="c27f8-166">Si se establece esta marca, se indica el YCbCr extendido (sipYCC).</span><span class="sxs-lookup"><span data-stu-id="c27f8-166">Setting this flag indicates extended YCbCr (xvYCC).</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-167">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-167">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-168">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-168">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c27f8-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span><span class="sxs-lookup"><span data-stu-id="c27f8-169">D3DPRESENTFLAG_RESTRICTED_CONTENT</span></span></td>
<td><span data-ttu-id="c27f8-170">0x00000400</span><span class="sxs-lookup"><span data-stu-id="c27f8-170">0x00000400</span></span></td>
<td><span data-ttu-id="c27f8-171">Establecer esta marca indica que la cadena de intercambio contiene contenido protegido y hace que el tiempo de ejecución restrinja automáticamente el acceso a la cadena de intercambio para que solo el Administrador de Escritorio de Windows (DWM) pueda usar la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="c27f8-171">Setting this flag indicates that the swapchain contains protected content and automatically causes the runtime to restrict access to the swapchain so that only the Desktop Windows Manager (DWM) can use the swapchain.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-172">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-172">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-173">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-173">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c27f8-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span><span class="sxs-lookup"><span data-stu-id="c27f8-174">D3DPRESENTFLAG_RESTRICT_SHARED_RESOURCE_DRIVER</span></span></td>
<td><span data-ttu-id="c27f8-175">0x00000800</span><span class="sxs-lookup"><span data-stu-id="c27f8-175">0x00000800</span></span></td>
<td><span data-ttu-id="c27f8-176">Establecer esta marca indica que el controlador debe restringir el acceso a los recursos compartidos que se crean para la interacción de DWM.</span><span class="sxs-lookup"><span data-stu-id="c27f8-176">Setting this flag indicates that the driver should restrict access to any shared resources that are created for DWM interaction.</span></span> <span data-ttu-id="c27f8-177">El autor de la llamada debe crear un canal autenticado con el controlador.</span><span class="sxs-lookup"><span data-stu-id="c27f8-177">The caller must create an authenticated channel with the driver.</span></span> <span data-ttu-id="c27f8-178">A continuación, el controlador debe permitir el acceso a los procesos que intentan abrir esos recursos compartidos.</span><span class="sxs-lookup"><span data-stu-id="c27f8-178">The driver should then allow access to processes that attempt to open those shared resources.</span></span>
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c27f8-179">Diferencias entre Direct3D 9 y Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="c27f8-179">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="c27f8-180">Esta marca solo está disponible en Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="c27f8-180">This flag is available in Direct3D 9Ex only.</span></span><br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c27f8-181">D3DPRESENT PARAMETERS usa estas [**\_ constantes.**](d3dpresent-parameters.md)</span><span class="sxs-lookup"><span data-stu-id="c27f8-181">These constants are used by [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md).</span></span>

## <a name="constant-information"></a><span data-ttu-id="c27f8-182">Información constante</span><span class="sxs-lookup"><span data-stu-id="c27f8-182">Constant Information</span></span>



| <span data-ttu-id="c27f8-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="c27f8-183">Requirement</span></span>                         | <span data-ttu-id="c27f8-184">Value</span><span class="sxs-lookup"><span data-stu-id="c27f8-184">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="c27f8-185">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c27f8-185">Header</span></span>                   | <span data-ttu-id="c27f8-186">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="c27f8-186">d3d9types.h</span></span> |
| <span data-ttu-id="c27f8-187">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="c27f8-187">Minimum operating system</span></span> | <span data-ttu-id="c27f8-188">Windows 98</span><span class="sxs-lookup"><span data-stu-id="c27f8-188">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="c27f8-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c27f8-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c27f8-190">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="c27f8-190">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




