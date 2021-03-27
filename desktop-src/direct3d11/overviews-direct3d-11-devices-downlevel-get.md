---
title: Cómo obtener el nivel de características del dispositivo
description: En este tema se muestra cómo obtener el nivel de características más alto compatible con un dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903752"
---
# <a name="how-to-get-the-device-feature-level"></a><span data-ttu-id="adf12-103">Cómo: obtener el nivel de características del dispositivo</span><span class="sxs-lookup"><span data-stu-id="adf12-103">How To: Get the Device Feature Level</span></span>

<span data-ttu-id="adf12-104">En este tema se muestra cómo obtener el [nivel de características](overviews-direct3d-11-devices-downlevel-intro.md) más alto compatible con un [dispositivo](overviews-direct3d-11-devices-intro.md).</span><span class="sxs-lookup"><span data-stu-id="adf12-104">This topics shows how to get the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a [device](overviews-direct3d-11-devices-intro.md).</span></span> <span data-ttu-id="adf12-105">Los dispositivos de Direct3D 11 admiten un conjunto fijo de niveles de características que se definen en la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="adf12-105">Direct3D 11 devices support a fixed set of feature levels that are defined in the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration.</span></span> <span data-ttu-id="adf12-106">Cuando conozca el nivel de [característica](overviews-direct3d-11-devices-downlevel-intro.md) más alto compatible con un dispositivo, puede ejecutar rutas de acceso de código apropiadas para ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="adf12-106">When you know the highest [feature level](overviews-direct3d-11-devices-downlevel-intro.md) supported by a device, you can run code paths that are appropriate for that device.</span></span>

<span data-ttu-id="adf12-107">**Para obtener el nivel de características del dispositivo**</span><span class="sxs-lookup"><span data-stu-id="adf12-107">**To get the device feature level**</span></span>

1.  <span data-ttu-id="adf12-108">Llame a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o a las funciones [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) al especificar **null** para el parámetro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="adf12-108">Call either the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function or the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) functions while specifying **NULL** for the *ppDevice* parameter.</span></span> <span data-ttu-id="adf12-109">Puede hacerlo antes de crear el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="adf12-109">You can do this before device creation.</span></span>

    <span data-ttu-id="adf12-110">\- o -</span><span class="sxs-lookup"><span data-stu-id="adf12-110">\- or -</span></span>

    <span data-ttu-id="adf12-111">Llame a [**ID3D11Device:: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) después de la creación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="adf12-111">Call [**ID3D11Device::GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) after device creation.</span></span>

2.  <span data-ttu-id="adf12-112">Examine el valor de la enumeración de [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) devuelta desde el último paso para determinar el nivel de característica admitido.</span><span class="sxs-lookup"><span data-stu-id="adf12-112">Examine the value of the returned [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumeration from the last step to determine the supported feature level.</span></span>

<span data-ttu-id="adf12-113">En el ejemplo de código siguiente se muestra cómo determinar el nivel de característica compatible más alto mediante una llamada a la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) .</span><span class="sxs-lookup"><span data-stu-id="adf12-113">The following code example demonstrates how to determine the highest supported feature level by calling the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function.</span></span> <span data-ttu-id="adf12-114">**D3D11CreateDevice** almacena el nivel de características admitido más alto en la variable FeatureLevel.</span><span class="sxs-lookup"><span data-stu-id="adf12-114">**D3D11CreateDevice** stores the highest supported feature level in the FeatureLevel variable.</span></span> <span data-ttu-id="adf12-115">Puede usar este código para examinar el valor del tipo enumerado del [**\_ \_ nivel de característica D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) que devuelve **D3D11CreateDevice** .</span><span class="sxs-lookup"><span data-stu-id="adf12-115">You can use this code to examine the value of the [**D3D\_FEATURE\_LEVEL**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) enumerated type that **D3D11CreateDevice** returns.</span></span> <span data-ttu-id="adf12-116">Tenga en cuenta que en este código se enumeran todos los niveles de características explícitamente (para Direct3D 11,1 y Direct3D 11,2).</span><span class="sxs-lookup"><span data-stu-id="adf12-116">Note that this code lists all feature levels explicitly (for Direct3D 11.1 and Direct3D 11.2).</span></span>

> [!Note]  
> <span data-ttu-id="adf12-117">Si el tiempo de ejecución de Direct3D 11,1 está presente en el equipo y *pFeatureLevels* está establecido en **null**, esta función no creará un dispositivo de [**nivel de característica de D3D \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) .</span><span class="sxs-lookup"><span data-stu-id="adf12-117">If the Direct3D 11.1 runtime is present on the computer and *pFeatureLevels* is set to **NULL**, this function won't create a [**D3D\_FEATURE\_LEVEL\_11\_1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) device.</span></span> <span data-ttu-id="adf12-118">Para crear un dispositivo de **nivel de característica de D3D \_ \_ \_ 11 \_ 1** , debe proporcionar explícitamente una matriz de **\_ \_ nivel de característica D3D** que incluya el **nivel de característica de D3D \_ \_ \_ 11 \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="adf12-118">To create a **D3D\_FEATURE\_LEVEL\_11\_1** device, you must explicitly provide a **D3D\_FEATURE\_LEVEL** array that includes **D3D\_FEATURE\_LEVEL\_11\_1**.</span></span> <span data-ttu-id="adf12-119">Si proporciona una matriz **de \_ \_ nivel de característica D3D** que contiene el **nivel de característica de D3D \_ \_ \_ 11 \_ 1** en un equipo que no tiene instalado el tiempo de ejecución de Direct3D 11,1, esta función genera un error inmediatamente con E \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="adf12-119">If you provide a **D3D\_FEATURE\_LEVEL** array that contains **D3D\_FEATURE\_LEVEL\_11\_1** on a computer that doesn't have the Direct3D 11.1 runtime installed, this function immediately fails with E\_INVALIDARG.</span></span>

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



<span data-ttu-id="adf12-120">En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.</span><span class="sxs-lookup"><span data-stu-id="adf12-120">The [10Level9 Reference](d3d11-graphics-reference-10level9.md) section lists the differences between how various [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) and [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) methods behave at various 10Level9 feature levels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="adf12-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="adf12-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="adf12-122">Direct3D 11 en hardware de nivel inferior</span><span class="sxs-lookup"><span data-stu-id="adf12-122">Direct3D 11 on Downlevel Hardware</span></span>](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[<span data-ttu-id="adf12-123">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="adf12-123">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




