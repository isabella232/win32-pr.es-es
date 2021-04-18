---
description: Direct3D proporciona las siguientes funciones para determinar la compatibilidad de hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinar la compatibilidad de hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714701"
---
# <a name="determining-hardware-support-direct3d-9"></a>Determinar la compatibilidad de hardware (Direct3D 9)

Direct3D proporciona las siguientes funciones para determinar la compatibilidad de hardware.

-   [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Se usa para comprobar si un formato de superficie se puede usar como textura, si se puede usar un formato de superficie como una textura y un destino de representación, o si se puede usar un formato de superficie como búfer de estarcido de profundidad. Además, este método se usa para comprobar la compatibilidad con el formato de búfer de profundidad y la compatibilidad con el formato de búfer de estarcido de profundidad.

-   [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Se usa para comprobar la capacidad de un dispositivo para realizar la aceleración de hardware, la capacidad de un dispositivo para crear una cadena de intercambio para la presentación o la capacidad de un dispositivo para representarse en el formato de presentación actual.

-   [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Se usa para comprobar si un formato de búfer de estarcido de profundidad es compatible con un formato de destino de representación. Tenga en cuenta que, antes de llamar a este método, la aplicación debe llamar a [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) en los formatos de la galería de símbolos de profundidad y de destino de representación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
