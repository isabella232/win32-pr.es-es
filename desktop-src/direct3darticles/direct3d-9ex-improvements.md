---
title: Mejoras de Direct3D 9Ex
description: En este tema se describe la compatibilidad agregada de Windows 7 con el modo de volteo presente y sus estadísticas actuales asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio.
ms.assetid: cb92a162-57eb-4aee-af7a-c8ece37075a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42eef10b6caaa959cb750f073c97a0f665384463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421171"
---
# <a name="direct3d-9ex-improvements"></a><span data-ttu-id="9f709-103">Mejoras de Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="9f709-103">Direct3D 9Ex improvements</span></span>

<span data-ttu-id="9f709-104">En este tema se describe la compatibilidad agregada de Windows 7 con el modo de volteo presente y sus estadísticas actuales asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio.</span><span class="sxs-lookup"><span data-stu-id="9f709-104">This topic describes Windows 7's added support for Flip Mode Present and its associated present statistics in Direct3D 9Ex and Desktop Window Manager.</span></span> <span data-ttu-id="9f709-105">Las aplicaciones de destino incluyen aplicaciones de presentación basadas en la velocidad de fotogramas o en vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f709-105">Target applications include video or frame rate-based presentation applications.</span></span> <span data-ttu-id="9f709-106">Las aplicaciones que usan el modo Flip de Direct3D 9Ex, reducen la carga de recursos del sistema cuando DWM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="9f709-106">Applications that use Direct3D 9Ex Flip Mode Present reduce the system resource load when DWM is enabled.</span></span> <span data-ttu-id="9f709-107">Las mejoras presentes en las estadísticas asociadas con el modo de volteo permiten a las aplicaciones de Direct3D 9Ex controlar mejor la velocidad de presentación al proporcionar mecanismos de corrección y comentarios en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="9f709-107">Present statistics enhancements associated with Flip Mode Present enable Direct3D 9Ex applications to better control the rate of presentation by providing real-time feedback and correction mechanisms.</span></span> <span data-ttu-id="9f709-108">Se incluyen explicaciones detalladas y punteros a los recursos de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9f709-108">Detailed explanations and pointers to sample resources are included.</span></span>

<span data-ttu-id="9f709-109">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="9f709-109">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9f709-110">Mejoras de Direct3D 9Ex para Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f709-110">What's Improved about Direct3D 9Ex for Windows 7</span></span>](#whats-improved-about-direct3d-9ex-for-windows-7)
-   [<span data-ttu-id="9f709-111">Presentación del modo Flip de Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="9f709-111">Direct3D 9EX Flip Mode Presentation</span></span>](#direct3d-9ex-flip-mode-presentation)
-   [<span data-ttu-id="9f709-112">Modelo de programación y API</span><span class="sxs-lookup"><span data-stu-id="9f709-112">Programming Model and APIs</span></span>](#programming-model-and-apis)
    -   [<span data-ttu-id="9f709-113">Cómo participar en el modelo Flip de Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="9f709-113">How to Opt Into the Direct3D 9Ex Flip Model</span></span>](#how-to-opt-into-the-direct3d-9ex-flip-model)
    -   [<span data-ttu-id="9f709-114">Instrucciones de diseño para aplicaciones de modelo Flip 9Ex de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9f709-114">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>](#design-guidelines-for-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="9f709-115">Sincronización de fotogramas de aplicaciones de modelo Flip 9Ex de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9f709-115">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>](#frame-synchronization-of-direct3d-9ex-flip-model-applications)
    -   [<span data-ttu-id="9f709-116">Sincronización de fotogramas para aplicaciones en ventanas cuando DWM está desactivado</span><span class="sxs-lookup"><span data-stu-id="9f709-116">Frame Synchronization for Windowed Applications When DWM is Off</span></span>](#frame-synchronization-for-windowed-applications-when-dwm-is-off)
-   [<span data-ttu-id="9f709-117">Tutorial sobre un modelo Flip de Direct3D 9Ex y el ejemplo present Statistics</span><span class="sxs-lookup"><span data-stu-id="9f709-117">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>](#walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample)
    -   [<span data-ttu-id="9f709-118">Resumen de las recomendaciones de programación para la sincronización de fotogramas</span><span class="sxs-lookup"><span data-stu-id="9f709-118">Summary of Programming Recommendations for Frame Synchronization</span></span>](#summary-of-programming-recommendations-for-frame-synchronization)
-   [<span data-ttu-id="9f709-119">Conclusión sobre las mejoras de Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="9f709-119">Conclusion about Direct3D 9Ex Improvements</span></span>](#conclusion-about-direct3d-9ex-improvements)
-   [<span data-ttu-id="9f709-120">Llamada a la acción</span><span class="sxs-lookup"><span data-stu-id="9f709-120">Call to Action</span></span>](#call-to-action)
-   [<span data-ttu-id="9f709-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f709-121">Related topics</span></span>](#related-topics)

## <a name="whats-improved-about-direct3d-9ex-for-windows-7"></a><span data-ttu-id="9f709-122">Mejoras de Direct3D 9Ex para Windows 7</span><span class="sxs-lookup"><span data-stu-id="9f709-122">What's Improved about Direct3D 9Ex for Windows 7</span></span>

<span data-ttu-id="9f709-123">La presentación del modo de volteo de Direct3D 9Ex es un modo mejorado de presentar imágenes en Direct3D 9Ex que se entregan de forma eficaz imágenes representadas a Windows 7 Administrador de ventanas de escritorio (DWM) para su composición.</span><span class="sxs-lookup"><span data-stu-id="9f709-123">Flip Mode Presentation of Direct3D 9Ex is an improved mode of presenting images in Direct3D 9Ex that efficiently hands off rendered images to Windows 7 Desktop Window Manager (DWM) for composition.</span></span> <span data-ttu-id="9f709-124">A partir de Windows Vista, DWM compone todo el escritorio.</span><span class="sxs-lookup"><span data-stu-id="9f709-124">Beginning in Windows Vista, DWM composes the entire Desktop.</span></span> <span data-ttu-id="9f709-125">Cuando DWM está habilitado, las aplicaciones en modo de ventana presentan su contenido en el escritorio mediante un método denominado BLT Mode present to DWM (o BLT Model).</span><span class="sxs-lookup"><span data-stu-id="9f709-125">When DWM is enabled, windowed mode applications present their contents on the Desktop by using a method called Blt Mode Present to DWM (or Blt Model).</span></span> <span data-ttu-id="9f709-126">Con el modelo BLT, DWM mantiene una copia de la superficie representada de Direct3D 9Ex para la composición del escritorio.</span><span class="sxs-lookup"><span data-stu-id="9f709-126">With Blt Model, DWM maintains a copy of the Direct3D 9Ex rendered surface for Desktop composition.</span></span> <span data-ttu-id="9f709-127">Cuando se actualiza la aplicación, el nuevo contenido se copia en la superficie de DWM a través de BLT.</span><span class="sxs-lookup"><span data-stu-id="9f709-127">When the application updates, the new content is copied to the DWM surface through a blt.</span></span> <span data-ttu-id="9f709-128">En el caso de las aplicaciones que contienen contenido de Direct3D y GDI, los datos GDI también se copian en la superficie DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-128">For applications that contain Direct3D and GDI content, the GDI data is also copied onto the DWM surface.</span></span>

<span data-ttu-id="9f709-129">Disponible en Windows 7, el modo de volteo presente para DWM (o voltear modelo) es un nuevo método de presentación que habilita esencialmente los controladores de paso de las superficies de aplicación entre las aplicaciones en modo de ventana y DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-129">Available in Windows 7, Flip Mode Present to DWM (or Flip Model) is a new presentation method that essentially enables passing handles of application surfaces between windowed mode applications and DWM.</span></span> <span data-ttu-id="9f709-130">Además de guardar los recursos, flip Model admite estadísticas actuales mejoradas.</span><span class="sxs-lookup"><span data-stu-id="9f709-130">In addition to saving resources, Flip Model supports enhanced present statistics.</span></span>

<span data-ttu-id="9f709-131">Las estadísticas presentes son información de temporización de fotogramas que las aplicaciones pueden usar para sincronizar secuencias de audio y vídeo y recuperarse de problemas de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f709-131">Present statistics are frame-timing information that applications can use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="9f709-132">La información de tiempo de marco de las estadísticas presentes permite a las aplicaciones ajustar la velocidad de presentación de los fotogramas de vídeo para una presentación más fluida.</span><span class="sxs-lookup"><span data-stu-id="9f709-132">The frame-timing information in present statistics allows applications to adjust the presentation rate of their video frames for smoother presentation.</span></span> <span data-ttu-id="9f709-133">En Windows Vista, donde DWM mantiene una copia correspondiente de la superficie de marco para la composición del escritorio, las aplicaciones pueden usar estadísticas presentes proporcionadas por DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-133">In Windows Vista, where DWM maintains a corresponding copy of the frame surface for Desktop composition, applications can use present statistics provided by DWM.</span></span> <span data-ttu-id="9f709-134">Este método de obtención de estadísticas actuales seguirá estando disponible en Windows 7 para las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="9f709-134">This method of obtaining present statistics will still be available in Windows 7 for existing applications.</span></span>

<span data-ttu-id="9f709-135">En Windows 7, las aplicaciones basadas en Direct3D 9Ex que adopten Flip Model deben usar las API de D3D9Ex para obtener estadísticas actuales.</span><span class="sxs-lookup"><span data-stu-id="9f709-135">In Windows 7, Direct3D 9Ex-based applications that adopt Flip Model should use D3D9Ex APIs to obtain present statistics.</span></span> <span data-ttu-id="9f709-136">Cuando DWM está habilitado, las aplicaciones en modo de ventana y de Direct3D 9Ex de modo exclusivo de pantalla completa pueden esperar la misma información de estadísticas presente al usar Flip Model.</span><span class="sxs-lookup"><span data-stu-id="9f709-136">When DWM is enabled, windowed mode and full-screen exclusive mode Direct3D 9Ex applications can expect the same present statistics information when using Flip Model.</span></span> <span data-ttu-id="9f709-137">Las estadísticas presentes del modelo Flip de Direct3D 9Ex permiten que las aplicaciones consulten estadísticas presentes en tiempo real, en lugar de después de que el fotograma se muestre en la pantalla. la misma información de estadísticas presentes está disponible para las aplicaciones de modo de ventana Flip-Model habilitadas como aplicaciones de pantalla completa; una marca agregada en las API de D3D9Ex permite a las aplicaciones de Flip Model descartar eficazmente los fotogramas en tiempo de presentación.</span><span class="sxs-lookup"><span data-stu-id="9f709-137">Direct3D 9Ex Flip Model present statistics enable applications to query for present statistics in real time, rather than after the frame has been shown on screen; the same present statistics information is available for windowed-mode Flip-Model enabled applications as full-screen applications; an added flag in D3D9Ex APIs allows Flip Model applications to effectively discard late frames at presentation time.</span></span>

<span data-ttu-id="9f709-138">El modelo Flip de Direct3D 9Ex debe usarse en las nuevas aplicaciones de presentación basadas en la velocidad de fotogramas y el vídeo que tienen como destino Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f709-138">Direct3D 9Ex Flip Model should be used by new video or frame rate-based presentation applications that target Windows 7.</span></span> <span data-ttu-id="9f709-139">Debido a la sincronización entre DWM y el tiempo de ejecución de Direct3D 9Ex, las aplicaciones que usan Flip Model deben especificar entre 2 y 4 búferes retroversos para garantizar una presentación fluida.</span><span class="sxs-lookup"><span data-stu-id="9f709-139">Because of the synchronization between DWM and the Direct3D 9Ex runtime, applications that use Flip Model should specify between 2 to 4 backbuffers to ensure smooth presentation.</span></span> <span data-ttu-id="9f709-140">Las aplicaciones que usan información de estadísticas presentes se beneficiarán del uso de las mejoras de las estadísticas presentes de Flip Model enabled.</span><span class="sxs-lookup"><span data-stu-id="9f709-140">Those applications that use present statistics information will benefit from using Flip Model enabled present statistics enhancements.</span></span>

## <a name="direct3d-9ex-flip-mode-presentation"></a><span data-ttu-id="9f709-141">Presentación del modo Flip de Direct3D 9EX</span><span class="sxs-lookup"><span data-stu-id="9f709-141">Direct3D 9EX Flip Mode Presentation</span></span>

<span data-ttu-id="9f709-142">Las mejoras de rendimiento del modo de volteo 9Ex de Direct3D son significativas en el sistema cuando DWM está activado y cuando la aplicación está en modo de ventana, en lugar de en modo exclusivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9f709-142">Performance improvements of Direct3D 9Ex Flip Mode Present are significant on the system when DWM is on and when the application is in windowed mode, rather than in full screen exclusive mode.</span></span> <span data-ttu-id="9f709-143">En la siguiente tabla y ilustración se muestra una comparación simplificada de los usos de ancho de banda de memoria y las lecturas y escrituras del sistema que eligen Flip Model frente al modelo de uso predeterminado BLT.</span><span class="sxs-lookup"><span data-stu-id="9f709-143">The following table and illustration show a simplified comparison of memory bandwidth usages and system reads and writes of windowed applications that choose Flip Model versus the default usage Blt Model.</span></span>



| <span data-ttu-id="9f709-144">Modo BLT presente en DWM</span><span class="sxs-lookup"><span data-stu-id="9f709-144">Blt mode present to DWM</span></span>                                                                                                 | <span data-ttu-id="9f709-145">D3D9Ex modo de volteo presente en DWM</span><span class="sxs-lookup"><span data-stu-id="9f709-145">D3D9Ex Flip Mode Present to DWM</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="9f709-146">1. la aplicación actualiza su marco (escritura)</span><span class="sxs-lookup"><span data-stu-id="9f709-146">1. The application updates its frame (Write)</span></span><br/>                                                                 | <span data-ttu-id="9f709-147">1. la aplicación actualiza su marco (escritura)</span><span class="sxs-lookup"><span data-stu-id="9f709-147">1. The application updates its frame (Write)</span></span><br/>                     |
| <span data-ttu-id="9f709-148">2. el tiempo de ejecución de Direct3D copia el contenido de la superficie en una superficie de redirección de DWM (lectura, escritura)</span><span class="sxs-lookup"><span data-stu-id="9f709-148">2. Direct3D runtime copies surface contents to a DWM redirection surface (Read, Write)</span></span><br/>                       | <span data-ttu-id="9f709-149">2. el tiempo de ejecución de Direct3D pasa la superficie de aplicación a DWM</span><span class="sxs-lookup"><span data-stu-id="9f709-149">2. Direct3D runtime passes the application surface to DWM</span></span><br/>        |
| <span data-ttu-id="9f709-150">3. una vez completada la copia de la superficie compartida, DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)</span><span class="sxs-lookup"><span data-stu-id="9f709-150">3. After the shared surface copy is completed, DWM renders the application surface onto screen (Read, Write)</span></span><br/> | <span data-ttu-id="9f709-151">3. DWM representa la superficie de la aplicación en la pantalla (lectura, escritura)</span><span class="sxs-lookup"><span data-stu-id="9f709-151">3. DWM renders the application surface onto screen (Read, Write)</span></span><br/> |



 

![Ilustración de una comparación del modelo BLT y el modelo Flip](images/blt-flip-mode-present.png)

<span data-ttu-id="9f709-153">El modo de volteo está presente reduce el uso de memoria del sistema al reducir el número de lecturas y escrituras realizadas por el tiempo de ejecución de Direct3D para la composición de fotogramas en ventanas por DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-153">Flip Mode Present reduces system memory usage by reducing the number of reads and writes by the Direct3D runtime for the windowed frame composition by DWM.</span></span> <span data-ttu-id="9f709-154">Esto reduce el consumo de energía del sistema y el uso de memoria general.</span><span class="sxs-lookup"><span data-stu-id="9f709-154">This reduces the system power consumption and overall memory usage.</span></span>

<span data-ttu-id="9f709-155">Las aplicaciones pueden beneficiarse de las mejoras de las estadísticas presentes del modo Flip de Direct3D 9Ex cuando DWM está activado, independientemente de si la aplicación está en modo de ventana o en el modo exclusivo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="9f709-155">Applications can take advantage of Direct3D 9Ex Flip Mode present statistics enhancements when DWM is on, regardless of whether the application is in windowed mode or in full screen exclusive mode.</span></span>

## <a name="programming-model-and-apis"></a><span data-ttu-id="9f709-156">Modelo de programación y API</span><span class="sxs-lookup"><span data-stu-id="9f709-156">Programming Model and APIs</span></span>

<span data-ttu-id="9f709-157">Las nuevas aplicaciones que usan las API de Direct3D 9Ex en Windows 7 pueden aprovechar las ventajas de la memoria y el ahorro de energía y de la presentación mejorada que ofrece el modo Flip cuando se ejecuta en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9f709-157">New video or frame rate-gauging applications that use Direct3D 9Ex APIs on Windows 7 can take advantage of the memory and power savings and of the improved presentation offered by Flip Mode Present when running on Windows 7.</span></span> <span data-ttu-id="9f709-158">(Cuando se ejecuta en versiones anteriores de Windows, el tiempo de ejecución de Direct3D utiliza de forma predeterminada la aplicación en el modo BLT).</span><span class="sxs-lookup"><span data-stu-id="9f709-158">(When running on previous Windows versions, the Direct3D runtime defaults the application to Blt Mode Present.)</span></span>

<span data-ttu-id="9f709-159">El modo de volteo supone que la aplicación puede aprovechar las ventajas de los mecanismos de corrección y comentarios de estadísticas presentes en tiempo real cuando DWM está activado.</span><span class="sxs-lookup"><span data-stu-id="9f709-159">Flip Mode Present entails that the application can take advantage of real-time present statistics feedback and correction mechanisms when DWM is on.</span></span> <span data-ttu-id="9f709-160">Sin embargo, las aplicaciones que usan el modo de volteo presente deben tener en cuenta las limitaciones cuando usan la representación simultánea de la API de GDI.</span><span class="sxs-lookup"><span data-stu-id="9f709-160">However, applications that use Flip Mode Present should be aware of limitations when they use concurrent GDI API rendering.</span></span>

<span data-ttu-id="9f709-161">Puede modificar las aplicaciones existentes para aprovechar el modo de volteo presente, con las mismas ventajas y advertencias que las aplicaciones recién desarrolladas.</span><span class="sxs-lookup"><span data-stu-id="9f709-161">You can modify existing applications to take advantage of Flip Mode Present, with the same benefits and caveats as the newly developed applications.</span></span>

### <a name="how-to-opt-into-the-direct3d-9ex-flip-model"></a><span data-ttu-id="9f709-162">Cómo participar en el modelo Flip de Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="9f709-162">How to Opt Into the Direct3D 9Ex Flip Model</span></span>

<span data-ttu-id="9f709-163">Las aplicaciones de Direct3D 9Ex que tienen como destino Windows 7 pueden participar en el modelo Flip mediante la creación de la cadena de intercambio con el valor de enumeración [**\_ FLIPEX de D3DSWAPEFFECT**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="9f709-163">Direct3D 9Ex applications that target Windows 7 can opt into the Flip Model by creating the swap chain with the [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) enumeration value.</span></span> <span data-ttu-id="9f709-164">Para participar en el modelo Flip, las aplicaciones especifican la estructura de [**\_ parámetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) y, a continuación, pasan un puntero a esta estructura cuando llaman a la API [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="9f709-164">To opt into the Flip Model, applications specify the [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) structure, and then pass a pointer to this structure when they call the [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) API.</span></span> <span data-ttu-id="9f709-165">En esta sección se describe cómo las aplicaciones que tienen como destino Windows 7 usan **IDirect3D9Ex:: CreateDeviceEx** para participar en el modelo de volteo.</span><span class="sxs-lookup"><span data-stu-id="9f709-165">This section describes how applications that target Windows 7 use **IDirect3D9Ex::CreateDeviceEx** to opt into the Flip Model.</span></span> <span data-ttu-id="9f709-166">Para obtener más información sobre la API **IDirect3D9Ex:: CreateDeviceEx** , vea **IDirect3D9Ex:: CreateDeviceEx en MSDN**.</span><span class="sxs-lookup"><span data-stu-id="9f709-166">For more information about the **IDirect3D9Ex::CreateDeviceEx** API, see **IDirect3D9Ex::CreateDeviceEx on MSDN**.</span></span>

<span data-ttu-id="9f709-167">Para mayor comodidad, aquí se repite la sintaxis de [**\_ los parámetros de D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters) y [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="9f709-167">For convenience, the syntax of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) and [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

``` syntax
typedef struct D3DPRESENT_PARAMETERS {
    UINT BackBufferWidth, BackBufferHeight;
    D3DFORMAT BackBufferFormat;
    UINT BackBufferCount;
    D3DMULTISAMPLE_TYPE MultiSampleType;
    DWORD MultiSampleQuality;
    D3DSWAPEFFECT SwapEffect;
    HWND hDeviceWindow;
    BOOL Windowed;
    BOOL EnableAutoDepthStencil;
    D3DFORMAT AutoDepthStencilFormat;
    DWORD Flags;
    UINT FullScreen_RefreshRateInHz;
    UINT PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```

<span data-ttu-id="9f709-168">Cuando se modifican las aplicaciones de Direct3D 9Ex para Windows 7 para participar en el modelo Flip, se deben tener en cuenta los siguientes elementos sobre los miembros especificados de los [**\_ parámetros D3DPRESENT**](/windows/desktop/direct3d9/d3dpresent-parameters):</span><span class="sxs-lookup"><span data-stu-id="9f709-168">When you modify Direct3D 9Ex applications for Windows 7 to opt into the Flip Model, you should consider the following items about the specified members of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters):</span></span>

<dl> <dt>

<span data-ttu-id="9f709-169">**BackBufferCount**</span><span class="sxs-lookup"><span data-stu-id="9f709-169">**BackBufferCount**</span></span>
</dt> <dd>

<span data-ttu-id="9f709-170">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9f709-170">(Windows 7 Only)</span></span>

<span data-ttu-id="9f709-171">Cuando **SwapEffect** se establece en el nuevo tipo de efecto de cadena de intercambio de D3DSWAPEFFECT \_ FLIPEX, el número de búferes de reserva debe ser igual o mayor que 2, para evitar una reducción del rendimiento de la aplicación como resultado de la espera en el búfer actual anterior para que DWM lo libere.</span><span class="sxs-lookup"><span data-stu-id="9f709-171">When **SwapEffect** is set to the new D3DSWAPEFFECT\_FLIPEX swap chain effect type, the back buffer count should be equal or greater than 2, to prevent an application performance penalty as a result of waiting on the previous Present buffer to be released by DWM.</span></span>

<span data-ttu-id="9f709-172">Cuando la aplicación también usa estadísticas presentes asociadas a D3DSWAPEFFECT \_ FLIPEX, se recomienda establecer el número de búferes de reserva en de 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="9f709-172">When the application also uses present statistics associated with D3DSWAPEFFECT\_FLIPEX, we recommend that you set the back buffer count to from 2 to 4.</span></span>

<span data-ttu-id="9f709-173">El uso \_ de D3DSWAPEFFECT FLIPEX en Windows Vista o versiones anteriores del sistema operativo devolverá un error desde [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="9f709-173">Using D3DSWAPEFFECT\_FLIPEX on Windows Vista or previous operating system versions will return fail from [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

<span data-ttu-id="9f709-174">**SwapEffect**</span><span class="sxs-lookup"><span data-stu-id="9f709-174">**SwapEffect**</span></span>
</dt> <dd>

<span data-ttu-id="9f709-175">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9f709-175">(Windows 7 Only)</span></span>

<span data-ttu-id="9f709-176">El nuevo tipo de efecto de cadena de intercambio de D3DSWAPEFFECT \_ FLIPEX designa cuando una aplicación está adoptando el modo de volteo presente para DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-176">The new D3DSWAPEFFECT\_FLIPEX swap chain effect type designates when an application is adopting Flip Mode Present to DWM.</span></span> <span data-ttu-id="9f709-177">Permite a la aplicación un uso más eficaz de la memoria y la capacidad, y también permite a la aplicación aprovechar las estadísticas presentes en modo de pantalla completa en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="9f709-177">It allows the application more efficient usage of memory and power, and also enables the application to take advantage of full-screen present statistics in windowed mode.</span></span> <span data-ttu-id="9f709-178">El comportamiento de la aplicación de pantalla completa no se ve afectado.</span><span class="sxs-lookup"><span data-stu-id="9f709-178">Full-screen application behavior is not affected.</span></span> <span data-ttu-id="9f709-179">Si windowed está establecido en **true** y **SwapEffect** se establece en D3DSWAPEFFECT \_ FLIPEX, el tiempo de ejecución crea un búfer de reserva adicional y gira el identificador que pertenece al búfer que se convierte en el búfer frontal en el momento de la presentación.</span><span class="sxs-lookup"><span data-stu-id="9f709-179">If Windowed is set to **TRUE** and **SwapEffect** is set to D3DSWAPEFFECT\_FLIPEX, the runtime creates one extra back buffer and rotates whichever handle belongs to the buffer that becomes the front buffer at presentation time.</span></span>

</dd> <dt>

<span data-ttu-id="9f709-180">**Marcas**</span><span class="sxs-lookup"><span data-stu-id="9f709-180">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9f709-181">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9f709-181">(Windows 7 Only)</span></span>

<span data-ttu-id="9f709-182">No se puede establecer la marca de [ \_ búfer de \_ reserva con bloqueos D3DPRESENTFLAG](/windows/desktop/direct3d9/d3dpresentflag) si **SwapEffect** está establecido en el tipo de efecto nueva cadena de intercambio de [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) .</span><span class="sxs-lookup"><span data-stu-id="9f709-182">The [D3DPRESENTFLAG\_LOCKABLE\_BACKBUFFER](/windows/desktop/direct3d9/d3dpresentflag) flag cannot be set if **SwapEffect** is set to the new [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chain effect type.</span></span>

</dd> </dl>

### <a name="design-guidelines-for-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="9f709-183">Instrucciones de diseño para aplicaciones de modelo Flip 9Ex de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9f709-183">Design Guidelines for Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="9f709-184">Siga las instrucciones de las secciones siguientes para diseñar las aplicaciones de modelo Flip de Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="9f709-184">Use the guidelines in the following sections to design your Direct3D 9Ex Flip Model applications.</span></span>

### <a name="use-flip-mode-present-in-a-separate-hwnd-from-blt-mode-present"></a><span data-ttu-id="9f709-185">Usar el modo de volteo presente en un HWND independiente del modo BLT presente</span><span class="sxs-lookup"><span data-stu-id="9f709-185">Use Flip Mode Present in a Separate HWND from Blt Mode Present</span></span>

<span data-ttu-id="9f709-186">Las aplicaciones deben usar el modo Flip de Direct3D 9Ex presente en un HWND que no sea también dirigido por otras API, incluido el modo BLT presente Direct3D 9Ex, otras versiones de Direct3D o GDI.</span><span class="sxs-lookup"><span data-stu-id="9f709-186">Applications should use Direct3D 9Ex Flip Mode Present in an HWND that is not also targeted by other APIs, including Blt Mode Present Direct3D 9Ex, other versions of Direct3D, or GDI.</span></span> <span data-ttu-id="9f709-187">El modo de volteo presente se puede usar para presentar a las ventanas secundarias; es decir, las aplicaciones pueden usar Flip Model cuando no está mezclado con el modelo BLT en el mismo HWND, tal y como se muestra en las siguientes ilustraciones.</span><span class="sxs-lookup"><span data-stu-id="9f709-187">Flip Mode Present can be used to present to child windows; that is, applications can use Flip Model when it is not mixed with Blt Model in the same HWND, as shown in the following illustrations.</span></span>

![Ilustración de la ventana primaria de Direct3D y una ventana secundaria de GDI, cada una con su propio HWND](images/parent-d3d.png)

![Ilustración de la ventana primaria de GDI y una ventana secundaria de Direct3D, cada una con su propio HWND](images/parent-gdi.png)

<span data-ttu-id="9f709-190">Dado que el modelo BLT mantiene una copia adicional de la superficie, se pueden agregar GDI y otros contenidos de Direct3D al mismo HWND a través de actualizaciones por etapas de Direct3D y GDI.</span><span class="sxs-lookup"><span data-stu-id="9f709-190">Because Blt Model maintains an additional copy of the surface, GDI and other Direct3D contents can be added to the same HWND through piecemeal updates from Direct3D and GDI.</span></span> <span data-ttu-id="9f709-191">Con el modelo Flip, solo estará visible el contenido de Direct3D 9Ex en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) cadenas de intercambio que se pasan a DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-191">Using the Flip Model, only Direct3D 9Ex content in [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) swap chains that are passed to DWM will be visible.</span></span> <span data-ttu-id="9f709-192">Se omitirán todas las demás actualizaciones de contenido de la modelo de Direct3D o GDI, tal y como se muestra en las ilustraciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="9f709-192">All other Blt Model Direct3D or GDI content updates will be ignored, as shown in the following illustrations.</span></span>

![Ilustración del texto GDI que podría no mostrarse si se usa Flip Model y el contenido de Direct3D y GDI está en el mismo HWND](images/d3d-gdi-same-hwnd.png)

![Ilustración del contenido de Direct3D y GDI en el que DWM está habilitado y la aplicación está en modo de ventana](images/d3d-gdinotext-same-hwnd.png)

<span data-ttu-id="9f709-195">Por lo tanto, el modelo de volteo debe estar habilitado para las superficies de búferes de cadena de intercambio en las que el modelo de volteo de Direct3D 9Ex se representa en todo el HWND.</span><span class="sxs-lookup"><span data-stu-id="9f709-195">Therefore, Flip Model should be enabled for swap chain buffers surfaces where the Direct3D 9Ex Flip Model alone renders to the entire HWND.</span></span>

### <a name="do-not-use-flip-model-with-gdis-scrollwindow-or-scrollwindowex"></a><span data-ttu-id="9f709-196">No usar Flip Model con ScrollWindow o ScrollWindowEx de GDI</span><span class="sxs-lookup"><span data-stu-id="9f709-196">Do Not Use Flip Model with GDI's ScrollWindow or ScrollWindowEx</span></span>

<span data-ttu-id="9f709-197">Algunas aplicaciones de Direct3D 9Ex usan las funciones ScrollWindow o ScrollWindowEx de GDI para actualizar el contenido de la ventana cuando se desencadena un evento de desplazamiento del usuario.</span><span class="sxs-lookup"><span data-stu-id="9f709-197">Some Direct3D 9Ex applications use GDI's ScrollWindow or ScrollWindowEx functions to update window contents when a user scroll event is triggered.</span></span> <span data-ttu-id="9f709-198">ScrollWindow y ScrollWindowEx realizan blts de contenido de la ventana en la pantalla cuando se desplaza una ventana.</span><span class="sxs-lookup"><span data-stu-id="9f709-198">ScrollWindow and ScrollWindowEx perform blts of window contents on screen as a window is scrolled.</span></span> <span data-ttu-id="9f709-199">Estas funciones también requieren las actualizaciones del modelo BLT para el contenido de 9Ex y de GDI.</span><span class="sxs-lookup"><span data-stu-id="9f709-199">These functions also require Blt Model updates for GDI and Direct3D 9Ex content.</span></span> <span data-ttu-id="9f709-200">Las aplicaciones que usan cualquiera de las funciones no mostrarán necesariamente el desplazamiento del contenido de la ventana visible en la pantalla cuando la aplicación esté en modo de ventana y se habilite DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-200">Applications that use either function will not necessarily display visible window contents scrolling on screen when the application is in windowed mode and DWM is enabled.</span></span> <span data-ttu-id="9f709-201">Se recomienda no usar las API ScrollWindow y ScrollWindowEx de GDI en las aplicaciones y, en su lugar, volver a dibujar el contenido en pantalla en respuesta a un desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="9f709-201">We recommend that you not use GDI's ScrollWindow and ScrollWindowEx APIs in your applications, and instead redraw their contents on screen in response to scrolling.</span></span>

### <a name="use-one-d3dswapeffect_flipex-swap-chain-per-hwnd"></a><span data-ttu-id="9f709-202">Usar una cadena de intercambio de D3DSWAPEFFECT \_ FLIPEX por HWND</span><span class="sxs-lookup"><span data-stu-id="9f709-202">Use One D3DSWAPEFFECT\_FLIPEX Swap Chain per HWND</span></span>

<span data-ttu-id="9f709-203">Las aplicaciones que utilizan Flip Model no deben usar varias cadenas de intercambio de volteo del modelo que tienen como destino el mismo HWND.</span><span class="sxs-lookup"><span data-stu-id="9f709-203">Applications that use Flip Model should not use multiple Flip Model swap chains targeting the same HWND.</span></span>

### <a name="frame-synchronization-of-direct3d-9ex-flip-model-applications"></a><span data-ttu-id="9f709-204">Sincronización de fotogramas de aplicaciones de modelo Flip 9Ex de Direct3D</span><span class="sxs-lookup"><span data-stu-id="9f709-204">Frame Synchronization of Direct3D 9Ex Flip Model Applications</span></span>

<span data-ttu-id="9f709-205">Las estadísticas presentes son información de temporización de fotogramas que usan las aplicaciones multimedia para sincronizar secuencias de audio y vídeo y recuperarse de problemas de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9f709-205">Present statistics are frame timing information that media applications use to synchronize video and audio streams and recover from video playback glitches.</span></span> <span data-ttu-id="9f709-206">Para habilitar la disponibilidad de las estadísticas presentes, la aplicación 9Ex de Direct3D debe asegurarse de que el parámetro *BehaviorFlags* que la aplicación pasa a [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contiene la marca de comportamiento del dispositivo [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span><span class="sxs-lookup"><span data-stu-id="9f709-206">To enable present statistics availability, the Direct3D 9Ex application must ensure that the *BehaviorFlags* parameter that the application passes to [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) contains the device behavior flag [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate).</span></span>

<span data-ttu-id="9f709-207">Para mayor comodidad, aquí se repite la sintaxis de [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) .</span><span class="sxs-lookup"><span data-stu-id="9f709-207">For convenience, the syntax of [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) is repeated here.</span></span>

``` syntax
HRESULT CreateDeviceEx(
  UINT Adapter,
  D3DDEVTYPE DeviceType,
  HWND hFocusWindow,
  DWORD BehaviorFlags,
  D3DPRESENT_PARAMETERS* pPresentationParameters,
  D3DDISPLAYMODEEX *pFullscreenDisplayMode,
  IDirect3DDevice9Ex **ppReturnedDeviceInterface
);
```

<span data-ttu-id="9f709-208">El modelo Flip de Direct3D 9Ex agrega la marca de presentación [D3DPRESENT \_ FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) que aplica el comportamiento de marca de presentación [ \_ \_ inmediata de intervalo de D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) .</span><span class="sxs-lookup"><span data-stu-id="9f709-208">Direct3D 9Ex Flip Model adds the [D3DPRESENT\_FORCEIMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation flag that enforces the [D3DPRESENT\_INTERVAL\_IMMEDIATE](/windows/desktop/direct3d9/d3dpresent) presentation-flag behavior.</span></span> <span data-ttu-id="9f709-209">La aplicación Direct3D 9Ex especifica estas marcas de presentación en el parámetro *dwFlags* que la aplicación pasa a [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="9f709-209">The Direct3D 9Ex application specifies these presentation flags in the *dwFlags* parameter that the application passes to [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex), as shown here.</span></span>

``` syntax
HRESULT PresentEx(
  CONST RECT *pSourceRect,
  CONST RECT *pDestRect,
  HWND hDestWindowOverride,
  CONST RGNDATA *pDirtyRegion,
  DWORD dwFlags
);
```

<span data-ttu-id="9f709-210">Al modificar la aplicación Direct3D 9Ex para Windows 7, debe tener en cuenta la siguiente información sobre las marcas de presentación [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) especificadas:</span><span class="sxs-lookup"><span data-stu-id="9f709-210">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the specified [D3DPRESENT](/windows/desktop/direct3d9/d3dpresent) presentation flags:</span></span>

<dl> <dt>

[<span data-ttu-id="9f709-211">D3DPRESENT \_ DONOTFLIP</span><span class="sxs-lookup"><span data-stu-id="9f709-211">D3DPRESENT\_DONOTFLIP</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="9f709-212">Esta marca solo está disponible en modo de pantalla completa o</span><span class="sxs-lookup"><span data-stu-id="9f709-212">This flag is available only in full-screen mode or</span></span>

<span data-ttu-id="9f709-213">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9f709-213">(Windows 7 Only)</span></span>

<span data-ttu-id="9f709-214">Cuando la aplicación establece el miembro **SwapEffect** de [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="9f709-214">when the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>

</dd> <dt>

[<span data-ttu-id="9f709-215">D3DPRESENT \_ FORCEIMMEDIATE</span><span class="sxs-lookup"><span data-stu-id="9f709-215">D3DPRESENT\_FORCEIMMEDIATE</span></span>](/windows/desktop/direct3d9/d3dpresent)
</dt> <dd>

<span data-ttu-id="9f709-216">(Solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="9f709-216">(Windows 7 Only)</span></span>

<span data-ttu-id="9f709-217">Esta marca solo se puede especificar si la aplicación establece el miembro **SwapEffect** de [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="9f709-217">This flag can be specified only if the application sets the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span> <span data-ttu-id="9f709-218">La aplicación puede usar esta marca para actualizar inmediatamente una superficie con varios fotogramas más adelante en la cola de la presentación de DWM, omitiendo básicamente los marcos intermedios.</span><span class="sxs-lookup"><span data-stu-id="9f709-218">The application can use this flag to immediately update a surface with several frames later in the DWM Present queue, essentially skipping intermediate frames.</span></span>

<span data-ttu-id="9f709-219">Las aplicaciones habilitadas para FlipEx en ventanas pueden usar esta marca para actualizar inmediatamente una superficie con un marco que se encuentra más adelante en la cola de presentación de DWM, omitiendo los marcos intermedios.</span><span class="sxs-lookup"><span data-stu-id="9f709-219">Windowed FlipEx-enabled applications can use this flag to immediately update a surface with a frame that is later in the DWM Present queue, skipping intermediate frames.</span></span> <span data-ttu-id="9f709-220">Esto es especialmente útil para las aplicaciones multimedia que desean descartar fotogramas detectados en tiempo de espera y presentan fotogramas posteriores en el momento de la composición.</span><span class="sxs-lookup"><span data-stu-id="9f709-220">This is especially useful for media applications that want to discard frames that have been detected as late and present subsequent frames at composition time.</span></span> <span data-ttu-id="9f709-221">[**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) devuelve un error de parámetro no válido si esta marca no se ha especificado correctamente.</span><span class="sxs-lookup"><span data-stu-id="9f709-221">[**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) returns invalid parameter error if this flag is improperly specified.</span></span>

</dd> </dl>

<span data-ttu-id="9f709-222">Para obtener información de estadísticas presentes, la aplicación obtiene la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) llamando a la API [**IDirect3DSwapChain9Ex:: GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9f709-222">To obtain present statistics information, the application obtains the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure by calling the [**IDirect3DSwapChain9Ex::GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) API.</span></span>

<span data-ttu-id="9f709-223">La estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) contiene estadísticas sobre [**IDirect3DDevice9Ex::P llamadas resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) .</span><span class="sxs-lookup"><span data-stu-id="9f709-223">The [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure contains statistics about [**IDirect3DDevice9Ex::PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) calls.</span></span> <span data-ttu-id="9f709-224">El dispositivo se debe crear mediante una llamada a [**IDirect3D9Ex:: CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) con la marca [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) .</span><span class="sxs-lookup"><span data-stu-id="9f709-224">The device must be created by using a [**IDirect3D9Ex::CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex) call with the [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) flag.</span></span> <span data-ttu-id="9f709-225">De lo contrario, los datos devueltos por [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) no están definidos.</span><span class="sxs-lookup"><span data-stu-id="9f709-225">Otherwise, the data returned by [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is undefined.</span></span> <span data-ttu-id="9f709-226">Una cadena de intercambio 9Ex de Direct3D habilitada para Flip Model proporciona información de estadísticas presentes en los modos de pantalla completa y de ventana.</span><span class="sxs-lookup"><span data-stu-id="9f709-226">A Flip-Model-enabled Direct3D 9Ex swap chain provides present statistics information in both windowed and full-screen modes.</span></span>

<span data-ttu-id="9f709-227">En el caso de las cadenas de intercambio 9Ex de Direct3D habilitadas para BLT-Model en modo de ventana, todos los valores de estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) serán ceros.</span><span class="sxs-lookup"><span data-stu-id="9f709-227">For Blt-Model-enabled Direct3D 9Ex swap chains in windowed mode, all [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure values will be zeroes.</span></span>

<span data-ttu-id="9f709-228">En el caso de las estadísticas presentes en FlipEx, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) devuelve D3DERR \_ \_ estadísticas presentes \_ en las siguientes situaciones:</span><span class="sxs-lookup"><span data-stu-id="9f709-228">For FlipEx present statistics, [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) returns D3DERR\_PRESENT\_STATISTICS\_DISJOINT in the following situations:</span></span>

-   <span data-ttu-id="9f709-229">Primera llamada a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) Ever, que indica el principio de una secuencia</span><span class="sxs-lookup"><span data-stu-id="9f709-229">First call to [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) ever, which indicates the beginning of a sequence</span></span>
-   <span data-ttu-id="9f709-230">Transición de DWM de on a OFF</span><span class="sxs-lookup"><span data-stu-id="9f709-230">DWM transition from on to off</span></span>
-   <span data-ttu-id="9f709-231">Cambio de modo: modo de ventana a o desde pantalla completa o pantalla completa hasta transiciones de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="9f709-231">Mode change: either windowed mode to or from full screen or full screen to full screen transitions</span></span>

<span data-ttu-id="9f709-232">Para mayor comodidad, aquí se repite la sintaxis de [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="9f709-232">For convenience, the syntax of [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) is repeated here.</span></span>

``` syntax
HRESULT GetPresentStatistics(
  D3DPRESENTSTATS * pPresentationStatistics
);
```

<span data-ttu-id="9f709-233">El método [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) devuelve el último PresentCount, es decir, el identificador actual de la última llamada presente correcta realizada por un dispositivo de pantalla que está asociado a la cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="9f709-233">The [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) method returns the last PresentCount, that is, the Present ID of the last successful Present call that was made by a display device that is associated with the swap chain.</span></span> <span data-ttu-id="9f709-234">Este identificador actual es el valor del miembro **PresentCount** de la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) .</span><span class="sxs-lookup"><span data-stu-id="9f709-234">This Present ID is the value of the **PresentCount** member of the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure.</span></span> <span data-ttu-id="9f709-235">En el caso de las cadenas de intercambio 9Ex de Direct3D habilitadas para BLT-Model, mientras que en el modo de ventana, todos los valores de estructura **D3DPRESENTSTATS** serán ceros.</span><span class="sxs-lookup"><span data-stu-id="9f709-235">For Blt-Model-enabled Direct3D 9Ex swap chains, while in windowed mode, all **D3DPRESENTSTATS** structure values will be zeroes.</span></span>

<span data-ttu-id="9f709-236">Para mayor comodidad, aquí se repite la sintaxis de [**IDirect3DSwapChain9Ex:: GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) .</span><span class="sxs-lookup"><span data-stu-id="9f709-236">For convenience, the syntax of [**IDirect3DSwapChain9Ex::GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) is repeated here.</span></span>

``` syntax
HRESULT GetLastPresentCount(
  UINT * pLastPresentCount
);
```

<span data-ttu-id="9f709-237">Al modificar la aplicación Direct3D 9Ex para Windows 7, debe tener en cuenta la siguiente información sobre la estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) :</span><span class="sxs-lookup"><span data-stu-id="9f709-237">When you modify your Direct3D 9Ex application for Windows 7, you should consider the following information about the [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure:</span></span>

-   <span data-ttu-id="9f709-238">El valor PresentCount que devuelve [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) no se actualiza cuando una llamada [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTWAIT especificada en el parámetro *dwFlags* devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="9f709-238">The PresentCount value that [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount) returns does not update when a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) call with D3DPRESENT\_DONOTWAIT specified in the *dwFlags* parameter returns failure.</span></span>
-   <span data-ttu-id="9f709-239">Cuando se llama a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, una llamada a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se realiza correctamente, pero no devuelve una estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) actualizada cuando la aplicación está en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="9f709-239">When [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) is called with D3DPRESENT\_DONOTFLIP, a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>
-   <span data-ttu-id="9f709-240">**PresentRefreshCount** frente a **SyncRefreshCount** en [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span><span class="sxs-lookup"><span data-stu-id="9f709-240">**PresentRefreshCount** versus **SyncRefreshCount** in [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats):</span></span>
    -   <span data-ttu-id="9f709-241">**PresentRefreshCount** es igual a **SyncRefreshCount** cuando la aplicación presenta en cada VSYNC.</span><span class="sxs-lookup"><span data-stu-id="9f709-241">**PresentRefreshCount** is equal to **SyncRefreshCount** when the application presents on every vsync.</span></span>
    -   <span data-ttu-id="9f709-242">**SyncRefreshCount** se obtiene en el intervalo de VSYNC cuando se envió el presente, **SyncQPCTime** es aproximadamente el tiempo asociado con el intervalo de VSYNC.</span><span class="sxs-lookup"><span data-stu-id="9f709-242">**SyncRefreshCount** is obtained on the vsync interval when the present was submitted, **SyncQPCTime** is approximately the time associated with the vsync interval.</span></span>

``` syntax
typedef struct _D3DPRESENTSTATS {
    UINT PresentCount;
    UINT PresentRefreshCount;
    UINT SyncRefreshCount;
    LARGE_INTEGER SyncQPCTime;
    LARGE_INTEGER SyncGPUTime;
} D3DPRESENTSTATS;
```

### <a name="frame-synchronization-for-windowed-applications-when-dwm-is-off"></a><span data-ttu-id="9f709-243">Sincronización de fotogramas para aplicaciones en ventanas cuando DWM está desactivado</span><span class="sxs-lookup"><span data-stu-id="9f709-243">Frame Synchronization for Windowed Applications When DWM is Off</span></span>

<span data-ttu-id="9f709-244">Cuando DWM está desactivado, las aplicaciones en ventanas se muestran directamente en la pantalla del monitor sin pasar por una cadena de volteo.</span><span class="sxs-lookup"><span data-stu-id="9f709-244">When DWM is off, windowed applications display directly to the monitor screen without going through a flip chain.</span></span> <span data-ttu-id="9f709-245">En Windows Vista, no se admite la obtención de información de estadísticas de fotogramas para aplicaciones en ventanas cuando DWM está desactivado.</span><span class="sxs-lookup"><span data-stu-id="9f709-245">In Windows Vista, there is no support for obtaining frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="9f709-246">Para mantener una API en la que las aplicaciones no necesitan ser compatibles con DWM, Windows 7 devolverá información de estadísticas de fotogramas para aplicaciones en ventanas cuando DWM esté desactivado.</span><span class="sxs-lookup"><span data-stu-id="9f709-246">To maintain an API where applications need not be DWM- aware, Windows 7 will return frame statistics information for windowed applications when DWM is off.</span></span> <span data-ttu-id="9f709-247">Las estadísticas de fotogramas que se devuelven cuando DWM es OFF solo se estiman.</span><span class="sxs-lookup"><span data-stu-id="9f709-247">The frame statistics returned when DWM is off are estimations only.</span></span>

## <a name="walk-through-of-a-direct3d-9ex-flip-model-and-present-statistics-sample"></a><span data-ttu-id="9f709-248">Walk-Through de un modelo Flip 9Ex de Direct3D y el ejemplo present Statistics</span><span class="sxs-lookup"><span data-stu-id="9f709-248">Walk-Through of a Direct3D 9Ex Flip Model and Present Statistics Sample</span></span>

<span data-ttu-id="9f709-249">**Para participar en el ejemplo de presentación de FlipEx para Direct3D 9Ex**</span><span class="sxs-lookup"><span data-stu-id="9f709-249">**To opt into FlipEx presentation for Direct3D 9Ex sample**</span></span>

1.  <span data-ttu-id="9f709-250">Asegúrese de que la aplicación de ejemplo se está ejecutando en la versión del sistema operativo Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9f709-250">Ensure the sample application is running on Windows 7 or later operating system version.</span></span>
2.  <span data-ttu-id="9f709-251">Establezca el miembro **SwapEffect** de [**D3DPRESENT \_ Parameters**](/windows/desktop/direct3d9/d3dpresent-parameters) en [**D3DSWAPEFFECT \_ FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) en una llamada a [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="9f709-251">Set the **SwapEffect** member of [**D3DPRESENT\_PARAMETERS**](/windows/desktop/direct3d9/d3dpresent-parameters) to [**D3DSWAPEFFECT\_FLIPEX**](/windows/desktop/direct3d9/d3dswapeffect) in a call to [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    OSVERSIONINFO version;
    ZeroMemory(&version, sizeof(version));
    version.dwOSVersionInfoSize = sizeof(version);
    GetVersionEx(&version);
    
    // Sample would run only on Win7 or higher
    // Flip Model present and its associated present statistics behavior are only available on Windows 7 or higher operating system
    bool bIsWin7 = (version.dwMajorVersion > 6) || 
        ((version.dwMajorVersion == 6) && (version.dwMinorVersion >= 1));

    if (!bIsWin7)
    {
        MessageBox(NULL, L"This sample requires Windows 7 or higher", NULL, MB_OK);
        return 0;
    }
```



<span data-ttu-id="9f709-252">**Para participar también en FlipEx estadísticas presentes asociadas para el ejemplo de 9Ex de Direct3D**</span><span class="sxs-lookup"><span data-stu-id="9f709-252">**To also opt into FlipEx associated Present Statistics for Direct3D 9Ex sample**</span></span>

-   <span data-ttu-id="9f709-253">Establezca [D3DCREATE \_ enable \_ PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) en el parámetro *BehaviorFlags* de [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span><span class="sxs-lookup"><span data-stu-id="9f709-253">Set [D3DCREATE\_ENABLE\_PRESENTSTATS](/windows/desktop/direct3d9/d3dcreate) in the *BehaviorFlags* parameter of [**CreateDeviceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9ex-createdeviceex).</span></span>


```C++
    // Set up the structure used to create the D3DDevice
    D3DPRESENT_PARAMETERS d3dpp;
    ZeroMemory(&d3dpp, sizeof(d3dpp));

    d3dpp.Windowed = TRUE;
    d3dpp.SwapEffect = D3DSWAPEFFECT_FLIPEX;        // Opts into Flip Model present for D3D9Ex swapchain
    d3dpp.BackBufferFormat = D3DFMT_X8R8G8B8;
    d3dpp.BackBufferWidth = 256;                
    d3dpp.BackBufferHeight = 256;
    d3dpp.BackBufferCount = QUEUE_SIZE;
    d3dpp.PresentationInterval = D3DPRESENT_INTERVAL_ONE;

    g_iWidth = d3dpp.BackBufferWidth;
    g_iHeight = d3dpp.BackBufferHeight;

    // Create the D3DDevice with present statistics enabled - set D3DCREATE_ENABLE_PRESENTSTATS for behaviorFlags parameter
    if(FAILED(g_pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                      D3DCREATE_HARDWARE_VERTEXPROCESSING | D3DCREATE_ENABLE_PRESENTSTATS,
                                      &d3dpp, NULL, &g_pd3dDevice)))
    {
        return E_FAIL;
    }
```



<span data-ttu-id="9f709-254">**Para evitar, detectar y recuperarse de problemas**</span><span class="sxs-lookup"><span data-stu-id="9f709-254">**To avoid, detect and recover from glitches**</span></span>

1.  <span data-ttu-id="9f709-255">Llamadas de la cola presente: el número de búferes de reserva recomendado es de 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="9f709-255">Queue Present calls: recommended backbuffer count is from 2 to 4.</span></span>
2.  <span data-ttu-id="9f709-256">El ejemplo Direct3D 9Ex agrega un búfer de reserva implícito, la longitud actual de la cola actual es el número de búferes de reserva + 1.</span><span class="sxs-lookup"><span data-stu-id="9f709-256">Direct3D 9Ex sample adds an implicit backbuffer, actual Present queue length is backbuffer count + 1.</span></span>
3.  <span data-ttu-id="9f709-257">Crear la estructura de cola de la aplicación auxiliar para almacenar todos los IDENTIFICADOres actuales del presente (PresentCount) enviados correctamente y asociados, calculados o esperados, PresentRefreshCount.</span><span class="sxs-lookup"><span data-stu-id="9f709-257">Create helper Present queue structure to store all successfully submitted Present's Present ID (PresentCount) and associated, calculated/expected PresentRefreshCount.</span></span>
4.  <span data-ttu-id="9f709-258">Para detectar la ocurrencia del problema:</span><span class="sxs-lookup"><span data-stu-id="9f709-258">To detect glitch occurrence:</span></span>

    -   <span data-ttu-id="9f709-259">Llame a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9f709-259">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)).</span></span>
    -   <span data-ttu-id="9f709-260">Obtiene el identificador actual (PresentCount) y el recuento de VSYNC en el que se muestra el fotograma (PresentRefreshCount) del marco cuyas estadísticas presentes se obtienen.</span><span class="sxs-lookup"><span data-stu-id="9f709-260">Get the Present ID (PresentCount) and vsync count where the frame is shown (PresentRefreshCount) of the frame whose present statistics is obtained.</span></span>
    -   <span data-ttu-id="9f709-261">Recupere el PresentRefreshCount esperado (TargetRefresh en el código de ejemplo) asociado al identificador actual.</span><span class="sxs-lookup"><span data-stu-id="9f709-261">Retrieve the expected PresentRefreshCount (TargetRefresh in sample code) associated with the Present ID.</span></span>
    -   <span data-ttu-id="9f709-262">Si la PresentRefreshCount real es posterior a la esperada, se ha producido un problema.</span><span class="sxs-lookup"><span data-stu-id="9f709-262">If actual PresentRefreshCount is later than expected, a glitch has occurred.</span></span>

5.  <span data-ttu-id="9f709-263">Para recuperarse de un problema:</span><span class="sxs-lookup"><span data-stu-id="9f709-263">To recover from glitch:</span></span>

    -   <span data-ttu-id="9f709-264">Calcular el número de fotogramas que se van a omitir (g \_ iImmediates variable en el código de ejemplo).</span><span class="sxs-lookup"><span data-stu-id="9f709-264">Calculate how many frames to skip (g\_ iImmediates variable in sample code).</span></span>
    -   <span data-ttu-id="9f709-265">Presente los marcos omitidos con Interval D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="9f709-265">Present the skipped frames with interval D3DPRESENT\_FORCEIMMEDIATE.</span></span>

<span data-ttu-id="9f709-266">**Consideraciones sobre la detección y recuperación de problemas**</span><span class="sxs-lookup"><span data-stu-id="9f709-266">**Considerations for glitch detection and recovery**</span></span>

1.  <span data-ttu-id="9f709-267">La recuperación con problemas toma la variable N (g \_ iQueueDelay en el código de ejemplo) del número de llamadas presentes, donde N (g \_ iQueueDelay) es igual a g \_ iImmediates más la longitud de la cola actual, es decir:</span><span class="sxs-lookup"><span data-stu-id="9f709-267">Glitch recovery takes N (g\_iQueueDelay variable in sample code) number of Present calls where N (g\_iQueueDelay) equals g\_iImmediates plus length of the Present queue, that is:</span></span>

    -   <span data-ttu-id="9f709-268">Omitir fotogramas con el intervalo presente D3DPRESENT \_ FORCEIMMEDIATE, más</span><span class="sxs-lookup"><span data-stu-id="9f709-268">Skipping frames with Present interval D3DPRESENT\_FORCEIMMEDIATE, plus</span></span>
    -   <span data-ttu-id="9f709-269">Queued presenta que debe procesarse</span><span class="sxs-lookup"><span data-stu-id="9f709-269">Queued Presents that need to be processed</span></span>

2.  <span data-ttu-id="9f709-270">Establezca un límite en la longitud del problema ( \_ \_ límite de recuperación por problema en el ejemplo).</span><span class="sxs-lookup"><span data-stu-id="9f709-270">Set a limit to the glitch length (GLITCH\_RECOVERY\_LIMIT in sample).</span></span> <span data-ttu-id="9f709-271">Si la aplicación de ejemplo no puede recuperarse de un problema que es demasiado largo (por ejemplo, 1 segundo o 60 vsyncs en el monitor de 60 Hz), salte la animación intermitente y restablezca la cola del ayudante actual.</span><span class="sxs-lookup"><span data-stu-id="9f709-271">If the sample application cannot recover from a glitch that is too long (that is say, 1 second, or 60 vsyncs on 60Hz monitor), jump over the intermittent animation and reset the Present helper queue.</span></span>


```C++
VOID Render()
{
    g_pd3dDevice->Clear(0, NULL, D3DCLEAR_TARGET, D3DCOLOR_XRGB(0, 0, 0), 1.0f, 0);

    g_pd3dDevice->BeginScene();

    // Compute new animation parameters for time and frame based animations

    // Time-based is a difference between base and current SyncRefreshCount
    g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
    // Frame-based is incrementing frame value
    g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;

    RenderBlurredMesh(TRUE);    // Time-based
    RenderBlurredMesh(FALSE);   // Frame-based

    g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;

    DrawText();

    g_pd3dDevice->EndScene();

    // Performs glitch recovery if glitch was detected
    if (g_bGlitchRecovery && (g_iImmediates > 0))
    {
        // If we have present immediates queued as a result of glitch detected, issue forceimmediate Presents for glitch recovery 
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE);
        g_iImmediates--;
        g_iShowingGlitchRecovery = MESSAGE_SHOW;
    }
    // Otherwise, Present normally
    else
    {
        g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, 0);
    }

    // Add to helper Present queue: PresentID + expected present refresh count of last submitted Present
    UINT PresentCount;
    g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
    g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);
    
    // QueueDelay specifies # Present calls to be processed before another glitch recovery attempt
    if (g_iQueueDelay > 0)
    {
        g_iQueueDelay--;
    }

    if (g_bGlitchRecovery)
    {
        // Additional DONOTFLIP presents for frame conversions, which basically follows the same logic, but without rendering
        for (DWORD i = 0; i < g_iDoNotFlipNum; i++)
        {
            if (g_TargetRefreshCount != -1)
            {
                g_TargetRefreshCount++;
                g_iFrameNumber++;
                g_aTimeBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_LastSyncRefreshCount - g_SyncRefreshCount;
                g_aFrameBasedHistory[g_iBlurHistoryCounter] = g_iStartFrame + g_iFrameNumber;
                g_iBlurHistoryCounter = (g_iBlurHistoryCounter + 1) % BLUR_FRAMES;
            }
            
            if (g_iImmediates > 0)
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_FORCEIMMEDIATE | D3DPRESENT_DONOTFLIP);
                g_iImmediates--;
            }
            else
            {
                g_pd3dDevice->PresentEx(NULL, NULL, NULL, NULL, D3DPRESENT_DONOTFLIP);
            }
            UINT PresentCount;
            g_pd3dSwapChain->GetLastPresentCount(&PresentCount);
            g_Queue.QueueFrame(PresentCount, g_TargetRefreshCount);

            if (g_iQueueDelay > 0)
            {
                g_iQueueDelay--;
            }
        }
    }

    // Check Present Stats info for glitch detection 
    D3DPRESENTSTATS PresentStats;

    // Obtain present statistics information for successfully displayed presents
    HRESULT hr = g_pd3dSwapChain->GetPresentStats(&PresentStats);

    if (SUCCEEDED(hr))
    {
        // Time-based update
        g_LastSyncRefreshCount = PresentStats.SyncRefreshCount;
        if ((g_SyncRefreshCount == -1) && (PresentStats.PresentCount != 0))
        {
            // First time SyncRefreshCount is reported, use it as base
            g_SyncRefreshCount = PresentStats.SyncRefreshCount;
        }

        // Fetch frame from the queue...
        UINT TargetRefresh = g_Queue.DequeueFrame(PresentStats.PresentCount);

        // If PresentStats returned a really old frame that we no longer have in the queue, just don't do any glitch detection
        if (TargetRefresh == FRAME_NOT_FOUND)
            return;

        if (g_TargetRefreshCount == -1)
        {
            // This is first time issued frame is confirmed by present stats, so fill target refresh count for all frames in the queue
            g_TargetRefreshCount = g_Queue.FillRefreshCounts(PresentStats.PresentCount, g_SyncRefreshCount);
        } 
        else
        {
            g_TargetRefreshCount++;
            g_iFrameNumber++;

            // To determine whether we're glitching, see if our estimated refresh count is confirmed
            // if the frame is displayed later than the expected vsync count
            if (TargetRefresh < PresentStats.PresentRefreshCount)
            {
                // then, glitch is detected!

                // If glitch is too big, don't bother recovering from it, just jump animation
                if ((PresentStats.PresentRefreshCount - TargetRefresh) > GLITCH_RECOVERY_LIMIT)
                {
                    g_iStartFrame += PresentStats.SyncRefreshCount - g_SyncRefreshCount;
                    ResetAnimation();
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;    
                } 
                // Otherwise, compute number of immediate presents to recover from it -- if we?re not still trying to recover from another glitch
                else if (g_iQueueDelay == 0)
                {
                      // skip frames to catch up to expected refresh count
                    g_iImmediates = PresentStats.PresentRefreshCount - TargetRefresh;
                    // QueueDelay specifies # Present calls before another glitch recovery 
                    g_iQueueDelay = g_iImmediates + QUEUE_SIZE;
                    if (g_bGlitchRecovery)
                        g_iGlitchesInaRow++;
                }
            }
            else
            {
                // No glitch, reset glitch count
                g_iGlitchesInaRow = 0;
            }
        }
    }
    else if (hr == D3DERR_PRESENT_STATISTICS_DISJOINT)
    {
        // D3DERR_PRESENT_STATISTICS_DISJOINT means measurements should be started from the scratch (could be caused by mode change or DWM on/off transition)
        ResetAnimation();
    }

    // If we got too many glitches in a row, reduce framerate conversion factor (that is, render less frames)
    if (g_iGlitchesInaRow == FRAMECONVERSION_GLITCH_LIMIT)
    {
        if (g_iDoNotFlipNum < FRAMECONVERSION_LIMIT)
        {
            g_iDoNotFlipNum++;
        }
        g_iGlitchesInaRow = 0;
        g_iShowingDoNotFlipBump = MESSAGE_SHOW;
    }
}
```



<span data-ttu-id="9f709-272">**Escenario de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="9f709-272">**Sample scenario**</span></span>

-   <span data-ttu-id="9f709-273">En la ilustración siguiente se muestra una aplicación con el recuento de búferes de reserva de 4.</span><span class="sxs-lookup"><span data-stu-id="9f709-273">The following illustration shows an application with backbuffer count of 4.</span></span> <span data-ttu-id="9f709-274">Por lo tanto, la longitud actual de la cola es 5.</span><span class="sxs-lookup"><span data-stu-id="9f709-274">The actual Present queue length is therefore 5.</span></span>

    ![Ilustración de un applicas representado frames y present Queue](images/sample-scenario.png)

    <span data-ttu-id="9f709-276">El marco a está destinada a pasar a la pantalla en el recuento de intervalos de sincronización de 1, pero se detectó que se mostró en el recuento de intervalos de sincronización de 4.</span><span class="sxs-lookup"><span data-stu-id="9f709-276">Frame A is targeted to go on screen on sync interval count of 1 but was detected that it was shown on sync interval count of 4.</span></span> <span data-ttu-id="9f709-277">Por lo tanto, se ha producido un problema.</span><span class="sxs-lookup"><span data-stu-id="9f709-277">Therefore a glitch has occurred.</span></span> <span data-ttu-id="9f709-278">Los 3 fotogramas siguientes se presentan con el intervalo de D3DPRESENT \_ \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="9f709-278">Subsequent 3 frames are presented with D3DPRESENT\_INTERVAL\_FORCEIMMEDIATE.</span></span> <span data-ttu-id="9f709-279">El problema debe llevar un total de 8 llamadas presentes antes de que se recuperen: el siguiente fotograma se mostrará según el número de intervalos de sincronización de destino.</span><span class="sxs-lookup"><span data-stu-id="9f709-279">The glitch should take a total of 8 Present calls before it is recovered - the next frame will be shown as per its targeted sync interval count.</span></span>

### <a name="summary-of-programming-recommendations-for-frame-synchronization"></a><span data-ttu-id="9f709-280">Resumen de las recomendaciones de programación para la sincronización de fotogramas</span><span class="sxs-lookup"><span data-stu-id="9f709-280">Summary of Programming Recommendations for Frame Synchronization</span></span>

-   <span data-ttu-id="9f709-281">Cree una lista de copia de seguridad de todos los identificadores de LastPresentCount (obtenidos a través de [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) y el PresentRefreshCount Estimado asociado de todas las presentaciones enviadas.</span><span class="sxs-lookup"><span data-stu-id="9f709-281">Create a backup list of all the LastPresentCount IDs (obtained via [**GetLastPresentCount**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dswapchain9ex-getlastpresentcount)) and associated estimated PresentRefreshCount of all the Presents submitted.</span></span>
    > [!Note]  
    > <span data-ttu-id="9f709-282">Cuando la aplicación llama a [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) con D3DPRESENT \_ DONOTFLIP, la llamada [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) se realiza correctamente, pero no devuelve una estructura [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) actualizada cuando la aplicación está en modo de ventana.</span><span class="sxs-lookup"><span data-stu-id="9f709-282">When the application calls [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) with D3DPRESENT\_DONOTFLIP, the [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) call succeeds but does not return an updated [**D3DPRESENTSTATS**](/windows/desktop/direct3d9/d3dpresentstats) structure when the application is in windowed mode.</span></span>

     

-   <span data-ttu-id="9f709-283">Llame a [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) para obtener el PresentRefreshCount real asociado a cada identificador presente de los fotogramas mostrados, para asegurarse de que la aplicación controla las devoluciones de errores de la llamada.</span><span class="sxs-lookup"><span data-stu-id="9f709-283">Call [**GetPresentStatistics**](/previous-versions/windows/desktop/legacy/bb205901(v=vs.85)) to obtain the actual PresentRefreshCount associated with each Present ID of frames shown, to make sure that the application handles failure returns from the call.</span></span>
-   <span data-ttu-id="9f709-284">Si PresentRefreshCount real es posterior a la estimación de PresentRefreshCount, se detecta un problema.</span><span class="sxs-lookup"><span data-stu-id="9f709-284">If actual PresentRefreshCount is later than estimated PresentRefreshCount, a glitch is detected.</span></span> <span data-ttu-id="9f709-285">Compensar enviando fotogramas atrasados con D3DPRESENT \_ FORCEIMMEDIATE.</span><span class="sxs-lookup"><span data-stu-id="9f709-285">Compensate by submitting lagging frames' Present with D3DPRESENT\_FORCEIMMEDIATE.</span></span>
-   <span data-ttu-id="9f709-286">Cuando un fotograma se presenta en la cola actual, todos los fotogramas en cola subsiguientes se presentarán en tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="9f709-286">When one frame is presented late in the Present queue, all subsequent queued frames will be presented late.</span></span> <span data-ttu-id="9f709-287">D3DPRESENT \_ FORCEIMMEDIATE corregirá solo el siguiente fotograma que se presentará después de todos los marcos en cola.</span><span class="sxs-lookup"><span data-stu-id="9f709-287">D3DPRESENT\_FORCEIMMEDIATE will correct only the next frame to be presented after all the queued frames.</span></span> <span data-ttu-id="9f709-288">Por lo tanto, la cola actual o el número de búferes de reserva no deben ser demasiado largos, por lo que hay menos problemas de fotogramas con los que ponerse al día.</span><span class="sxs-lookup"><span data-stu-id="9f709-288">Therefore, the Present queue or backbuffer count should not be too long -- so there are less frame glitches to catch up with.</span></span> <span data-ttu-id="9f709-289">El número de búferes de reserva óptimo es de 2 a 4.</span><span class="sxs-lookup"><span data-stu-id="9f709-289">The optimal backbuffer count is 2 to 4.</span></span>
-   <span data-ttu-id="9f709-290">Si el PresentRefreshCount Estimado es posterior al PresentRefreshCount real, es posible que se haya producido una limitación de DWM.</span><span class="sxs-lookup"><span data-stu-id="9f709-290">If estimated PresentRefreshCount is later than the actual PresentRefreshCount, DWM throttling might have occurred.</span></span> <span data-ttu-id="9f709-291">Las siguientes soluciones son posibles:</span><span class="sxs-lookup"><span data-stu-id="9f709-291">The following solutions are possible:</span></span>

    -   <span data-ttu-id="9f709-292">reducción de la longitud de la cola actual</span><span class="sxs-lookup"><span data-stu-id="9f709-292">reducing Present queue length</span></span>
    -   <span data-ttu-id="9f709-293">reducir los requisitos de memoria de GPU con cualquier otro medio además de reducir la longitud de la cola actual (es decir, reducir la calidad, quitar efectos, etc.)</span><span class="sxs-lookup"><span data-stu-id="9f709-293">reducing GPU memory requirements with any other means besides reducing Present Queue length (that is, decreasing quality, removing effects, and so on)</span></span>
    -   <span data-ttu-id="9f709-294">especificar [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) para evitar la limitación DWM en general</span><span class="sxs-lookup"><span data-stu-id="9f709-294">specifying [**DwmEnableMMCSS**](/windows/desktop/api/dwmapi/nf-dwmapi-dwmenablemmcss) to prevent DWM throttling in general</span></span>

-   <span data-ttu-id="9f709-295">Compruebe la funcionalidad de presentación de la aplicación y el rendimiento de las estadísticas de fotogramas en los escenarios siguientes:</span><span class="sxs-lookup"><span data-stu-id="9f709-295">Verify application display functionality and frame statistics performance in the following scenarios:</span></span>

    -   <span data-ttu-id="9f709-296">con DWM activado y desactivado</span><span class="sxs-lookup"><span data-stu-id="9f709-296">with DWM on and off</span></span>
    -   <span data-ttu-id="9f709-297">modos exclusivo y en ventana de pantalla completa</span><span class="sxs-lookup"><span data-stu-id="9f709-297">fullscreen exclusive and windowed modes</span></span>
    -   <span data-ttu-id="9f709-298">hardware de funcionalidad inferior</span><span class="sxs-lookup"><span data-stu-id="9f709-298">lower capability hardware</span></span>

-   <span data-ttu-id="9f709-299">Cuando las aplicaciones no pueden recuperarse de un gran número de fotogramas con problemas con D3DPRESENT \_ FORCEIMMEDIATE presentes, pueden realizar las siguientes operaciones:</span><span class="sxs-lookup"><span data-stu-id="9f709-299">When applications cannot recover from large numbers of glitched frames with D3DPRESENT\_FORCEIMMEDIATE Present, they can potentially perform the following operations:</span></span>

    -   <span data-ttu-id="9f709-300">reduzca el uso de la CPU y la GPU mediante la representación de menos carga de trabajo.</span><span class="sxs-lookup"><span data-stu-id="9f709-300">reduce CPU and GPU usage by rendering with less workload.</span></span>
    -   <span data-ttu-id="9f709-301">en el caso de la descodificación de vídeo, descodifique más rápido reduciendo la calidad y, por lo tanto, el uso de la CPU y la GPU.</span><span class="sxs-lookup"><span data-stu-id="9f709-301">in the case of video decode, decode faster by reducing quality and, therefore, CPU and GPU usage.</span></span>

## <a name="conclusion-about-direct3d-9ex-improvements"></a><span data-ttu-id="9f709-302">Conclusión sobre las mejoras de Direct3D 9Ex</span><span class="sxs-lookup"><span data-stu-id="9f709-302">Conclusion about Direct3D 9Ex Improvements</span></span>

<span data-ttu-id="9f709-303">En Windows 7, las aplicaciones que muestran la velocidad de fotogramas de vídeo o medidor durante la presentación pueden optar por voltear el modelo.</span><span class="sxs-lookup"><span data-stu-id="9f709-303">On Windows 7, applications that display video or gauge frame rate during presentation can opt into Flip Model.</span></span> <span data-ttu-id="9f709-304">Las mejoras presentes en las estadísticas asociadas a Flip Model Direct3D 9Ex pueden beneficiar a las aplicaciones que sincronizan la presentación por velocidad de fotogramas, con comentarios en tiempo real para la detección y recuperación de problemas.</span><span class="sxs-lookup"><span data-stu-id="9f709-304">The present statistics improvements that are associated with Flip Model Direct3D 9Ex can benefit applications that synchronize presentation per frame rate, with real time feedback for glitch detection and recovery.</span></span> <span data-ttu-id="9f709-305">Los desarrolladores que adopten el modelo Flip 9Ex de Direct3D deben tener en cuenta un HWND independiente del contenido GDI y la sincronización de la velocidad de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="9f709-305">Developers that adopt the Direct3D 9Ex Flip Model should take targeting a separate HWND from GDI content and frame rate synchronization into account.</span></span> <span data-ttu-id="9f709-306">Consulte los detalles de este tema y la documentación de MSDN.</span><span class="sxs-lookup"><span data-stu-id="9f709-306">Refer to details in this topic, and MSDN documentation.</span></span> <span data-ttu-id="9f709-307">Para obtener documentación adicional, consulte el [Centro para desarrolladores de DirectX en MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="9f709-307">For additional documentation, see [DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10)).</span></span>

## <a name="call-to-action"></a><span data-ttu-id="9f709-308">Pasar a la acción</span><span class="sxs-lookup"><span data-stu-id="9f709-308">Call to Action</span></span>

<span data-ttu-id="9f709-309">Le recomendamos que use Direct3D 9Ex Flip Model y sus estadísticas presentes en Windows 7 cuando cree aplicaciones que intenten sincronizar la velocidad de fotogramas de presentación o recuperarse de los problemas de visualización.</span><span class="sxs-lookup"><span data-stu-id="9f709-309">We encourage you to use Direct3D 9Ex Flip Model and its present statistics on Windows 7 when you create applications that attempt to synchronize presentation frame rate or recover from display glitches.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9f709-310">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9f709-310">Related topics</span></span>

<span data-ttu-id="9f709-311">[Centro para desarrolladores de DirectX en MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="9f709-311">[DirectX Developer Center on MSDN](/previous-versions/windows/apps/hh452744(v=win.10))</span></span>
</dt> </dl>