---
title: Limitaciones al crear dewarp y dispositivos de referencia
description: Existen algunas limitaciones para crear dispositivos de hipervelocidad y de referencia en Direct3D 10,1 y Direct3D 11,0. En este tema se describen estas limitaciones.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358994"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitaciones al crear dewarp y dispositivos de referencia

Existen algunas limitaciones para crear dispositivos de hipervelocidad y de referencia en Direct3D 10,1 y Direct3D 11,0. En este tema se describen estas limitaciones.

Los tipos de controlador D3D10 \_ \_ Type \_ Warp y D3D10 de \_ referencia de tipo controlador \_ \_ no se admiten en los niveles de características \_ de D3D10 de nivel \_ \_ 9 \_ 1 a D3D10 \_ \_ \_ de nivel de característica 9 \_ 3 en Direct3D 10,1. Además, el \_ tipo de \_ controlador D3D Type \_ Warp no se admite en el \_ nivel de característica de D3d \_ \_ 11 \_ 0 en Direct3D 11,0. Es decir, cuando se llama a [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear un dispositivo Direct3D 10,1 o cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11,0, si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características en la llamada, la llamada no es válida. Solo las siguientes combinaciones de niveles de características, tiempos de ejecución y tipos de controlador son válidas para los dispositivos WARP y Reference:

-   \_Tipo de controlador D3D \_ \_ Warp en todos los niveles de características de Direct3D 11,1, que incluye Windows 8

    \_Referencia de \_ tipo de controlador D3D \_ en todos los niveles de características de Direct3D 11,1

    Cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11,1, la llamada es válida si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características.

-   \_ \_ Tipo de controlador D3D \_ Warp en el nivel de característica de D3D \_ \_ \_ 9 \_ 1 a \_ \_ \_ \_ los niveles de características de nivel de característica 10 1 de D3D en Direct3D 11

    \_ \_ \_ Referencia de tipo de controlador D3D en el nivel de característica de D3D de nivel \_ \_ \_ 9 \_ 1 a \_ \_ \_ \_ los niveles de características 11 0 de nivel de característica D3D en Direct3D 11

    Cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11, la llamada es válida si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características.

-   \_ \_ Tipo de controlador D3D10 \_ Warp y \_ \_ referencia de tipo de controlador D3D10 en el \_ nivel de características D3D10 de \_ \_ \_ 10 \_ 0 a D3D10 \_ \_ \_ de nivel de característica 10 \_ 1 en Direct3D 10,1

    Cuando se llama a [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear un dispositivo Direct3D 10,1, la llamada es válida si se especifica una combinación de uno de estos tipos de controlador con uno de estos niveles de características.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Introducción a Direct3D 11 en el hardware de nivel inferior](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Cómo: crear un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Cómo: crear un dispositivo de referencia](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**\_Tipo de controlador D3D10 \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 \_ característica \_ Level1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**\_Tipo de controlador D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**\_Nivel de característica D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 