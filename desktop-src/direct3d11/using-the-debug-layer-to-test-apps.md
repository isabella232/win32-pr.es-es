---
title: Usar la capa de depuración para depurar aplicaciones
description: Aquí hablaremos sobre cómo habilitar la capa de depuración y algunos de los problemas que puede evitar mediante el uso de la capa de depuración.
ms.assetid: 3C2B0A12-FB57-4400-BE39-05ED23F552C7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aaa3f4748da6893470e3bb6631c4228ec1ae3d48
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773711"
---
# <a name="using-the-debug-layer-to-debug-apps"></a><span data-ttu-id="7aaa4-103">Usar la capa de depuración para depurar aplicaciones</span><span class="sxs-lookup"><span data-stu-id="7aaa4-103">Using the debug layer to debug apps</span></span>

<span data-ttu-id="7aaa4-104">Se recomienda usar la capa de [depuración](overviews-direct3d-11-devices-layers.md) para depurar las aplicaciones con el fin de asegurarse de que están limpias de errores y advertencias.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-104">We recommend that you use the [debug layer](overviews-direct3d-11-devices-layers.md) to debug your apps to ensure that they are clean of errors and warnings.</span></span> <span data-ttu-id="7aaa4-105">La capa de depuración le ayuda a escribir código de Direct3D.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-105">The debug layer helps you write Direct3D code.</span></span> <span data-ttu-id="7aaa4-106">Además, la productividad puede aumentar al usar la capa de depuración, ya que puede ver inmediatamente las causas de los errores de representación ocultos o incluso las pantallas negras en su origen.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-106">In addition, your productivity can increase when you use the debug layer because you can immediately see the causes of obscure rendering errors or even black screens at their source.</span></span> <span data-ttu-id="7aaa4-107">El nivel de depuración proporciona advertencias para muchos problemas.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-107">The debug layer provides warnings for many issues.</span></span> <span data-ttu-id="7aaa4-108">Por ejemplo, la capa de depuración proporciona advertencias para estos problemas:</span><span class="sxs-lookup"><span data-stu-id="7aaa4-108">For example, the debug layer provides warnings for these issues:</span></span>

-   <span data-ttu-id="7aaa4-109">Olvidó establecer una textura pero leerla en el sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="7aaa4-109">Forgot to set a texture but read from it in your pixel shader</span></span>
-   <span data-ttu-id="7aaa4-110">Profundidad de salida, pero no tiene ningún límite de estado de estarcido de profundidad</span><span class="sxs-lookup"><span data-stu-id="7aaa4-110">Output depth but have no depth-stencil state bound</span></span>
-   <span data-ttu-id="7aaa4-111">Error de creación de textura con INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="7aaa4-111">Texture creation failed with INVALIDARG</span></span>

<span data-ttu-id="7aaa4-112">Aquí hablaremos sobre cómo habilitar la [capa de depuración](overviews-direct3d-11-devices-layers.md) y algunos de los problemas que puede evitar mediante el uso de la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-112">Here we talk about how to enable the [debug layer](overviews-direct3d-11-devices-layers.md) and some of the issues that you can prevent by using the debug layer.</span></span>

-   [<span data-ttu-id="7aaa4-113">Habilitar la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="7aaa4-113">Enabling the debug layer</span></span>](#enabling-the-debug-layer)
-   [<span data-ttu-id="7aaa4-114">Evitar errores en la aplicación con la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="7aaa4-114">Preventing errors in your app with the debug layer</span></span>](#preventing-errors-in-your-app-with-the-debug-layer)
    -   [<span data-ttu-id="7aaa4-115">No pasar punteros NULL a la asignación</span><span class="sxs-lookup"><span data-stu-id="7aaa4-115">Don't pass NULL pointers to Map</span></span>](#dont-pass-null-pointers-to-map)
    -   [<span data-ttu-id="7aaa4-116">Cuadro de código fuente de límites dentro de los recursos de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="7aaa4-116">Confine source box within source and destination resources</span></span>](#confine-source-box-within-source-and-destination-resources)
    -   [<span data-ttu-id="7aaa4-117">No quite DiscardResource ni DiscardView</span><span class="sxs-lookup"><span data-stu-id="7aaa4-117">Don't drop DiscardResource or DiscardView</span></span>](#dont-drop-discardresource-or-discardview)
-   [<span data-ttu-id="7aaa4-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7aaa4-118">Related topics</span></span>](#related-topics)

## <a name="enabling-the-debug-layer"></a><span data-ttu-id="7aaa4-119">Habilitar la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="7aaa4-119">Enabling the debug layer</span></span>

<span data-ttu-id="7aaa4-120">Para habilitar la [capa de depuración](overviews-direct3d-11-devices-layers.md), especifique la marca de [**\_ \_ \_ depuración crear dispositivo de D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) en el parámetro *Flags* al llamar a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear el dispositivo de representación.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-120">To enable the [debug layer](overviews-direct3d-11-devices-layers.md), specify the [**D3D11\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag) flag in the *Flags* parameter when you call the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function to create the rendering device.</span></span> <span data-ttu-id="7aaa4-121">Este código de ejemplo muestra cómo habilitar la capa de depuración cuando el proyecto de Microsoft Visual Studio está en una compilación de depuración:</span><span class="sxs-lookup"><span data-stu-id="7aaa4-121">This example code shows how to enable the debug layer when your Microsoft Visual Studio project is in a debug build:</span></span>


```C++
        UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
#if defined(_DEBUG)
        // If the project is in a debug build, enable the debug layer.
        creationFlags |= D3D11_CREATE_DEVICE_DEBUG;
#endif
        // Define the ordering of feature levels that Direct3D attempts to create.
        D3D_FEATURE_LEVEL featureLevels[] =
        {
            D3D_FEATURE_LEVEL_11_1,
            D3D_FEATURE_LEVEL_11_0,
            D3D_FEATURE_LEVEL_10_1,
            D3D_FEATURE_LEVEL_10_0,
            D3D_FEATURE_LEVEL_9_3,
            D3D_FEATURE_LEVEL_9_1
        };

        ComPtr<ID3D11Device> d3dDevice;
        ComPtr<ID3D11DeviceContext> d3dDeviceContext;
        DX::ThrowIfFailed(
            D3D11CreateDevice(
                nullptr,                    // specify nullptr to use the default adapter
                D3D_DRIVER_TYPE_HARDWARE,
                nullptr,                    // specify nullptr because D3D_DRIVER_TYPE_HARDWARE 
                                            // indicates that this function uses hardware
                creationFlags,              // optionally set debug and Direct2D compatibility flags
                featureLevels,
                ARRAYSIZE(featureLevels),
                D3D11_SDK_VERSION,          // always set this to D3D11_SDK_VERSION
                &d3dDevice,
                nullptr,
                &d3dDeviceContext
                )
            );
```



## <a name="preventing-errors-in-your-app-with-the-debug-layer"></a><span data-ttu-id="7aaa4-122">Evitar errores en la aplicación con la capa de depuración</span><span class="sxs-lookup"><span data-stu-id="7aaa4-122">Preventing errors in your app with the debug layer</span></span>

<span data-ttu-id="7aaa4-123">Si se emplea el uso incorrecto de la API de Direct3D 11 o se pasan parámetros incorrectos, la salida de depuración de la [capa de depuración](overviews-direct3d-11-devices-layers.md) notifica un error o una advertencia.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-123">If you misuse the Direct3D 11 API or pass bad parameters, the debug output of the [debug layer](overviews-direct3d-11-devices-layers.md) reports an error or a warning.</span></span> <span data-ttu-id="7aaa4-124">Después, puede corregir el error.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-124">You can then correct your mistake.</span></span> <span data-ttu-id="7aaa4-125">A continuación, veremos algunos problemas de codificación que pueden provocar un comportamiento indefinido o incluso que el sistema operativo se bloquee.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-125">Next, we look at some coding issues that can cause undefined behavior or even the operating system to crash.</span></span> <span data-ttu-id="7aaa4-126">Puede detectar y evitar estos problemas mediante el uso de la capa de depuración.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-126">You can catch and prevent these issues by using the debug layer.</span></span>

### <a name="dont-pass-null-pointers-to-map"></a><span data-ttu-id="7aaa4-127">No pasar punteros NULL a la asignación</span><span class="sxs-lookup"><span data-stu-id="7aaa4-127">Don't pass NULL pointers to Map</span></span>

<span data-ttu-id="7aaa4-128">Si pasa **null** al parámetro *PreSource* o *pMappedResource* del método [**ID3D11DeviceContext:: Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) , el comportamiento de la **asignación** es indefinido.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-128">If you pass **NULL** to the *pResource* or *pMappedResource* parameter of the [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map) method, the behavior of **Map** is undefined.</span></span> <span data-ttu-id="7aaa4-129">Si creó un dispositivo que solo admite la [capa básica](overviews-direct3d-11-devices-layers.md), los parámetros no válidos para **asignar** pueden bloquear el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-129">If you created a device that just supports the [core layer](overviews-direct3d-11-devices-layers.md), invalid parameters to **Map** can crash the operating system.</span></span> <span data-ttu-id="7aaa4-130">Si creó un dispositivo que admite la [capa de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notificará un error en esta llamada de **asignación** no válida.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-130">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **Map** call.</span></span>

### <a name="confine-source-box-within-source-and-destination-resources"></a><span data-ttu-id="7aaa4-131">Cuadro de código fuente de límites dentro de los recursos de origen y de destino</span><span class="sxs-lookup"><span data-stu-id="7aaa4-131">Confine source box within source and destination resources</span></span>

<span data-ttu-id="7aaa4-132">En una llamada al método [**ID3D11DeviceContext:: CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) , el cuadro de código fuente debe estar dentro del recurso de origen.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-132">In a call to the [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) method, the source box must be within the source resource.</span></span> <span data-ttu-id="7aaa4-133">Los desplazamientos de destino, (x, y y z) permiten que el cuadro de origen se desplace cuando se escribe en el recurso de destino, pero las dimensiones del cuadro de código fuente y los desplazamientos deben estar dentro del tamaño del recurso.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-133">The destination offsets, (x, y, and z) allow the source box to be offset when writing into the destination resource, but the dimensions of the source box and the offsets must be within the size of the resource.</span></span> <span data-ttu-id="7aaa4-134">Si intenta copiar fuera del recurso de destino o especifica un cuadro de código fuente mayor que el recurso de origen, el comportamiento de **CopySubresourceRegion** es indefinido.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-134">If you try to copy outside the destination resource or specify a source box that is larger than the source resource, the behavior of **CopySubresourceRegion** is undefined.</span></span> <span data-ttu-id="7aaa4-135">Si creó un dispositivo que admite la [capa de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notificará un error en esta llamada **CopySubresourceRegion** no válida.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-135">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error on this invalid **CopySubresourceRegion** call.</span></span> <span data-ttu-id="7aaa4-136">Los parámetros no válidos para **CopySubresourceRegion** causan un comportamiento indefinido y pueden dar lugar a una representación, un recorte, una copia incorrectas o incluso la eliminación del dispositivo de representación.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-136">Invalid parameters to **CopySubresourceRegion** cause undefined behavior and might result in incorrect rendering, clipping, no copy, or even the removal of the rendering device.</span></span>

### <a name="dont-drop-discardresource-or-discardview"></a><span data-ttu-id="7aaa4-137">No quite DiscardResource ni DiscardView</span><span class="sxs-lookup"><span data-stu-id="7aaa4-137">Don't drop DiscardResource or DiscardView</span></span>

<span data-ttu-id="7aaa4-138">El Runtime quita una llamada a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) o [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) a menos que cree correctamente el recurso.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-138">The runtime drops a call to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) or [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) unless you correctly create the resource.</span></span>

<span data-ttu-id="7aaa4-139">El recurso que se pasa a [**ID3D11DeviceContext1::D iscardresource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) se debe haber creado con [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). de lo contrario, el tiempo de ejecución quita la llamada a **DiscardResource**.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-139">The resource that you pass to [**ID3D11DeviceContext1::DiscardResource**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardresource) must have been created by using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardResource**.</span></span>

<span data-ttu-id="7aaa4-140">El recurso subyacente a la vista que se pasa a [**ID3D11DeviceContext1::D iscardview**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) se debe haber creado con [**D3D11 \_ Usage \_ default**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) o [**D3D11 \_ Usage \_ Dynamic**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage). de lo contrario, el tiempo de ejecución quita la llamada a **DiscardView**.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-140">The resource that underlies the view that you pass to [**ID3D11DeviceContext1::DiscardView**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-discardview) must have been created using [**D3D11\_USAGE\_DEFAULT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage) or [**D3D11\_USAGE\_DYNAMIC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_usage), otherwise the runtime drops the call to **DiscardView**.</span></span>

<span data-ttu-id="7aaa4-141">Si creó un dispositivo que admite la [capa de depuración](overviews-direct3d-11-devices-layers.md), la salida de depuración notifica un error relacionado con la llamada quitada.</span><span class="sxs-lookup"><span data-stu-id="7aaa4-141">If you created a device that supports the [debug layer](overviews-direct3d-11-devices-layers.md), the debug output reports an error regarding the dropped call.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7aaa4-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7aaa4-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7aaa4-143">Capas de software</span><span class="sxs-lookup"><span data-stu-id="7aaa4-143">Software Layers</span></span>](overviews-direct3d-11-devices-layers.md)
</dt> </dl>

 

 




