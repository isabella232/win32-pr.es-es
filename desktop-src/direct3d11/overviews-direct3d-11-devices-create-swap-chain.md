---
title: Cómo crear una cadena de intercambio
description: En este tema se muestra cómo crear una cadena de intercambio que encapsule dos o más búferes que se usan para la representación y presentación.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104421047"
---
# <a name="how-to-create-a-swap-chain"></a>Cómo: crear una cadena de intercambio

En este tema se muestra cómo crear una cadena de intercambio que encapsule dos o más búferes que se usan para la representación y presentación. Normalmente contienen un búfer frontal que se presenta al dispositivo de pantalla y un búfer de reserva que actúa como destino de representación. Una vez que el contexto inmediato finaliza la representación en el búfer de reserva, la cadena de intercambio presenta el búfer de reserva intercambiando los dos búferes.

La cadena de intercambio define varias características de representación, entre las que se incluyen:

-   Tamaño del área de representación.
-   La frecuencia de actualización de la pantalla.
-   Modo de presentación.
-   El formato de la superficie.

Defina las características de la cadena de intercambio rellenando una estructura de DESC de cadena de intercambio de DXGI e inicializando una interfaz [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) . [**\_ \_ \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) Inicialice una cadena de intercambio mediante una llamada a [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="create-a-device-and-a-swap-chain"></a>Crear un dispositivo y una cadena de intercambio

Para inicializar un dispositivo y una cadena de intercambio, utilice una de las dos funciones siguientes:

-   Utilice la función [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) cuando desee inicializar la cadena de intercambio al mismo tiempo que la inicialización del dispositivo. Normalmente, esta es la opción más sencilla.

-   Use la función [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) cuando ya haya creado una cadena de intercambio mediante [**IDXGIFactory:: CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Cómo usar Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 