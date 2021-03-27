---
title: Cómo obtener modos de presentación de adaptador
description: En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para obtener los modos de presentación válidos asociados a un adaptador.
ms.assetid: 3d182f29-48d4-4e25-b34e-b424cc9eed0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c2602fcd4e1baa4476bb89273eda676f444e38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358998"
---
# <a name="how-to-get-adapter-display-modes"></a>Cómo: obtener modos de presentación de adaptador

En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para obtener los modos de presentación válidos asociados a un adaptador. DirectX 10 y 11 pueden usar DXGI para obtener los modos de presentación válidos. Conocer los modos de presentación válidos garantiza que la aplicación puede elegir correctamente un modo de pantalla completa válido.

**Para obtener los modos de presentación del adaptador**

1.  Cree un objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) y úselo para enumerar los adaptadores disponibles. Para obtener más información, consulte [Cómo: enumerar adaptadores](overviews-direct3d-11-devices-enum.md).
2.  Llame a IDXGIAdapter:: EnumOutputs para enumerar las salidas de cada adaptador.
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  Llame a IDXGIOutput:: GetDisplayModeList para recuperar una matriz de las estructuras [**\_ \_ DESC del modo DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) y el número de elementos de la matriz. Cada estructura de **\_ \_ DESC del modo de DXGI** representa un modo de presentación válido para la salida.
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

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 