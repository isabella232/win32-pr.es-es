---
title: Limitaciones al crear dispositivos DE REFERENCIA y WARP
description: Existen algunas limitaciones para crear dispositivos WARP y Reference en Direct3D 10.1 y Direct3D 11.0. En este tema se de abordan esas limitaciones.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566681"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitaciones al crear dispositivos DE REFERENCIA y WARP

Existen algunas limitaciones para crear dispositivos WARP y Reference en Direct3D 10.1 y Direct3D 11.0. En este tema se de abordan esas limitaciones.

Los tipos de controladores D3D10 DRIVER TYPE WARP y D3D10 DRIVER TYPE REFERENCE no se admiten en los niveles de características \_ \_ \_ \_ \_ \_ D3D10 \_ FEATURE \_ LEVEL 9 1 a \_ \_ D3D10 \_ FEATURE LEVEL \_ \_ 9 3 en \_ Direct3D 10.1. Además, el tipo de controlador WARP D3D DRIVER TYPE no se admite en \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ 11 \_ 0 en Direct3D 11.0. Es decir, cuando se llama a [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear un dispositivo Direct3D 10.1 o cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11.0, si se especifica una combinación de uno de estos tipos de controladores con uno de estos niveles de características en la llamada, la llamada no es válida. Solo las siguientes combinaciones de niveles de características, tiempos de ejecución y tipos de controlador son válidas para dispositivos WARP y Reference:

-   D3D DRIVER TYPE WARP en todos los niveles de características de \_ \_ \_ Direct3D 11.1, que Windows 8 incluye

    REFERENCIA DEL TIPO \_ DE CONTROLADOR D3D en todos los niveles de características de \_ \_ Direct3D 11.1

    Cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11.1, la llamada es válida si se especifica una combinación de uno de estos tipos de controladores con uno de estos niveles de características.

-   FACTORÍA DE TIPO CONTROLADOR \_ \_ D3D en \_ D3D \_ FEATURE LEVEL \_ \_ 9 \_ 1 a D3D FEATURE LEVEL 10 1 niveles de \_ características en \_ \_ \_ Direct3D 11

    REFERENCIA DEL TIPO DE CONTROLADOR \_ \_ D3D en \_ D3D \_ FEATURE LEVEL \_ \_ 9 \_ 1 a D3D \_ FEATURE LEVEL \_ \_ 11 0 feature levels in \_ Direct3D 11

    Cuando se llama a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para crear un dispositivo Direct3D 11, la llamada es válida si se especifica una combinación de uno de estos tipos de controladores con uno de estos niveles de características.

-   REFERENCIA DEL TIPO DE CONTROLADOR \_ \_ \_ D3D10 WARP y D3D10 \_ DRIVER TYPE EN \_ \_ D3D10 \_ FEATURE LEVEL \_ \_ \_ 10 0 a D3D10 \_ FEATURE LEVEL \_ \_ 10 1 feature levels \_ in Direct3D 10.1

    Cuando se llama a [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para crear un dispositivo Direct3D 10.1, la llamada es válida si especifica una combinación de uno de estos tipos de controladores con uno de estos niveles de características.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Introducción a Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Cómo: Crear un dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Cómo: Crear un dispositivo de referencia](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**TIPO DE CONTROLADOR D3D10 \_ \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 \_ FEATURE \_ LEVEL1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**TIPO DE CONTROLADOR D3D \_ \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**NIVEL DE CARACTERÍSTICA D3D \_ \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 