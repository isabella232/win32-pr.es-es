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
# <a name="checking-supported-dxva-hd-formats"></a>Comprobando formatos de DXVA compatibles: HD

## <a name="checking-supported-input-formats"></a>Comprobando formatos de entrada admitidos

Para obtener una lista de los formatos de entrada que admite el dispositivo de alta definición de Microsoft DirectX video Acceleration (DXVA-HD), haga lo siguiente:

1.  Llame a [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.
2.  Compruebe el miembro **InputFormatCount** de la [**estructura \_ VPDEVCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Este miembro proporciona el número de formatos de entrada admitidos.
3.  Asigne una matriz de valores **D3DFORMAT** , de tamaño **InputFormatCount**.
4.  Pase esta matriz al método [**\_ Device:: GetVideoProcessorInputFormats de IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) . Los métodos llenan la matriz con una lista de formatos de entrada.

El siguiente código muestra estos pasos:


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



## <a name="checking-supported-output-formats"></a>Comprobar los formatos de salida admitidos

Para obtener una lista de los formatos de salida que admite el dispositivo DXVA-HD, haga lo siguiente:

1.  Llame a [**IDXVAHD \_ Device:: GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.
2.  Compruebe el miembro **OutputFormatCount** de la [**estructura \_ VPDEVCAPS de DXVAHD**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) . Este miembro proporciona el número de formatos de entrada admitidos.
3.  Asigne una matriz de valores **D3DFORMAT** , de tamaño **OutputFormatCount**.
4.  Pase esta matriz al método [**\_ Device:: GetVideoProcessorOutputFormats de IDXVAHD**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) . Los métodos llenan la matriz con una lista de formatos de salida.

El siguiente código muestra estos pasos:


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DXVA-HD](dxva-hd.md)
</dt> </dl>

 

 



