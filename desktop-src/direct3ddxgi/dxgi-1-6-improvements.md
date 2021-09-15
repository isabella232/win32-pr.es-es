---
description: En este tema se describen las novedades de Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.6 para varias versiones de Windows 10.
ms.assetid: C68EC437-7600-43A8-8DEA-5A6AEE75D5AA
title: Mejoras de DXGI 1.6
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 03961b4f9af50675ee157c4840b9ed744c54f423
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127574057"
---
# <a name="dxgi-16-improvements"></a>Mejoras de DXGI 1.6

En este tema se describen las novedades de Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.6 para varias versiones de Windows 10.

## <a name="windows-10-october-2018-update"></a>Actualización de octubre de 2018 de Windows 10

Estas API se agregaron para Windows 10, versión 1809 (10.0; Compilación 17763) &mdash; también conocida como Actualización de octubre de 2018 de Windows 10.

- [**Interfaz IDXGIFactory7**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory7) y sus métodos.

## <a name="windows-10-april-2018-update"></a>Actualización de abril de 2018 de Windows 10

Estas API se agregaron para Windows 10 versión 1803 (10.0; Compilación 17134) &mdash; también conocida como Windows 10 actualización de abril de 2018.

- [**DXGI_GPU_PREFERENCE**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_gpu_preference) enumeración.
- [**Interfaz IDXGIFactory6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgifactory6) y sus métodos.

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Por Windows 10, versión 1709 (10.0; Compilación 16299) también conocida como Windows 10 Fall Creators Update estas constantes se han &mdash; &mdash; agregado a la [**enumeración DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) datos. 

- **DXGI_ADAPTER_FLAG3_SUPPORT_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_SUPPORT_NON_MONITORED_FENCES**
- **DXGI_ADAPTER_FLAG3_KEYED_MUTEX_CONFORMANCE**

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Por Windows 10, versión 1703 (10.0; Compilación 15063) también conocida como Windows 10 Creators Update se ha agregado la siguiente funcionalidad &mdash; &mdash; a Microsoft Infraestructura de gráficos de DirectX (DXGI) 1.6 para detectar pantallas HDR.

### <a name="high-dynamic-range-hdr-detection"></a>Detección de intervalo dinámico alto (HDR)

Estas API se han agregado para detectar pantallas HDR.

- [**DXGI_ADAPTER_DESC3**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_adapter_desc3) estructura
- [**DXGI_ADAPTER_FLAG3**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_adapter_flag3) enumeración
- [**DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS**](/windows/win32/api/dxgi1_6/ne-dxgi1_6-dxgi_hardware_composition_support_flags) enumeración
- [**DXGI_OUTPUT_DESC1**](/windows/win32/api/dxgi1_6/ns-dxgi1_6-dxgi_output_desc1) estructura
- [**Función DXGIDeclareAdapterRemovalSupport**](/windows/win32/api/dxgi1_6/nf-dxgi1_6-dxgideclareadapterremovalsupport)
- [**Interfaz IDXGIAdapter4**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgiadapter4) y sus métodos
- [**Interfaz IDXGIOutput6**](/windows/win32/api/dxgi1_6/nn-dxgi1_6-idxgioutput6) y sus métodos

Además, se han agregado constantes a la [**enumeración DXGI_COLOR_SPACE_TYPE**](/windows/win32/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) para admitir estas API.

## <a name="related-topics"></a>Temas relacionados
[Guía de programación para DXGI](dx-graphics-dxgi-overviews.md)
