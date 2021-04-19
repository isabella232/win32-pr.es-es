---
description: En este tema se describen las novedades de Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 para varias versiones de Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Mejoras en DXGI 1,6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 03961b4f9af50675ee157c4840b9ed744c54f423
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537941"
---
# <a name="dxgi-16-improvements"></a>Mejoras en DXGI 1,6

En este tema se describen las novedades de Microsoft DirectX Graphics Infrastructure (DXGI) 1,6 para varias versiones de Windows 10.

## <a name="windows-10-october-2018-update"></a>Actualización de octubre de 2018 de Windows 10

Estas API se agregaron para Windows 10, versión 1809 (10,0; Compilación 17763) &mdash; también se conoce como actualización de Windows 10 de octubre de 2018.

- Interfaz [**IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) y sus métodos.

## <a name="windows-10-april-2018-update"></a>Actualización de abril de 2018 de Windows 10

Estas API se agregaron para Windows 10, versión 1803 (10,0; Compilación 17134) &mdash; también se conoce como actualización de Windows 10 de abril de 2018.

- Enumeración [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) .
- Interfaz [**IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) y sus métodos.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Para Windows 10, versión 1709 (10,0; Compilación 16299) &mdash; también conocido como Windows 10 Fall Creators Update &mdash; . estas constantes se han agregado a la enumeración [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) . 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update.

Para Windows 10, versión 1703 (10,0; Compilación 15063) &mdash; también conocido como Windows 10 Creators Update, se ha &mdash; agregado la siguiente funcionalidad a la infraestructura de gráficos de Microsoft DirectX (DXGI) 1,6 para detectar pantallas HDR.

### <a name="high-dynamic-range-hdr-detection"></a>Detección de intervalo dinámico alto (HDR)

Estas API se han agregado para detectar pantallas HDR.

- Estructura de [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3)
- Enumeración [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3)
- Enumeración [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags)
- Estructura de [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1)
- [**DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport) función)
- Interfaz [**IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) y sus métodos
- Interfaz [**IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) y sus métodos

Además, se han agregado constantes a la enumeración [**DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) para admitir estas API.

## <a name="related-topics"></a>Temas relacionados
[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
