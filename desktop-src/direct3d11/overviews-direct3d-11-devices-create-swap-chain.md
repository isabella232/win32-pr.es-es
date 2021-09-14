---
title: Cómo crear una cadena de intercambio
description: En este tema se muestra cómo crear una cadena de intercambio que encapsula dos o más búferes que se usan para representar y mostrar.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358892"
---
# <a name="how-to-create-a-swap-chain"></a>Cómo: Crear una cadena de intercambio

En este tema se muestra cómo crear una cadena de intercambio que encapsula dos o más búferes que se usan para representar y mostrar. Normalmente contienen un búfer frontal que se presenta al dispositivo de visualización y un búfer de reserva que actúa como destino de representación. Una vez que se realiza la representación del contexto inmediato en el búfer de reserva, la cadena de intercambio presenta el búfer de reserva intercambiando los dos búferes.

La cadena de intercambio define varias características de representación, entre las que se incluyen:

-   Tamaño del área de representación.
-   Frecuencia de actualización de pantalla.
-   Modo de presentación.
-   Formato de superficie.

Defina las características de la cadena de intercambio rellenando una estructura [**\_ DXGI SWAP \_ CHAIN \_ DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) e inicializando una [**interfaz IDXGISwapChain.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) Inicialice una cadena de intercambio mediante una llamada [**a IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).

## <a name="create-a-device-and-a-swap-chain"></a>Creación de un dispositivo y una cadena de intercambio

Para inicializar un dispositivo y una cadena de intercambio, use una de las dos funciones siguientes:

-   Use la [**función D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) cuando desee inicializar la cadena de intercambio al mismo tiempo que la inicialización del dispositivo. Esta suele ser la opción más sencilla.

-   Use la [**función D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) cuando ya haya creado una cadena de intercambio mediante [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Uso de Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 