---
description: .
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: 'Comprobando formatos de DXVA compatibles: HD'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7560d574cee5fca21ab8de78b01b87af1de5a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496846"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="b33f4-103">Comprobando formatos de DXVA compatibles: HD</span><span class="sxs-lookup"><span data-stu-id="b33f4-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="b33f4-104">Comprobando formatos de entrada admitidos</span><span class="sxs-lookup"><span data-stu-id="b33f4-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="b33f4-105">Para obtener una lista de los formatos de entrada que admite el dispositivo de alta definición de Microsoft DirectX video Acceleration (DXVA-HD), haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b33f4-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="b33f4-106">Llame a [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b33f4-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="b33f4-107">Compruebe el miembro **InputFormatCount** de la [**estructura \_ VPDEVCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="b33f4-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="b33f4-108">Este miembro proporciona el número de formatos de entrada admitidos.</span><span class="sxs-lookup"><span data-stu-id="b33f4-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="b33f4-109">Asigne una matriz de valores **D3DFORMAT** , de tamaño **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="b33f4-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="b33f4-110">Pase esta matriz al método [**\_ Device:: GetVideoProcessorInputFormats de IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) .</span><span class="sxs-lookup"><span data-stu-id="b33f4-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="b33f4-111">Los métodos llenan la matriz con una lista de formatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="b33f4-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="b33f4-112">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b33f4-112">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified input format.

HRESULT CheckInputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[ caps.InputFormatCount ];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorInputFormats(
        caps.InputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.InputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.InputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="checking-supported-output-formats"></a><span data-ttu-id="b33f4-113">Comprobar los formatos de salida admitidos</span><span class="sxs-lookup"><span data-stu-id="b33f4-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="b33f4-114">Para obtener una lista de los formatos de salida que admite el dispositivo DXVA-HD, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="b33f4-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="b33f4-115">Llame a [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b33f4-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="b33f4-116">Compruebe el miembro **OutputFormatCount** de la [**estructura \_ VPDEVCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) .</span><span class="sxs-lookup"><span data-stu-id="b33f4-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="b33f4-117">Este miembro proporciona el número de formatos de entrada admitidos.</span><span class="sxs-lookup"><span data-stu-id="b33f4-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="b33f4-118">Asigne una matriz de valores **D3DFORMAT** , de tamaño **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="b33f4-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="b33f4-119">Pase esta matriz al método [**\_ Device:: GetVideoProcessorOutputFormats de IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) .</span><span class="sxs-lookup"><span data-stu-id="b33f4-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="b33f4-120">Los métodos llenan la matriz con una lista de formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="b33f4-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="b33f4-121">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="b33f4-121">The following code shows these steps:</span></span>


```C++
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b33f4-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b33f4-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b33f4-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="b33f4-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



