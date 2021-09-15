---
description: Comprobación de los formatos DXVA-HD admitidos
ms.assetid: 43ae9f70-34a1-48ca-be61-e974e2daebd7
title: Comprobación de los formatos DXVA-HD admitidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d07d47043ed200d256e2bef8fa2c9ab6717f3b82
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574985"
---
# <a name="checking-supported-dxva-hd-formats"></a>Comprobación de los formatos DXVA-HD admitidos

## <a name="checking-supported-input-formats"></a>Comprobar los formatos de entrada admitidos

Para obtener una lista de los formatos de entrada que admite el dispositivo de alta definición de aceleración de vídeo (DXVA-HD) de Microsoft DirectX, haga lo siguiente:

1.  Llame [**a IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.
2.  Compruebe el **miembro InputFormatCount** de la [**estructura DXVAHD \_ VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Este miembro proporciona el número de formatos de entrada admitidos.
3.  Asigne una matriz de **valores D3DFORMAT,** de tamaño **InputFormatCount.**
4.  Pase esta matriz al [**método IDXVAHD \_ Device::GetVideoProcessorInputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessorinputformats) Los métodos rellenan la matriz con una lista de formatos de entrada.

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

1.  Llame [**a IDXVAHD \_ Device::GetVideoProcessorDeviceCaps**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps) para obtener las funcionalidades del dispositivo.
2.  Compruebe el **miembro OutputFormatCount** de la [**estructura \_ DXVAHD VPDEVCAPS.**](/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps) Este miembro proporciona el número de formatos de entrada admitidos.
3.  Asigne una matriz de **valores D3DFORMAT,** de tamaño **OutputFormatCount.**
4.  Pase esta matriz al [**método IDXVAHD \_ Device::GetVideoProcessorOutputFormats.**](/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessoroutputformats) Los métodos rellenan la matriz con una lista de formatos de salida.

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

 

 



