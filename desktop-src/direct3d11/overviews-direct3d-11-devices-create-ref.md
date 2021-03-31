---
title: Creación de un dispositivo de referencia
description: En este tema se muestra cómo crear un dispositivo de referencia que implementa una implementación de software muy precisa del tiempo de ejecución.
ms.assetid: 00d3f5f2-02c6-4ff4-82a9-0726ad4a8cb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dec5f3834bf1f10027da2a3f3a8e22acdee742b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418989"
---
# <a name="how-to-create-a-reference-device"></a><span data-ttu-id="6045e-103">Cómo: crear un dispositivo de referencia</span><span class="sxs-lookup"><span data-stu-id="6045e-103">How To: Create a Reference Device</span></span>

<span data-ttu-id="6045e-104">En este tema se muestra cómo crear un dispositivo de referencia que implementa una implementación de software muy precisa del tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="6045e-104">This topic shows how to create a reference device that implements a highly accurate, software implementation of the runtime.</span></span> <span data-ttu-id="6045e-105">Para crear un dispositivo de referencia, simplemente especifique que el dispositivo que está creando usará un controlador de referencia.</span><span class="sxs-lookup"><span data-stu-id="6045e-105">To create a reference device, simply specify that the device you are creating will use a reference driver.</span></span> <span data-ttu-id="6045e-106">En este ejemplo se crea un dispositivo y una cadena de intercambio al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="6045e-106">This example creates a device and a swap chain at the same time.</span></span>

<span data-ttu-id="6045e-107">**Para crear un dispositivo de referencia**</span><span class="sxs-lookup"><span data-stu-id="6045e-107">**To create a reference device**</span></span>

1.  <span data-ttu-id="6045e-108">Defina los parámetros iniciales de una cadena de intercambio.</span><span class="sxs-lookup"><span data-stu-id="6045e-108">Define initial parameters for a swap chain.</span></span>
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

    

2.  <span data-ttu-id="6045e-109">Solicite un nivel de características que implemente las características que necesitará la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6045e-109">Request a feature level that implements the features your application will need.</span></span> <span data-ttu-id="6045e-110">Se puede crear correctamente un dispositivo de referencia para el tiempo de ejecución de Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="6045e-110">A reference device can be successfully created for the Direct3D 11 runtime.</span></span>

    ```
        D3D_FEATURE_LEVEL FeatureLevels = D3D_FEATURE_LEVEL_11_0;
    ```

    

    <span data-ttu-id="6045e-111">Vea más información sobre los niveles de características en la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="6045e-111">See more about feature levels in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span>

3.  <span data-ttu-id="6045e-112">Cree el dispositivo mediante una llamada a [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span><span class="sxs-lookup"><span data-stu-id="6045e-112">Create the device by calling [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>


```
    HRESULT hr = S_OK;
    D3D_FEATURE_LEVEL FeatureLevel;

    if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                    D3D_DRIVER_TYPE_REFERENCE,
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



<span data-ttu-id="6045e-113">Tendrá que proporcionar la llamada de API con el tipo de controlador de referencia de la enumeración de [**\_ \_ tipo de controlador D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) .</span><span class="sxs-lookup"><span data-stu-id="6045e-113">You will need to supply the API call with the reference driver type from the [**D3D\_DRIVER\_TYPE**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) enumeration.</span></span> <span data-ttu-id="6045e-114">Una vez que el método se ejecuta correctamente, devolverá una interfaz de la cadena de intercambio, una interfaz de dispositivo, un puntero al nivel de característica que ha concedido el controlador y una interfaz de contexto inmediata.</span><span class="sxs-lookup"><span data-stu-id="6045e-114">After the method succeeds, it will return a swap chain interface, a device interface, a pointer to the feature level that was granted by the driver, and an immediate context interface.</span></span>

<span data-ttu-id="6045e-115">Para obtener información sobre las limitaciones de la creación de un dispositivo de referencia en determinados niveles de características, vea [limitaciones para crear dispositivos de Hipersalto y de referencia](overviews-direct3d-11-devices-limitations.md). [Cómo usar Direct3D 11](how-to-use-direct3d-11.md)</span><span class="sxs-lookup"><span data-stu-id="6045e-115">For information about limitations creating a reference device on certain feature levels, see [Limitations Creating WARP and Reference Devices](overviews-direct3d-11-devices-limitations.md).[How to Use Direct3D 11](how-to-use-direct3d-11.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="6045e-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6045e-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6045e-117">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="6045e-117">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="6045e-118">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="6045e-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




