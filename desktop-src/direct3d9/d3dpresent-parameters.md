---
description: Describe los parámetros de presentación.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS estructura (D3D9Types. h)
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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362611"
---
# <a name="d3dpresent_parameters-structure"></a><span data-ttu-id="34d1a-103">\_Estructura de los parámetros D3DPRESENT</span><span class="sxs-lookup"><span data-stu-id="34d1a-103">D3DPRESENT\_PARAMETERS structure</span></span>

<span data-ttu-id="34d1a-104">Describe los parámetros de presentación.</span><span class="sxs-lookup"><span data-stu-id="34d1a-104">Describes the presentation parameters.</span></span>

## <a name="syntax"></a><span data-ttu-id="34d1a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="34d1a-105">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="34d1a-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="34d1a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="34d1a-107">**BackBufferWidth**</span><span class="sxs-lookup"><span data-stu-id="34d1a-107">**BackBufferWidth**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-109">Ancho de los búferes de reserva de la nueva cadena de intercambio, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="34d1a-109">Width of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="34d1a-110">Si **windowed** es **false** (la presentación está en pantalla completa), este valor debe ser igual al ancho de uno de los modos de presentación enumerados que se encuentran en [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="34d1a-110">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the width of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="34d1a-111">Si **windowed** es **true** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área cliente de **HDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **null**).</span><span class="sxs-lookup"><span data-stu-id="34d1a-111">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-112">**BackBufferHeight**</span><span class="sxs-lookup"><span data-stu-id="34d1a-112">**BackBufferHeight**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-113">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-114">Alto de los búferes de reserva de la nueva cadena de intercambio, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="34d1a-114">Height of the new swap chain's back buffers, in pixels.</span></span> <span data-ttu-id="34d1a-115">Si **windowed** es **false** (la presentación está en pantalla completa), este valor debe ser igual al alto de uno de los modos de presentación enumerados que se encuentran en [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="34d1a-115">If **Windowed** is **FALSE** (the presentation is full-screen), this value must equal the height of one of the enumerated display modes found through [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span> <span data-ttu-id="34d1a-116">Si **windowed** es **true** y **BackBufferWidth** o **BackBufferHeight** es cero, se toma la dimensión correspondiente del área cliente de **HDeviceWindow** (o la ventana de foco, si **hDeviceWindow** es **null**).</span><span class="sxs-lookup"><span data-stu-id="34d1a-116">If **Windowed** is **TRUE** and either **BackBufferWidth** or **BackBufferHeight** is zero, the corresponding dimension of the client area of the **hDeviceWindow** (or the focus window, if **hDeviceWindow** is **NULL**) is taken.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-117">**BackBufferFormat**</span><span class="sxs-lookup"><span data-stu-id="34d1a-117">**BackBufferFormat**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-118">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-118">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-119">El formato del búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="34d1a-119">The back buffer format.</span></span> <span data-ttu-id="34d1a-120">Para obtener más información acerca de los formatos, vea [D3DFORMAT](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="34d1a-120">For more information about formats, see [D3DFORMAT](d3dformat.md).</span></span> <span data-ttu-id="34d1a-121">Este valor debe ser uno de los formatos de representación-destino tal y como lo valida [**CheckDeviceType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="34d1a-121">This value must be one of the render-target formats as validated by [**CheckDeviceType**](/windows/desktop/api).</span></span> <span data-ttu-id="34d1a-122">Puede usar [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) para obtener el formato actual.</span><span class="sxs-lookup"><span data-stu-id="34d1a-122">You can use [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) to obtain the current format.</span></span>

<span data-ttu-id="34d1a-123">De hecho, \_ se puede especificar D3DFMT Unknown para **BackBufferFormat** mientras está en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="34d1a-123">In fact, D3DFMT\_UNKNOWN can be specified for the **BackBufferFormat** while in windowed mode.</span></span> <span data-ttu-id="34d1a-124">Esto indica al tiempo de ejecución que use el formato de modo de presentación actual y elimina la necesidad de llamar a [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span><span class="sxs-lookup"><span data-stu-id="34d1a-124">This tells the runtime to use the current display-mode format and eliminates the need to call [**GetDisplayMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode).</span></span>

<span data-ttu-id="34d1a-125">En el caso de las aplicaciones en ventanas, el formato del búfer de reserva ya no necesita coincidir con el formato de modo de presentación, ya que el hardware ahora puede realizar la conversión de colores (si el hardware admite la conversión de colores).</span><span class="sxs-lookup"><span data-stu-id="34d1a-125">For windowed applications, the back buffer format no longer needs to match the display-mode format because color conversion can now be done by the hardware (if the hardware supports color conversion).</span></span> <span data-ttu-id="34d1a-126">El conjunto de posibles formatos de búfer de reserva está restringido, pero el tiempo de ejecución permitirá que se presente cualquier formato de búfer de reserva válido a cualquier formato de escritorio.</span><span class="sxs-lookup"><span data-stu-id="34d1a-126">The set of possible back buffer formats is constrained, but the runtime will allow any valid back buffer format to be presented to any desktop format.</span></span> <span data-ttu-id="34d1a-127">(Existe el requisito adicional de que el dispositivo funcione en el escritorio; normalmente, los dispositivos no funcionan en los modos de 8 bits por píxel).</span><span class="sxs-lookup"><span data-stu-id="34d1a-127">(There is the additional requirement that the device be operable in the desktop; devices typically do not operate in 8 bits per pixel modes.)</span></span>

<span data-ttu-id="34d1a-128">Las aplicaciones de pantalla completa no pueden realizar la conversión de color.</span><span class="sxs-lookup"><span data-stu-id="34d1a-128">Full-screen applications cannot do color conversion.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-129">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="34d1a-129">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-130">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-131">Este valor puede estar comprendido entre 0 y [D3DPRESENT \_ \_ búferes \_ ](d3dpresent-back-buffers.md) de reserva Max (o [D3DPRESENT de \_ \_ búferes de reserva \_ Max \_ ex](d3dpresent-back-buffers.md) al usar Direct3D 9Ex).</span><span class="sxs-lookup"><span data-stu-id="34d1a-131">This value can be between 0 and [D3DPRESENT\_BACK\_BUFFERS\_MAX](d3dpresent-back-buffers.md) (or [D3DPRESENT\_BACK\_BUFFERS\_MAX\_EX](d3dpresent-back-buffers.md) when using Direct3D 9Ex).</span></span> <span data-ttu-id="34d1a-132">Los valores 0 se tratan como 1.</span><span class="sxs-lookup"><span data-stu-id="34d1a-132">Values of 0 are treated as 1.</span></span> <span data-ttu-id="34d1a-133">Si no se puede crear el número de búferes de reserva, el tiempo de ejecución producirá un error en la llamada al método y rellenará este valor con el número de búferes de reserva que se pueden crear.</span><span class="sxs-lookup"><span data-stu-id="34d1a-133">If the number of back buffers cannot be created, the runtime will fail the method call and fill this value with the number of back buffers that could be created.</span></span> <span data-ttu-id="34d1a-134">Como resultado, una aplicación puede llamar al método dos veces con la misma \_ estructura de parámetros D3DPRESENT y esperar que funcione la segunda vez.</span><span class="sxs-lookup"><span data-stu-id="34d1a-134">As a result, an application can call the method twice with the same D3DPRESENT\_PARAMETERS structure and expect it to work the second time.</span></span>

<span data-ttu-id="34d1a-135">El método genera un error si no se puede crear un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="34d1a-135">The method fails if one back buffer cannot be created.</span></span> <span data-ttu-id="34d1a-136">El valor de **BackBufferCount** influye en el conjunto de efectos de intercambio permitidos.</span><span class="sxs-lookup"><span data-stu-id="34d1a-136">The value of **BackBufferCount** influences what set of swap effects are allowed.</span></span> <span data-ttu-id="34d1a-137">En concreto, cualquier \_ efecto de intercambio de copia de D3DSWAPEFFECT requiere que haya exactamente un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="34d1a-137">Specifically, any D3DSWAPEFFECT\_COPY swap effect requires that there be exactly one back buffer.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-138">**MultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="34d1a-138">**MultiSampleType**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-139">Tipo: **[ **D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-139">Type: **[**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-140">Miembro del tipo enumerado de [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="34d1a-140">Member of the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="34d1a-141">El valor debe ser D3DMULTISAMPLE \_ None, a menos que **SwapEffect** se haya establecido en D3DSWAPEFFECT \_ discard.</span><span class="sxs-lookup"><span data-stu-id="34d1a-141">The value must be D3DMULTISAMPLE\_NONE unless **SwapEffect** has been set to D3DSWAPEFFECT\_DISCARD.</span></span> <span data-ttu-id="34d1a-142">El muestreo múltiple solo se admite si el efecto de intercambio es D3DSWAPEFFECT \_ discard.</span><span class="sxs-lookup"><span data-stu-id="34d1a-142">Multisampling is supported only if the swap effect is D3DSWAPEFFECT\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-143">**MultiSampleQuality**</span><span class="sxs-lookup"><span data-stu-id="34d1a-143">**MultiSampleQuality**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-144">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-144">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-145">Nivel de calidad.</span><span class="sxs-lookup"><span data-stu-id="34d1a-145">Quality level.</span></span> <span data-ttu-id="34d1a-146">El intervalo válido está comprendido entre cero y uno menos que el nivel devuelto por pQualityLevels usado por [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="34d1a-146">The valid range is between zero and one less than the level returned by pQualityLevels used by [**CheckDeviceMultiSampleType**](/windows/desktop/api).</span></span> <span data-ttu-id="34d1a-147">Al pasar un valor mayor, se devuelve el error D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="34d1a-147">Passing a larger value returns the error D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="34d1a-148">Los valores emparejados de destinos de representación o de superficies de estarcido de profundidad y [**\_ tipo D3DMULTISAMPLE**](./d3dmultisample-type.md) deben coincidir.</span><span class="sxs-lookup"><span data-stu-id="34d1a-148">Paired values of render targets or of depth stencil surfaces and [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) must match.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-149">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="34d1a-149">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-150">Tipo: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-150">Type: **[**D3DSWAPEFFECT**](./d3dswapeffect.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-151">Miembro del tipo enumerado [**D3DSWAPEFFECT**](./d3dswapeffect.md) .</span><span class="sxs-lookup"><span data-stu-id="34d1a-151">Member of the [**D3DSWAPEFFECT**](./d3dswapeffect.md) enumerated type.</span></span> <span data-ttu-id="34d1a-152">El tiempo de ejecución garantizará la semántica implícita relacionada con el comportamiento de intercambio de búfer; por lo tanto, si **windowed** es **true** y **SwapEffect** se establece en D3DSWAPEFFECT \_ Flip, el tiempo de ejecución creará un búfer de reserva adicional y copiará el que se convierta en el búfer frontal en el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="34d1a-152">The runtime will guarantee the implied semantics concerning buffer swap behavior; therefore, if **Windowed** is **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIP, the runtime will create one extra back buffer and copy whichever becomes the front buffer at presentation time.</span></span>

<span data-ttu-id="34d1a-153">La \_ copia de D3DSWAPEFFECT requiere que **BackBufferCount** se establezca en 1.</span><span class="sxs-lookup"><span data-stu-id="34d1a-153">D3DSWAPEFFECT\_COPY requires that **BackBufferCount** be set to 1.</span></span>

<span data-ttu-id="34d1a-154">D3DSWAPEFFECT \_ discard se aplicará en el tiempo de ejecución de depuración rellenando cualquier búfer con ruido una vez presentado.</span><span class="sxs-lookup"><span data-stu-id="34d1a-154">D3DSWAPEFFECT\_DISCARD will be enforced in the debug runtime by filling any buffer with noise after it is presented.</span></span>



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34d1a-155">Diferencias entre Direct3D9 y Direct3D9Ex</span><span class="sxs-lookup"><span data-stu-id="34d1a-155">Differences between Direct3D9 and Direct3D9Ex</span></span><br/> <span data-ttu-id="34d1a-156">En Direct3D9Ex, \_ se agrega D3DSWAPEFFECT FLIPEX para designar cuando una aplicación está adoptando el modo flip.</span><span class="sxs-lookup"><span data-stu-id="34d1a-156">In Direct3D9Ex, D3DSWAPEFFECT\_FLIPEX is added to designate when an application is adopting flip mode.</span></span> <span data-ttu-id="34d1a-157">Es decir, Whan el marco de una aplicación se pasa en el modo de la ventana (en lugar de copiarse) al Administrador de ventanas de escritorio (DWM) para la composición.</span><span class="sxs-lookup"><span data-stu-id="34d1a-157">That is, whan an application's frame is passed in window's mode (instead of copied) to the Desktop Window Manager(DWM) for composition.</span></span> <span data-ttu-id="34d1a-158">El modo Flip proporciona un ancho de banda de memoria más eficaz y permite a una aplicación aprovechar las estadísticas de presentación en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="34d1a-158">Flip mode provides more efficient memory bandwidth and enables an application to take advantage of full-screen-present statistics.</span></span> <span data-ttu-id="34d1a-159">No cambia el comportamiento de la pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="34d1a-159">It does not change full screen behavior.</span></span> <span data-ttu-id="34d1a-160">El comportamiento del modo de volteo está disponible a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="34d1a-160">Flip mode behavior is available beginning with Windows 7.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="34d1a-161">**hDeviceWindow**</span><span class="sxs-lookup"><span data-stu-id="34d1a-161">**hDeviceWindow**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-162">Tipo: **[ **hWnd**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-162">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-163">La ventana dispositivo determina la ubicación y el tamaño del búfer de reserva en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="34d1a-163">The device window determines the location and size of the back buffer on screen.</span></span> <span data-ttu-id="34d1a-164">Direct3D lo usa cuando el contenido del búfer de reserva se copia en el búfer frontal durante su [**presencia**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="34d1a-164">This is used by Direct3D when the back buffer contents are copied to the front buffer during [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span>

-   <span data-ttu-id="34d1a-165">En el caso de una aplicación de pantalla completa, se trata de un identificador de la ventana superior (que es la ventana de enfoque).</span><span class="sxs-lookup"><span data-stu-id="34d1a-165">For a full-screen application, this is a handle to the top window (which is the focus window).</span></span>

    <span data-ttu-id="34d1a-166">En el caso de las aplicaciones que usan varios dispositivos de pantalla completa (por ejemplo, un sistema de varios monitores), exactamente un dispositivo puede usar la ventana de enfoque como ventana del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d1a-166">For applications that use multiple full-screen devices (such as a multimonitor system), exactly one device can use the focus window as the device window.</span></span> <span data-ttu-id="34d1a-167">Todos los demás dispositivos deben tener ventanas de dispositivo únicas.</span><span class="sxs-lookup"><span data-stu-id="34d1a-167">All other devices must have unique device windows.</span></span>

-   <span data-ttu-id="34d1a-168">En el caso de una aplicación de modo de ventana, este identificador será la ventana de destino predeterminada para [**present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span><span class="sxs-lookup"><span data-stu-id="34d1a-168">For a windowed-mode application, this handle will be the default target window for [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).</span></span> <span data-ttu-id="34d1a-169">Si este identificador es **null**, se tomará la ventana de foco.</span><span class="sxs-lookup"><span data-stu-id="34d1a-169">If this handle is **NULL**, the focus window will be taken.</span></span>

<span data-ttu-id="34d1a-170">Tenga en cuenta que el tiempo de ejecución no realiza ningún intento para reflejar los cambios de usuario en el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="34d1a-170">Note that no attempt is made by the runtime to reflect user changes in window size.</span></span> <span data-ttu-id="34d1a-171">El búfer de reserva no se restablece implícitamente cuando se restablece esta ventana.</span><span class="sxs-lookup"><span data-stu-id="34d1a-171">The back buffer is not implicitly reset when this window is reset.</span></span> <span data-ttu-id="34d1a-172">Sin embargo, el método [**actual**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) realiza un seguimiento automático de los cambios de posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="34d1a-172">However, the [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) method does automatically track window position changes.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-173">**Ventanas**</span><span class="sxs-lookup"><span data-stu-id="34d1a-173">**Windowed**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-174">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-174">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-175">**True** si la aplicación se ejecuta en la ventana; **False** si la aplicación se ejecuta en pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="34d1a-175">**TRUE** if the application runs windowed; **FALSE** if the application runs full-screen.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-176">**EnableAutoDepthStencil**</span><span class="sxs-lookup"><span data-stu-id="34d1a-176">**EnableAutoDepthStencil**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-177">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-177">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-178">Si este valor es **true**, Direct3D administrará los búferes de profundidad de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="34d1a-178">If this value is **TRUE**, Direct3D will manage depth buffers for the application.</span></span> <span data-ttu-id="34d1a-179">El dispositivo creará un búfer de estarcido de profundidad cuando se cree.</span><span class="sxs-lookup"><span data-stu-id="34d1a-179">The device will create a depth-stencil buffer when it is created.</span></span> <span data-ttu-id="34d1a-180">El búfer de estarcido de profundidad se establecerá automáticamente como el destino de representación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d1a-180">The depth-stencil buffer will be automatically set as the render target of the device.</span></span> <span data-ttu-id="34d1a-181">Cuando se restablece el dispositivo, el búfer de estarcido de profundidad se destruye y se vuelve a crear automáticamente con el nuevo tamaño.</span><span class="sxs-lookup"><span data-stu-id="34d1a-181">When the device is reset, the depth-stencil buffer will be automatically destroyed and recreated in the new size.</span></span>

<span data-ttu-id="34d1a-182">Si EnableAutoDepthStencil es **true**, AutoDepthStencilFormat debe ser un formato de estarcido de profundidad válido.</span><span class="sxs-lookup"><span data-stu-id="34d1a-182">If EnableAutoDepthStencil is **TRUE**, then AutoDepthStencilFormat must be a valid depth-stencil format.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-183">**AutoDepthStencilFormat**</span><span class="sxs-lookup"><span data-stu-id="34d1a-183">**AutoDepthStencilFormat**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-184">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-184">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-185">Miembro del tipo enumerado [D3DFORMAT](d3dformat.md) .</span><span class="sxs-lookup"><span data-stu-id="34d1a-185">Member of the [D3DFORMAT](d3dformat.md) enumerated type.</span></span> <span data-ttu-id="34d1a-186">El formato de la superficie de estarcido de profundidad automática que creará el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34d1a-186">The format of the automatic depth-stencil surface that the device will create.</span></span> <span data-ttu-id="34d1a-187">Este miembro se omite a menos que **EnableAutoDepthStencil** sea **true**.</span><span class="sxs-lookup"><span data-stu-id="34d1a-187">This member is ignored unless **EnableAutoDepthStencil** is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-188">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="34d1a-188">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-189">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-189">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-190">Una de las constantes de [D3DPRESENTFLAG](d3dpresentflag.md) .</span><span class="sxs-lookup"><span data-stu-id="34d1a-190">One of the [D3DPRESENTFLAG](d3dpresentflag.md) constants.</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-191">**RefreshRateInHz de pantalla completa \_**</span><span class="sxs-lookup"><span data-stu-id="34d1a-191">**FullScreen\_RefreshRateInHz**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-192">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-192">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-193">Velocidad a la que el adaptador de pantalla actualiza la pantalla.</span><span class="sxs-lookup"><span data-stu-id="34d1a-193">The rate at which the display adapter refreshes the screen.</span></span> <span data-ttu-id="34d1a-194">El valor depende del modo en el que se ejecuta la aplicación:</span><span class="sxs-lookup"><span data-stu-id="34d1a-194">The value depends on the mode in which the application is running:</span></span>

-   <span data-ttu-id="34d1a-195">En el modo de ventana, la frecuencia de actualización debe ser 0.</span><span class="sxs-lookup"><span data-stu-id="34d1a-195">For windowed mode, the refresh rate must be 0.</span></span>
-   <span data-ttu-id="34d1a-196">En el modo de pantalla completa, la frecuencia de actualización es una de las frecuencias de actualización devueltas por [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span><span class="sxs-lookup"><span data-stu-id="34d1a-196">For full-screen mode, the refresh rate is one of the refresh rates returned by [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes).</span></span>

</dd> <dt>

<span data-ttu-id="34d1a-197">**PresentationInterval**</span><span class="sxs-lookup"><span data-stu-id="34d1a-197">**PresentationInterval**</span></span>
</dt> <dd>

<span data-ttu-id="34d1a-198">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34d1a-198">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34d1a-199">La velocidad máxima a la que se pueden presentar los búferes de reserva de la cadena de intercambio en el búfer frontal.</span><span class="sxs-lookup"><span data-stu-id="34d1a-199">The maximum rate at which the swap chain's back buffers can be presented to the front buffer.</span></span> <span data-ttu-id="34d1a-200">Para obtener una explicación detallada de los modos y los intervalos que se admiten, vea [D3DPRESENT](d3dpresent.md).</span><span class="sxs-lookup"><span data-stu-id="34d1a-200">For a detailed explanation of the modes and the intervals that are supported, see [D3DPRESENT](d3dpresent.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="34d1a-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="34d1a-201">Requirements</span></span>



| <span data-ttu-id="34d1a-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="34d1a-202">Requirement</span></span> | <span data-ttu-id="34d1a-203">Value</span><span class="sxs-lookup"><span data-stu-id="34d1a-203">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34d1a-204">Encabezado</span><span class="sxs-lookup"><span data-stu-id="34d1a-204">Header</span></span><br/> | <dl> <span data-ttu-id="34d1a-205"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="34d1a-205"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34d1a-206">Vea también</span><span class="sxs-lookup"><span data-stu-id="34d1a-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34d1a-207">Estructuras de Direct3D</span><span class="sxs-lookup"><span data-stu-id="34d1a-207">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="34d1a-208">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="34d1a-208">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="34d1a-209">**CreateAdditionalSwapChain**</span><span class="sxs-lookup"><span data-stu-id="34d1a-209">**CreateAdditionalSwapChain**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[<span data-ttu-id="34d1a-210">**Presente**</span><span class="sxs-lookup"><span data-stu-id="34d1a-210">**Present**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[<span data-ttu-id="34d1a-211">**Reset**</span><span class="sxs-lookup"><span data-stu-id="34d1a-211">**Reset**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
