---
description: Comprobación de los formatos DXVA-HD admitidos
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Comprobación de los formatos DXVA-HD admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090013"
---
# <a name="checking-supported-dxva-hd-formats"></a><span data-ttu-id="fc54d-103">Comprobación de los formatos DXVA-HD admitidos</span><span class="sxs-lookup"><span data-stu-id="fc54d-103">Checking Supported DXVA-HD Formats</span></span>

## <a name="checking-supported-input-formats"></a><span data-ttu-id="fc54d-104">Comprobar los formatos de entrada admitidos</span><span class="sxs-lookup"><span data-stu-id="fc54d-104">Checking Supported Input Formats</span></span>

<span data-ttu-id="fc54d-105">Para obtener una lista de los formatos de entrada que admite el dispositivo de alta definición de aceleración de vídeo (DXVA-HD) de Microsoft DirectX, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc54d-105">To get a list of the input formats that the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device supports, do the following:</span></span>

1.  <span data-ttu-id="fc54d-106">Llame [**a IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc54d-106">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="fc54d-107">Compruebe el **miembro InputFormatCount** de la [**estructura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="fc54d-107">Check the **InputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="fc54d-108">Este miembro proporciona el número de formatos de entrada admitidos.</span><span class="sxs-lookup"><span data-stu-id="fc54d-108">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="fc54d-109">Asigne una matriz **de valores D3DFORMAT,** de tamaño **InputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="fc54d-109">Allocate an array of **D3DFORMAT** values, of size **InputFormatCount**.</span></span>
4.  <span data-ttu-id="fc54d-110">Pase esta matriz [**al método IDXVAHD \_ Device::GetVideoProcessorInputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats)</span><span class="sxs-lookup"><span data-stu-id="fc54d-110">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorInputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) method.</span></span> <span data-ttu-id="fc54d-111">Los métodos rellenan la matriz con una lista de formatos de entrada.</span><span class="sxs-lookup"><span data-stu-id="fc54d-111">The methods fills the array with a list of input formats.</span></span>

<span data-ttu-id="fc54d-112">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="fc54d-112">The following code shows these steps:</span></span>


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



## <a name="checking-supported-output-formats"></a><span data-ttu-id="fc54d-113">Comprobar los formatos de salida admitidos</span><span class="sxs-lookup"><span data-stu-id="fc54d-113">Checking Supported Output Formats</span></span>

<span data-ttu-id="fc54d-114">Para obtener una lista de los formatos de salida que admite el dispositivo DXVA-HD, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="fc54d-114">To get a list of the output formats that the DXVA-HD device supports, do the following:</span></span>

1.  <span data-ttu-id="fc54d-115">Llame [**a IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fc54d-115">Call [**IDXVAHD\_Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) to get the device capabilities.</span></span>
2.  <span data-ttu-id="fc54d-116">Compruebe el **miembro OutputFormatCount** de la [**estructura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps)</span><span class="sxs-lookup"><span data-stu-id="fc54d-116">Check the **OutputFormatCount** member of the [**DXVAHD\_VPDEVCAPS**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) structure.</span></span> <span data-ttu-id="fc54d-117">Este miembro proporciona el número de formatos de entrada admitidos.</span><span class="sxs-lookup"><span data-stu-id="fc54d-117">This member gives the number of supported input formats.</span></span>
3.  <span data-ttu-id="fc54d-118">Asigne una matriz de **valores D3DFORMAT,** de tamaño **OutputFormatCount**.</span><span class="sxs-lookup"><span data-stu-id="fc54d-118">Allocate an array of **D3DFORMAT** values, of size **OutputFormatCount**.</span></span>
4.  <span data-ttu-id="fc54d-119">Pase esta matriz al [**método IDXVAHD \_ Device::GetVideoProcessorOutputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats)</span><span class="sxs-lookup"><span data-stu-id="fc54d-119">Pass this array to the [**IDXVAHD\_Device::GetVideoProcessorOutputFormats**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) method.</span></span> <span data-ttu-id="fc54d-120">Los métodos rellenan la matriz con una lista de formatos de salida.</span><span class="sxs-lookup"><span data-stu-id="fc54d-120">The methods fills the array with a list of output formats.</span></span>

<span data-ttu-id="fc54d-121">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="fc54d-121">The following code shows these steps:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="fc54d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fc54d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fc54d-123">DXVA-HD</span><span class="sxs-lookup"><span data-stu-id="fc54d-123">DXVA-HD</span></span>](dxva-hd.md)
</dt> </dl>

 

 



