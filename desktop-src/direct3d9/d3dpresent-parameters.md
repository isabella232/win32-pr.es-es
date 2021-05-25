---
description: Describe los parámetros de presentación.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS estructura (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: f113b3df247765b958dfe47bb04fafb6c9a13bbe
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343110"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="5f0dd-103">Estructura DE PARÁMETROS D3DPRESENT \_</span><span class="sxs-lookup"><span data-stu-id="5f0dd-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="5f0dd-104">Describe los parámetros de presentación.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f0dd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5f0dd-105">Syntax</span></span>


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="5f0dd-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="5f0dd-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5f0dd-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-109">Ancho de los búferes de reserva de la nueva cadena de intercambio, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="5f0dd-110">Si **Windowed** es **FALSE** (la presentación es de pantalla completa), este valor debe ser igual al ancho de uno de los modos de presentación enumerados que se encuentran a través de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="5f0dd-111">Si **Windowed** es **TRUE** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área de cliente de **hDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **NULL).**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-113">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-114">Alto de los búferes de reserva de la nueva cadena de intercambio, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="5f0dd-115">Si **Windowed** es **FALSE** (la presentación es de pantalla completa), este valor debe ser igual al alto de uno de los modos de presentación enumerados que se encuentran a través de [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="5f0dd-116">Si **Windowed** es **TRUE** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área de cliente de **hDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **NULL).**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-119">Formato de búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-119">The back buffer format.</span></span> <span data-ttu-id="5f0dd-120">Para obtener más información sobre los formatos, [vea D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="5f0dd-121">Este valor debe ser uno de los formatos de destino de representación validados [**por CheckDeviceType.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="5f0dd-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="5f0dd-122">Puede usar [**GetDisplayMode para**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) obtener el formato actual.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="5f0dd-123">De hecho, D3DFMT \_ UNKNOWN se puede especificar para **BackBufferFormat** en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="5f0dd-124">Esto indica al tiempo de ejecución que use el formato de modo de presentación actual y elimina la necesidad de llamar a [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="5f0dd-125">En el caso de las aplicaciones con ventanas, el formato de búfer de reserva ya no necesita coincidir con el formato de modo de presentación, ya que el hardware puede realizar la conversión de color (si el hardware admite la conversión de colores).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="5f0dd-126">El conjunto de posibles formatos de búfer de reserva está restringido, pero el tiempo de ejecución permitirá que cualquier formato de búfer de reserva válido se presente a cualquier formato de escritorio.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="5f0dd-127">(Existe el requisito adicional de que el dispositivo sea operable en el escritorio; los dispositivos normalmente no funcionan en modos de 8 bits por píxel).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="5f0dd-128">Las aplicaciones de pantalla completa no pueden realizar la conversión de colores.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-130">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-131">Este valor puede estar entre 0 y [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (o [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) cuando se usa Direct3D 9Ex).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="5f0dd-132">Los valores de 0 se tratan como 1.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="5f0dd-133">Si no se puede crear el número de búferes de reserva, el tiempo de ejecución producirá un error en la llamada al método y rellenará este valor con el número de búferes de reserva que se podrían crear.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="5f0dd-134">Como resultado, una aplicación puede llamar al método dos veces con la misma estructura D3DPRESENT PARAMETERS y esperar que funcione \_ la segunda vez.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="5f0dd-135">Se produce un error en el método si no se puede crear un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="5f0dd-136">El valor de **BackBufferCount influye** en qué conjunto de efectos de intercambio se permiten.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="5f0dd-137">En concreto, cualquier efecto de intercambio COPY de D3DSWAPEFFECT \_ requiere que haya exactamente un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-139">Tipo: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-140">Miembro del [**tipo enumerado D3DMULTISAMPLE \_ TYPE.**](./d3dmultisample-type.md)</span><span class="sxs-lookup"><span data-stu-id="5f0dd-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="5f0dd-141">El valor debe ser D3DMULTISAMPLE NONE a menos que SwapEffect se haya establecido \_ en D3DSWAPEFFECT  \_ DISCARD.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="5f0dd-142">Solo se admite la multimuestreo si el efecto de intercambio es D3DSWAPEFFECT \_ DISCARD.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-145">Nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-145">Quality level.</span></span> <span data-ttu-id="5f0dd-146">El intervalo válido está entre cero y uno menos que el nivel devuelto por pQualityLevels usado por [**CheckDeviceMultiSampleType.**](/windows/desktop/api)</span><span class="sxs-lookup"><span data-stu-id="5f0dd-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="5f0dd-147">Al pasar un valor mayor, se devuelve el error D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="5f0dd-148">Los valores emparejados de destinos de representación o de superficies de galería de símbolos de profundidad y [**D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md) deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-150">Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-151">Miembro del [**tipo enumerado D3DSWAPEFFECT.**](./d3dswapeffect.md)</span><span class="sxs-lookup"><span data-stu-id="5f0dd-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="5f0dd-152">El tiempo de ejecución garantizará la semántica implícita relativa al comportamiento de intercambio de búfer; Por lo tanto, si **Windowed** es **TRUE** y **SwapEffect** se establece en D3DSWAPEFFECT FLIP, el tiempo de ejecución creará un búfer de reserva adicional y copiará lo que se convierta en el búfer frontal en el momento de la \_ presentación.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="5f0dd-153">D3DSWAPEFFECT \_ COPY requiere que **BackBufferCount** se establezca en 1.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="5f0dd-154">D3DSWAPEFFECT DISCARD se aplicará en el tiempo de ejecución de depuración rellenando cualquier búfer con ruido \_ después de que se presente.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>

<span data-ttu-id="5f0dd-155">Diferencias entre Direct3D9 y Direct3D9Ex:</span><span class="sxs-lookup"><span data-stu-id="5f0dd-155">Differences between Direct3D9 and Direct3D9Ex:</span></span>

- <span data-ttu-id="5f0dd-156">En Direct3D9Ex, se agrega D3DSWAPEFFECT FLIPEX para designar cuándo una aplicación adopta \_ el modo de volteo.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="5f0dd-157">Es decir, el marco de una aplicación se pasa en modo de ventana (en lugar de copiarse) al Administrador de ventanas de escritorio(DWM) para la composición.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="5f0dd-158">El modo de volteo proporciona un ancho de banda de memoria más eficaz y permite que una aplicación aproveche las estadísticas de pantalla completa presentes.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="5f0dd-159">No cambia el comportamiento de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-159">It does not change full screen behavior.</span></span> <span data-ttu-id="5f0dd-160">El comportamiento del modo de volteo está disponible a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-160">Flip mode behavior is available beginning with Windows 7.</span></span>



 

</dd> <dt>

<span data-ttu-id="5f0dd-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-162">Tipo: **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-163">La ventana del dispositivo determina la ubicación y el tamaño del búfer de reserva en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="5f0dd-164">Direct3D lo usa cuando el contenido del búfer de reserva se copia en el búfer front-buffer durante [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="5f0dd-165">Para una aplicación de pantalla completa, se trata de un identificador de la ventana superior (que es la ventana de foco).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="5f0dd-166">En el caso de las aplicaciones que usan varios dispositivos de pantalla completa (por ejemplo, un sistema multimonitor), exactamente un dispositivo puede usar la ventana de foco como ventana del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="5f0dd-167">Todos los demás dispositivos deben tener ventanas de dispositivo únicas.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="5f0dd-168">Para una aplicación en modo de ventana, este identificador será la ventana de destino predeterminada para [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="5f0dd-169">Si este identificador es **NULL,** se toma la ventana de foco.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="5f0dd-170">Tenga en cuenta que el tiempo de ejecución no intenta reflejar los cambios del usuario en el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="5f0dd-171">El búfer de reserva no se restablece implícitamente cuando se restablece esta ventana.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="5f0dd-172">Sin embargo, [**el método Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) realiza un seguimiento automático de los cambios de posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-173">**Ventana**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-174">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-175">**TRUE** si la aplicación se ejecuta en ventanas; **FALSE** si la aplicación se ejecuta a pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-177">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-178">Si este valor es **TRUE,** Direct3D administrará los búferes de profundidad para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="5f0dd-179">El dispositivo creará un búfer de galería de símbolos de profundidad cuando se cree.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="5f0dd-180">El búfer de galería de símbolos de profundidad se establecerá automáticamente como destino de representación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="5f0dd-181">Cuando se restablece el dispositivo, el búfer de galería de símbolos de profundidad se destruirá automáticamente y se volverá a crear con el nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="5f0dd-182">Si EnableAutoDepthStencil es **TRUE,** AutoDepthStencilFormat debe ser un formato válido de galería de símbolos de profundidad.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-184">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-185">Miembro del [tipo enumerado D3DFORMAT.](d3dformat.md)</span><span class="sxs-lookup"><span data-stu-id="5f0dd-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="5f0dd-186">Formato de la superficie de galería de símbolos de profundidad automática que creará el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="5f0dd-187">Este miembro se omite a menos **que EnableAutoDepthStencil** sea **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-188">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-189">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-190">Una de las [constantes D3DPRESENTFLAG.](d3dpresentflag.md)</span><span class="sxs-lookup"><span data-stu-id="5f0dd-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-191">**Actualización de \_ FullScreenRateInHz**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-192">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-193">Velocidad a la que el adaptador de pantalla actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="5f0dd-194">El valor depende del modo en el que se ejecuta la aplicación:</span><span class="sxs-lookup"><span data-stu-id="5f0dd-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="5f0dd-195">Para el modo de ventana, la frecuencia de actualización debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="5f0dd-196">Para el modo de pantalla completa, la frecuencia de actualización es una de las tasas de actualización devueltas por [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="5f0dd-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="5f0dd-198">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="5f0dd-199">Velocidad máxima a la que se pueden presentar los búferes de reserva de la cadena de intercambio al búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="5f0dd-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="5f0dd-200">Para obtener una explicación detallada de los modos y los intervalos admitidos, vea [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="5f0dd-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f0dd-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f0dd-201">Requirements</span></span>



| <span data-ttu-id="5f0dd-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f0dd-202">Requirement</span></span> | <span data-ttu-id="5f0dd-203">Value</span><span class="sxs-lookup"><span data-stu-id="5f0dd-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f0dd-204">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f0dd-204">Header</span></span><br/> | <dl> <span data-ttu-id="5f0dd-205"><dt>D3D9Types.h</dt></span><span class="sxs-lookup"><span data-stu-id="5f0dd-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f0dd-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f0dd-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f0dd-207">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="5f0dd-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="5f0dd-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="5f0dd-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="5f0dd-210">**Presente**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="5f0dd-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="5f0dd-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
