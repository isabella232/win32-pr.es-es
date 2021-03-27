---
title: Creación de un dispositivo WARP
description: En este tema se muestra cómo crear un dispositivo de ALABEo que implementa un rasterizador de software de alta velocidad.
ms.assetid: 6daf661e-bc24-4b90-83a7-031acb57cf87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deda409971d22f46132a1cb9b008d3dd1eb7c407
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997109"
---
# <a name="how-to-create-a-warp-device"></a><span data-ttu-id="14994-103">Cómo: crear un dispositivo WARP</span><span class="sxs-lookup"><span data-stu-id="14994-103">How To: Create a WARP Device</span></span>

<span data-ttu-id="14994-104">En este tema se muestra cómo crear un dispositivo de ALABEo que implementa un rasterizador de software de alta velocidad.</span><span class="sxs-lookup"><span data-stu-id="14994-104">This topic shows how to create a WARP device that implements a high speed software rasterizer.</span></span> <span data-ttu-id="14994-105">Para crear un dispositivo de deformación, simplemente especifique que el dispositivo que está creando usará un controlador WARP.</span><span class="sxs-lookup"><span data-stu-id="14994-105">To create a WARP device, simply specify that the device you are creating will use a WARP driver.</span></span> <span data-ttu-id="14994-106">En este ejemplo se crea un dispositivo y una cadena de intercambio al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="14994-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="14994-107">**Para crear un dispositivo WARP**</span><span class="sxs-lookup"><span data-stu-id="14994-107">**To create a WARP device**</span></span>

1.  <span data-ttu-id="14994-108">Defina los parámetros iniciales de una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="14994-108">Define initial parameters for a swap chain.</span></span>
    ```
        DXGI_SWAP_CHAIN_DESC sd;
        ZeroMemory( &sd, sizeof( sd ) );
        sd.BufferCount = 1;
        sd.BufferDesc.Width = 640;
        sd.BufferDesc.Height = 480;
        sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
        sd.BufferDesc.RefreshRate.Numerator = 60;
        sd.BufferDesc.RefreshRate.Denominator = 1;
        sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        sd.OutputWindow = g_hWnd;
        sd.SampleDesc.Count = 1;
        sd.SampleDesc.Quality = 0;
        sd.Windowed = TRUE;
    ```

    

2.  <span data-ttu-id="14994-109">Solicite un nivel de características que implemente las características que necesitará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="14994-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="14994-110">Se puede crear correctamente un dispositivo de deformación para niveles de características D3D de nivel de característica del **\_ \_ \_ \_ 1** al **nivel de características de D3d \_ \_ \_ 10 \_ 1** y a partir de Windows 8 para todos los niveles de características.</span><span class="sxs-lookup"><span data-stu-id="14994-110">A WARP device can be successfully created for feature levels **D3D\_FEATURE\_LEVEL\_9\_1** through **D3D\_FEATURE\_LEVEL\_10\_1** and starting with Windows 8 for all feature levels.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_10_1;
    ```

    

    <span data-ttu-id="14994-111">Vea más información sobre los niveles de características en la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="14994-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="14994-112">Cree el dispositivo mediante una llamada a [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="14994-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_WARP,
                    NULL, 
                    0,
                    &FeatureLevels, 
                    1, 
                    D3D11_SDK_VERSION, 
                    &sd, 
                    &g_pSwapChain, 
                    &g_pd3dDevice, 
                    &FeatureLevel,
                    &g_pImmediateContext )))
    {
        return hr;
    }
```



<span data-ttu-id="14994-113">Tendrá que proporcionar la llamada de API con el tipo de controlador WARP desde la enumeración de [**\_ \_ tipo de controlador D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="14994-113">You will need to supply the API call with the WARP driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="14994-114">Una vez que el método se ejecuta correctamente, devolverá una interfaz de la cadena de intercambio, una interfaz de dispositivo, un puntero al nivel de característica que ha concedido el controlador y una interfaz de contexto inmediata.</span><span class="sxs-lookup"><span data-stu-id="14994-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="14994-115">Para obtener información sobre las limitaciones de la creación de un dispositivo de deformación en determinados niveles de características, vea [limitaciones para crear dispositivos de Hipersalto y de referencia](overviews-direct3d-11-devices-limitations.md).</span><span class="sxs-lookup"><span data-stu-id="14994-115">For information about limitations creating a WARP device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).</span></span>

## <a name="new-for-windows-8"></a><span data-ttu-id="14994-116">Novedades de Windows 8</span><span class="sxs-lookup"><span data-stu-id="14994-116">New for Windows 8</span></span>

<span data-ttu-id="14994-117">Cuando el adaptador de pantalla principal de un equipo es el "adaptador de pantalla básico de Microsoft" (adaptador de deformación), ese equipo también tiene un segundo adaptador.</span><span class="sxs-lookup"><span data-stu-id="14994-117">When a computer's primary display adapter is the "Microsoft Basic Display Adapter" (WARP adapter), that computer also has a second adapter.</span></span> <span data-ttu-id="14994-118">Este segundo adaptador es el dispositivo de solo representación que no tiene salidas de presentación.</span><span class="sxs-lookup"><span data-stu-id="14994-118">This second adapter is the render-only device that has no display outputs.</span></span> <span data-ttu-id="14994-119">Para obtener más información sobre el dispositivo de solo representación, consulte [nueva información en Windows 8 acerca de la enumeración de adaptadores](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span><span class="sxs-lookup"><span data-stu-id="14994-119">For more info about the render-only device, see [new info in Windows 8 about enumerating adapters](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).</span></span>

## <a name="related-topics"></a><span data-ttu-id="14994-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14994-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14994-121">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="14994-121">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="14994-122">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="14994-122">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 