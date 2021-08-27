---
title: Cómo obtener los modos de presentación del adaptador
description: En este tema se muestra cómo usar Microsoft Infraestructura de gráficos de DirectX (DXGI) para obtener los modos de presentación válidos asociados a un adaptador.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921d373a9ff0f79baaf848a55cbab0d08fd4e119d30a0a0cb917832830589dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119575"
---
# <a name="how-to-get-adapter-display-modes"></a>Cómo: Obtener modos de presentación del adaptador

En este tema se muestra cómo usar Microsoft Infraestructura de gráficos de DirectX (DXGI) para obtener los modos de presentación válidos asociados a un adaptador. DirectX 10 y 11 pueden usar DXGI para obtener los modos de visualización válidos. Conocer los modos de presentación válidos garantiza que la aplicación puede elegir correctamente un modo de pantalla completa válido.

**Para obtener los modos de presentación del adaptador**

1.  Cree un [**objeto IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) y úselo para enumerar los adaptadores disponibles. Para obtener más información, [vea Cómo: Enumerar adaptadores](overviews-direct3d-11-devices-enum.md).
2.  Llame a IDXGIAdapter::EnumOutputs para enumerar las salidas de cada adaptador.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Llame a IDXGIOutput::GetDisplayModeList para recuperar una matriz de estructuras [**\_ \_ DESC DXGI MODE**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) y el número de elementos de la matriz. Cada **estructura \_ \_ DESC DEL MODO DXGI** representa un modo de presentación válido para la salida.
    ```
    UINT numModes = 0;
    DXGI_MODE_DESC* displayModes = NULL;
    DXGI_FORMAT format = DXGI_FORMAT_R32G32B32A32_FLOAT;

        // Get the number of elements
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, NULL);

        displayModes = new DXGI_MODE_DESC[numModes]; 

        // Get the list
        hr = pOutput->GetDisplayModeList( format, 0, &numModes, displayModes);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 