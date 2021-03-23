---
title: D2D con D3D11on12
description: En el ejemplo D3D1211on12 se muestra cómo representar el contenido de D2D sobre el contenido de D3D12 compartiendo recursos entre un dispositivo basado en 11 y un dispositivo basado en 12.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d18399b85499787f74dab725d562b6a299878b35
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104549195"
---
# <a name="d2d-using-d3d11on12"></a><span data-ttu-id="baec2-103">D2D con D3D11on12</span><span class="sxs-lookup"><span data-stu-id="baec2-103">D2D using D3D11on12</span></span>

<span data-ttu-id="baec2-104">En el ejemplo **D3D1211on12** se muestra cómo representar el contenido de D2D sobre el contenido de D3D12 compartiendo recursos entre un dispositivo basado en 11 y un dispositivo basado en 12.</span><span class="sxs-lookup"><span data-stu-id="baec2-104">The **D3D1211on12** sample demonstrates how to render D2D content over D3D12 content by sharing resources between an 11 based device and a 12 based device.</span></span>

-   [<span data-ttu-id="baec2-105">Creación de un ID3D11On12Device</span><span class="sxs-lookup"><span data-stu-id="baec2-105">Create an ID3D11On12Device</span></span>](#create-an-id3d11on12device)
-   [<span data-ttu-id="baec2-106">Creación de un generador de D2D</span><span class="sxs-lookup"><span data-stu-id="baec2-106">Create a D2D factory</span></span>](#create-a-d2d-factory)
-   [<span data-ttu-id="baec2-107">Crear un destino de representación para D2D</span><span class="sxs-lookup"><span data-stu-id="baec2-107">Create a render target for D2D</span></span>](#create-a-render-target-for-d2d)
-   [<span data-ttu-id="baec2-108">Crear objetos de texto D2D básicos</span><span class="sxs-lookup"><span data-stu-id="baec2-108">Create basic D2D text objects</span></span>](#create-basic-d2d-text-objects)
-   [<span data-ttu-id="baec2-109">Actualizar el bucle de representación principal</span><span class="sxs-lookup"><span data-stu-id="baec2-109">Updating the main render loop</span></span>](#updating-the-main-render-loop)
-   [<span data-ttu-id="baec2-110">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="baec2-110">Run the sample</span></span>](#run-the-sample)
-   [<span data-ttu-id="baec2-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="baec2-111">Related topics</span></span>](#related-topics)

## <a name="create-an-id3d11on12device"></a><span data-ttu-id="baec2-112">Creación de un ID3D11On12Device</span><span class="sxs-lookup"><span data-stu-id="baec2-112">Create an ID3D11On12Device</span></span>

<span data-ttu-id="baec2-113">El primer paso es crear un [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) una vez creado el [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) , lo que implica la creación de un [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) que se ajusta alrededor de la **ID3D12Device** a través de la API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice).</span><span class="sxs-lookup"><span data-stu-id="baec2-113">The first step is to create an [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) after the [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) has been created, which involves creating an [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) that is wrapped around the **ID3D12Device** via the API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice).</span></span> <span data-ttu-id="baec2-114">Esta API también toma, entre otros parámetros, un [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) para que el dispositivo 11On12 pueda enviar sus comandos.</span><span class="sxs-lookup"><span data-stu-id="baec2-114">This API also takes in, among other parameters, an [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) so that the 11On12 device can submit its commands.</span></span> <span data-ttu-id="baec2-115">Una vez creado el **ID3D11Device** , puede consultar la interfaz de **ID3D11On12Device** desde él.</span><span class="sxs-lookup"><span data-stu-id="baec2-115">After the **ID3D11Device** is created, you can query the **ID3D11On12Device** interface from it.</span></span> <span data-ttu-id="baec2-116">Este es el objeto de dispositivo primario que se usará para configurar D2D.</span><span class="sxs-lookup"><span data-stu-id="baec2-116">This is the primary device object that will be used to set up D2D.</span></span>

<span data-ttu-id="baec2-117">En el método **LoadPipeline** , configure los dispositivos.</span><span class="sxs-lookup"><span data-stu-id="baec2-117">In the **LoadPipeline** method, setup the devices.</span></span>

``` syntax
 // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));
```



| <span data-ttu-id="baec2-118">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="baec2-118">Call flow</span></span>                                              | <span data-ttu-id="baec2-119">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baec2-119">Parameters</span></span> |
|--------------------------------------------------------|------------|
| [<span data-ttu-id="baec2-120">**ID3D11Device**</span><span class="sxs-lookup"><span data-stu-id="baec2-120">**ID3D11Device**</span></span>](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [<span data-ttu-id="baec2-121">**D3D11On12CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="baec2-121">**D3D11On12CreateDevice**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a><span data-ttu-id="baec2-122">Creación de un generador de D2D</span><span class="sxs-lookup"><span data-stu-id="baec2-122">Create a D2D factory</span></span>

<span data-ttu-id="baec2-123">Ahora que tenemos un dispositivo 11On12, lo usamos para crear un dispositivo y un generador de D2D de la misma forma que lo haría normalmente con D3D11.</span><span class="sxs-lookup"><span data-stu-id="baec2-123">Now that we have an 11On12 device, we use it to create a D2D factory and device just as it would normally be done with D3D11.</span></span>

<span data-ttu-id="baec2-124">Agregue al método **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="baec2-124">Add to the **LoadAssets** method.</span></span>

``` syntax
 // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &d2dFactoryOptions, &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &m_dWriteFactory));
    }
```



| <span data-ttu-id="baec2-125">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="baec2-125">Call flow</span></span>                                                                        | <span data-ttu-id="baec2-126">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baec2-126">Parameters</span></span>                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="baec2-127">**\_Opciones de \_ contexto de dispositivo de D2D1 \_**</span><span class="sxs-lookup"><span data-stu-id="baec2-127">**D2D1\_DEVICE\_CONTEXT\_OPTIONS**</span></span>](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [<span data-ttu-id="baec2-128">**D2D1CreateFactory**</span><span class="sxs-lookup"><span data-stu-id="baec2-128">**D2D1CreateFactory**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [<span data-ttu-id="baec2-129">**\_Tipo de fábrica D2D1 \_**</span><span class="sxs-lookup"><span data-stu-id="baec2-129">**D2D1\_FACTORY\_TYPE**</span></span>](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [<span data-ttu-id="baec2-130">**IDXGIDevice**</span><span class="sxs-lookup"><span data-stu-id="baec2-130">**IDXGIDevice**</span></span>](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [<span data-ttu-id="baec2-131">**ID2D1Factory3::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="baec2-131">**ID2D1Factory3::CreateDevice**</span></span>](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [<span data-ttu-id="baec2-132">**ID2D1Device::CreateDeviceContext**</span><span class="sxs-lookup"><span data-stu-id="baec2-132">**ID2D1Device::CreateDeviceContext**</span></span>](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [<span data-ttu-id="baec2-133">**DWriteCreateFactory**</span><span class="sxs-lookup"><span data-stu-id="baec2-133">**DWriteCreateFactory**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [<span data-ttu-id="baec2-134">**\_tipo de fábrica DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="baec2-134">**DWRITE\_FACTORY\_TYPE**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a><span data-ttu-id="baec2-135">Crear un destino de representación para D2D</span><span class="sxs-lookup"><span data-stu-id="baec2-135">Create a render target for D2D</span></span>

<span data-ttu-id="baec2-136">D3D12 es el propietario de la cadena de intercambio, por lo que si queremos representarla en el búfer de reserva mediante nuestro dispositivo 11On12 (contenido de D2D), necesitamos crear recursos ajustados de tipo [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) desde los búferes de reserva de tipo [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span><span class="sxs-lookup"><span data-stu-id="baec2-136">D3D12 owns the swap chain, so if we want to render to the back buffer using our 11On12 device (D2D content), then we need to create wrapped resources of type [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) from the back buffers of type [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource).</span></span> <span data-ttu-id="baec2-137">Esto vincula el **ID3D12Resource** con una interfaz basada en D3D11 para que se pueda usar con el dispositivo 11On12.</span><span class="sxs-lookup"><span data-stu-id="baec2-137">This links the **ID3D12Resource** with a D3D11 based interface so that it can be used with the 11On12 device.</span></span> <span data-ttu-id="baec2-138">Una vez que tenemos un recurso ajustado, podemos crear una superficie de destino de representación para que D2D se represente en, también en el método **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="baec2-138">After we have a wrapped resource, we can then create a render target surface for D2D to render to, also in the **LoadAssets** method.</span></span>

``` syntax
 // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory->GetDesktopDpi(&dpiX, &dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );  

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
```



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="baec2-139">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="baec2-139">Call flow</span></span></th>
<th><span data-ttu-id="baec2-140">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baec2-140">Parameters</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="baec2-141"><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-141"><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="baec2-142"><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-142"><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></span></span></td>
<td><dl><span data-ttu-id="baec2-143"><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-143"><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a></span></span><br />
<span data-ttu-id="baec2-144">[<strong>D2D1_BITMAP_OPTIONS</strong>] (/Windows/Desktop/API/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)</span><span class="sxs-lookup"><span data-stu-id="baec2-144">[<strong>D2D1_BITMAP_OPTIONS</strong>](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)</span></span><br />
<span data-ttu-id="baec2-145">[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)</span><span class="sxs-lookup"><span data-stu-id="baec2-145">[<strong>PixelFormat</strong>](/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)</span></span><br />
<span data-ttu-id="baec2-146">[<strong>DXGI_FORMAT</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format)</span><span class="sxs-lookup"><span data-stu-id="baec2-146">[<strong>DXGI_FORMAT</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)</span></span><br />
<span data-ttu-id="baec2-147">[<strong>D2D1_ALPHA_MODE</strong>] (/Windows/Desktop/API/dcommon/ne-dcommon-d2d1_alpha_mode)</span><span class="sxs-lookup"><span data-stu-id="baec2-147">[<strong>D2D1_ALPHA_MODE</strong>](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="baec2-148"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-148"><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></span></span></td>
<td><span data-ttu-id="baec2-149"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-149"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="baec2-150"><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain:: GetBuffer</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-150"><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain::GetBuffer</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="baec2-151"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-151"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="baec2-152"><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-152"><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></span></span></td>
<td><span data-ttu-id="baec2-153"><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-153"><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="baec2-154"><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-154"><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></span></span></td>
<td><span data-ttu-id="baec2-155"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-155"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="baec2-156"><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-156"><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="baec2-157"><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-157"><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="baec2-158"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-158"><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></span></span></td>
<td><span data-ttu-id="baec2-159"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="baec2-159"><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a><span data-ttu-id="baec2-160">Crear objetos de texto D2D básicos</span><span class="sxs-lookup"><span data-stu-id="baec2-160">Create basic D2D text objects</span></span>

<span data-ttu-id="baec2-161">Ahora tenemos un [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) para representar contenido 3D, un [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) que se comparte con nuestro dispositivo 12 a través de un [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) que se puede usar para representar contenido 2D, y ambos están configurados para representarse en la misma cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="baec2-161">Now we have an [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) to render 3D content, an [**ID2D1Device**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) that is shared with our 12 device via an [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) - which we can use to render 2D content - and they are both configured to render to the same swap chain.</span></span> <span data-ttu-id="baec2-162">En este ejemplo se usa simplemente el dispositivo D2D para representar texto en la escena 3D, de forma similar a como los juegos representan su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="baec2-162">This sample simply uses the D2D device to render text over the 3D scene, similar to how games render their UI.</span></span> <span data-ttu-id="baec2-163">Para ello, necesitamos crear algunos objetos D2D básicos, aún en el método **LoadAssets** .</span><span class="sxs-lookup"><span data-stu-id="baec2-163">For that, we need to create some basic D2D objects, still in the **LoadAssets** method.</span></span>

``` syntax
 // Create D2D/DWrite objects for rendering text.
    {
        ThrowIfFailed(m_d2dDeviceContext->CreateSolidColorBrush(D2D1::ColorF(D2D1::ColorF::Black), &m_textBrush));
        ThrowIfFailed(m_dWriteFactory->CreateTextFormat(
            L"Verdana",
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            50,
            L"en-us",
            &m_textFormat
            ));
        ThrowIfFailed(m_textFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER));
        ThrowIfFailed(m_textFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER));
    }
```



| <span data-ttu-id="baec2-164">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="baec2-164">Call flow</span></span>                                                                                           | <span data-ttu-id="baec2-165">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baec2-165">Parameters</span></span>                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="baec2-166">[**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))</span><span class="sxs-lookup"><span data-stu-id="baec2-166">[**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))</span></span>    | [<span data-ttu-id="baec2-167">**ColorF**</span><span class="sxs-lookup"><span data-stu-id="baec2-167">**ColorF**</span></span>](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [<span data-ttu-id="baec2-168">**IDWriteFactory::CreateTextFormat**</span><span class="sxs-lookup"><span data-stu-id="baec2-168">**IDWriteFactory::CreateTextFormat**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [<span data-ttu-id="baec2-169">**\_espesor de fuente de DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="baec2-169">**DWRITE\_FONT\_WEIGHT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [<span data-ttu-id="baec2-170">**IDWriteTextFormat::SetTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="baec2-170">**IDWriteTextFormat::SetTextAlignment**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [<span data-ttu-id="baec2-171">**\_alineación del texto DWRITE \_**</span><span class="sxs-lookup"><span data-stu-id="baec2-171">**DWRITE\_TEXT\_ALIGNMENT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [<span data-ttu-id="baec2-172">**IDWriteTextFormat::SetParagraphAlignment**</span><span class="sxs-lookup"><span data-stu-id="baec2-172">**IDWriteTextFormat::SetParagraphAlignment**</span></span>](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [<span data-ttu-id="baec2-173">**DWRITE \_ alineación de párrafo \_**</span><span class="sxs-lookup"><span data-stu-id="baec2-173">**DWRITE\_PARAGRAPH\_ALIGNMENT**</span></span>](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a><span data-ttu-id="baec2-174">Actualizar el bucle de representación principal</span><span class="sxs-lookup"><span data-stu-id="baec2-174">Updating the main render loop</span></span>

<span data-ttu-id="baec2-175">Ahora que se ha completado la inicialización del ejemplo, podemos pasar al bucle de representación principal.</span><span class="sxs-lookup"><span data-stu-id="baec2-175">Now that the initialization of the sample is complete, we can move on to the main render loop.</span></span>

``` syntax
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(0, 0));

    MoveToNextFrame();
}
```



| <span data-ttu-id="baec2-176">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="baec2-176">Call flow</span></span>                                                              | <span data-ttu-id="baec2-177">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baec2-177">Parameters</span></span> |
|------------------------------------------------------------------------|------------|
| [<span data-ttu-id="baec2-178">**ID3D12CommandList**</span><span class="sxs-lookup"><span data-stu-id="baec2-178">**ID3D12CommandList**</span></span>](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [<span data-ttu-id="baec2-179">**ExecuteCommandLists**</span><span class="sxs-lookup"><span data-stu-id="baec2-179">**ExecuteCommandLists**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [<span data-ttu-id="baec2-180">**IDXGISwapChain1::Present1**</span><span class="sxs-lookup"><span data-stu-id="baec2-180">**IDXGISwapChain1::Present1**</span></span>](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

<span data-ttu-id="baec2-181">Lo único que es nuevo en nuestro bucle de representación es la llamada **RenderUI** , que usará D2D para representar la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="baec2-181">The only thing new to our render loop is the **RenderUI** call, which will use D2D to render our UI.</span></span> <span data-ttu-id="baec2-182">Tenga en cuenta que todas las listas de comandos de D3D12 se ejecutan en primer lugar para representar la escena 3D y, a continuación, se presenta la interfaz de usuario sobre eso.</span><span class="sxs-lookup"><span data-stu-id="baec2-182">Notice that we execute all of our D3D12 command lists first to render our 3D scene, and then we render our UI on top of that.</span></span> <span data-ttu-id="baec2-183">Antes de profundizar en **RenderUI**, debemos observar un cambio en **PopulateCommandLists**.</span><span class="sxs-lookup"><span data-stu-id="baec2-183">Before we dive into **RenderUI**, we must look at a change to **PopulateCommandLists**.</span></span> <span data-ttu-id="baec2-184">En otros ejemplos, normalmente colocamos una barrera de recursos en la lista de comandos antes de cerrarla para pasar el búfer de reserva del estado de destino de representación al estado actual.</span><span class="sxs-lookup"><span data-stu-id="baec2-184">In other samples we commonly put a resource barrier on the command list prior to closing it to transition the back buffer from the render target state to the present state.</span></span> <span data-ttu-id="baec2-185">Sin embargo, en este ejemplo se quita esa barrera de recursos, porque todavía es necesario representarla en los búferes de reserva con D2D.</span><span class="sxs-lookup"><span data-stu-id="baec2-185">However, in this sample we remove that resource barrier, because we still need to render to the back buffers with D2D.</span></span> <span data-ttu-id="baec2-186">Tenga en cuenta que cuando se crean los recursos ajustados del búfer de reserva, se especifica el estado de destino de representación como el estado "en" y el estado actual como estado de "salida".</span><span class="sxs-lookup"><span data-stu-id="baec2-186">Note that when we created our wrapped resources of the back buffer that we specified the render target state as the “IN” state and the present state as the “OUT” state.</span></span>

<span data-ttu-id="baec2-187">**RenderUI** es bastante directo en términos de uso de D2D.</span><span class="sxs-lookup"><span data-stu-id="baec2-187">**RenderUI** is fairly straight-forward in terms of D2D usage.</span></span> <span data-ttu-id="baec2-188">Se establece el destino de representación y se representa el texto.</span><span class="sxs-lookup"><span data-stu-id="baec2-188">We set our render target and render our text.</span></span> <span data-ttu-id="baec2-189">Sin embargo, antes de usar los recursos encapsulados en un dispositivo 11On12, como los destinos de representación del búfer de reserva, debemos llamar a la API [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) en el dispositivo 11On12.</span><span class="sxs-lookup"><span data-stu-id="baec2-189">However, before using any wrapped resources on an 11On12 device, such as our back buffer render targets, we must call the [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) API on the 11On12 device.</span></span> <span data-ttu-id="baec2-190">Después de la representación se llama a la API [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) en el dispositivo 11On12.</span><span class="sxs-lookup"><span data-stu-id="baec2-190">After rendering we call the [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) API on the 11On12 device.</span></span> <span data-ttu-id="baec2-191">Al llamar a **ReleaseWrappedResources** , se incurre en una barrera de recursos en segundo plano que va a pasar el recurso especificado al estado "out" especificado en el momento de la creación.</span><span class="sxs-lookup"><span data-stu-id="baec2-191">By calling **ReleaseWrappedResources** we incur a resource barrier behind the scenes that will transition the specified resource to the “OUT” state specified at creation time.</span></span> <span data-ttu-id="baec2-192">En nuestro caso, este es el estado actual.</span><span class="sxs-lookup"><span data-stu-id="baec2-192">In our case, this is the present state.</span></span> <span data-ttu-id="baec2-193">Por último, para enviar todos los comandos que se realizaron en el dispositivo 11On12 a la [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)compartida, se debe llamar a [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) en el [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).</span><span class="sxs-lookup"><span data-stu-id="baec2-193">Finally, in order to submit all of our commands performed on the 11On12 device to the shared [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue), we must call [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) on the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext).</span></span>

``` syntax
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}
```



| <span data-ttu-id="baec2-194">Flujo de llamadas</span><span class="sxs-lookup"><span data-stu-id="baec2-194">Call flow</span></span>                                                                                                                                                                                 | <span data-ttu-id="baec2-195">Parámetros</span><span class="sxs-lookup"><span data-stu-id="baec2-195">Parameters</span></span>                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [<span data-ttu-id="baec2-196">**Tamaño de D2D1 \_ \_ F**</span><span class="sxs-lookup"><span data-stu-id="baec2-196">**D2D1\_SIZE\_F**</span></span>](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [<span data-ttu-id="baec2-197">**D2D1 \_ Rect \_ F**</span><span class="sxs-lookup"><span data-stu-id="baec2-197">**D2D1\_RECT\_F**</span></span>](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [<span data-ttu-id="baec2-198">**RectF**</span><span class="sxs-lookup"><span data-stu-id="baec2-198">**RectF**</span></span>](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [<span data-ttu-id="baec2-199">**AcquireWrappedResources**</span><span class="sxs-lookup"><span data-stu-id="baec2-199">**AcquireWrappedResources**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [<span data-ttu-id="baec2-200">**ID2D1DeviceContext::SetTarget**</span><span class="sxs-lookup"><span data-stu-id="baec2-200">**ID2D1DeviceContext::SetTarget**</span></span>](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [<span data-ttu-id="baec2-201">**ID2D1RenderTarget:: BeginDraw**</span><span class="sxs-lookup"><span data-stu-id="baec2-201">**ID2D1RenderTarget::BeginDraw**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [<span data-ttu-id="baec2-202">**ID2D1RenderTarget::SetTransform**</span><span class="sxs-lookup"><span data-stu-id="baec2-202">**ID2D1RenderTarget::SetTransform**</span></span>](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [<span data-ttu-id="baec2-203">**Matrix3x2F**</span><span class="sxs-lookup"><span data-stu-id="baec2-203">**Matrix3x2F**</span></span>](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| <span data-ttu-id="baec2-204">[**ID2D1RenderTarget::D rawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span><span class="sxs-lookup"><span data-stu-id="baec2-204">[**ID2D1RenderTarget::DrawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))</span></span> |                                       |
| [<span data-ttu-id="baec2-205">**ID2D1RenderTarget::EndDraw**</span><span class="sxs-lookup"><span data-stu-id="baec2-205">**ID2D1RenderTarget::EndDraw**</span></span>](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [<span data-ttu-id="baec2-206">**ReleaseWrappedResources**</span><span class="sxs-lookup"><span data-stu-id="baec2-206">**ReleaseWrappedResources**</span></span>](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [<span data-ttu-id="baec2-207">**ID3D11DeviceContext:: Flush**</span><span class="sxs-lookup"><span data-stu-id="baec2-207">**ID3D11DeviceContext::Flush**</span></span>](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a><span data-ttu-id="baec2-208">Ejecución del ejemplo</span><span class="sxs-lookup"><span data-stu-id="baec2-208">Run the sample</span></span>

![la salida final del ejemplo 11 en 12](images/11on12image.png)

## <a name="related-topics"></a><span data-ttu-id="baec2-210">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="baec2-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baec2-211">Tutoriales de código D3D12</span><span class="sxs-lookup"><span data-stu-id="baec2-211">D3D12 Code Walk-Throughs</span></span>](d3d12-code-walk-throughs.md)
</dt> <dt>

[<span data-ttu-id="baec2-212">Direct3D 11 en 12</span><span class="sxs-lookup"><span data-stu-id="baec2-212">Direct3D 11 on 12</span></span>](direct3d-11-on-12.md)
</dt> <dt>

[<span data-ttu-id="baec2-213">Interoperabilidad de Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="baec2-213">Direct3D 12 Interop</span></span>](direct3d-12-interop.md)
</dt> <dt>

[<span data-ttu-id="baec2-214">Referencia de 11on12</span><span class="sxs-lookup"><span data-stu-id="baec2-214">11on12 Reference</span></span>](direct3d-11on12-reference.md)
</dt> </dl>

 

 