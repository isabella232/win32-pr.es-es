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
# <a name="how-to-get-adapter-display-modes"></a><span data-ttu-id="5ba9a-103">Cómo: obtener modos de presentación de adaptador</span><span class="sxs-lookup"><span data-stu-id="5ba9a-103">How To: Get Adapter Display Modes</span></span>

<span data-ttu-id="5ba9a-104">En este tema se muestra cómo usar la infraestructura de gráficos de Microsoft DirectX (DXGI) para obtener los modos de presentación válidos asociados a un adaptador.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-104">This topic shows how to use Microsoft DirectX Graphics Infrastructure (DXGI) to get the valid display modes associated with an adapter.</span></span> <span data-ttu-id="5ba9a-105">DirectX 10 y 11 pueden usar DXGI para obtener los modos de presentación válidos.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-105">DirectX 10 and 11 can use DXGI to get the valid display modes.</span></span> <span data-ttu-id="5ba9a-106">Conocer los modos de presentación válidos garantiza que la aplicación puede elegir correctamente un modo de pantalla completa válido.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-106">Knowing the valid display modes ensures that your application can properly choose a valid full-screen mode.</span></span>

<span data-ttu-id="5ba9a-107">**Para obtener los modos de presentación del adaptador**</span><span class="sxs-lookup"><span data-stu-id="5ba9a-107">**To get adapter display modes**</span></span>

1.  <span data-ttu-id="5ba9a-108">Cree un objeto [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) y úselo para enumerar los adaptadores disponibles.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-108">Create an [**IDXGIFactory**](/windows/desktop/api/dxgi/nn-dxgi-idxgifactory) object and use it to enumerate the available adapters.</span></span> <span data-ttu-id="5ba9a-109">Para obtener más información, consulte [Cómo: enumerar adaptadores](overviews-direct3d-11-devices-enum.md).</span><span class="sxs-lookup"><span data-stu-id="5ba9a-109">For more information, see [How To: Enumerate Adapters](overviews-direct3d-11-devices-enum.md).</span></span>
2.  <span data-ttu-id="5ba9a-110">Llame a IDXGIAdapter:: EnumOutputs para enumerar las salidas de cada adaptador.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-110">Call IDXGIAdapter::EnumOutputs to enumerate the outputs for each adapter.</span></span>
    ```
    IDXGIOutput* pOutput = NULL; 
    HRESULT hr;

    hr = pAdapter->EnumOutputs(0,&pOutput);
    ```

    

3.  <span data-ttu-id="5ba9a-111">Llame a IDXGIOutput:: GetDisplayModeList para recuperar una matriz de las estructuras [**\_ \_ DESC del modo DXGI**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) y el número de elementos de la matriz.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-111">Call IDXGIOutput::GetDisplayModeList to retrieve an array of [**DXGI\_MODE\_DESC**](/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)) structures and the number of elements in the array.</span></span> <span data-ttu-id="5ba9a-112">Cada estructura de **\_ \_ DESC del modo de DXGI** representa un modo de presentación válido para la salida.</span><span class="sxs-lookup"><span data-stu-id="5ba9a-112">Each **DXGI\_MODE\_DESC** structure represents a valid display mode for the output.</span></span>
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

    

## <a name="related-topics"></a><span data-ttu-id="5ba9a-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ba9a-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ba9a-114">Dispositivos</span><span class="sxs-lookup"><span data-stu-id="5ba9a-114">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="5ba9a-115">Cómo usar Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="5ba9a-115">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 