---
title: Artículos sobre gráficos de DirectX
description: .
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ac2a3a6b9beff7dfc8bfe4f6c0de92885f39ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359268"
---
# <a name="directx-graphics-articles"></a>Artículos sobre gráficos de DirectX

## <a name="purpose"></a>Propósito

Esta sección contiene artículos técnicos en los que se describe la compatibilidad recién agregada de WARP y Windows 7 con el modo de volteo presente y sus estadísticas presentes asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio. Esta sección también contiene artículos técnicos sobre las API de gráficos de Windows, la portabilidad de las API de Direct3D 9 a las API de Microsoft DirectX Graphics Infrastructure (DXGI) y cómo implementar Direct3D 11.

Para obtener más información sobre Direct3D, vea [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Audiencia de desarrolladores

Estos artículos técnicos son para los desarrolladores de aplicaciones de gráficos de DirectX.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Actualización de la plataforma para Windows 7](platform-update-for-windows-7.md) | Describe qué componentes de la pila de gráficos de Windows 8 están disponibles y hasta qué punto, a través de la [actualización de la plataforma para Windows 7](https://support.microsoft.com/kb/2670838). |
| [Mejoras de Direct3D 9Ex](direct3d-9ex-improvements.md) | Describe la compatibilidad recién agregada de Windows 7 con el modo de volteo presente y sus estadísticas actuales asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio. Las aplicaciones de destino incluyen aplicaciones de presentación basadas en vídeo o velocidad de fotogramas. Las aplicaciones que usan el modo Flip de Direct3D 9Ex reducen la carga de recursos del sistema cuando DWM está habilitado. Las mejoras presentes en las estadísticas asociadas con el modo de volteo permiten a las aplicaciones de Direct3D 9Ex controlar mejor la velocidad de presentación al proporcionar mecanismos de corrección y comentarios en tiempo real. Se incluyen explicaciones detalladas y punteros a los recursos de ejemplo. |
| [Uso compartido de la superficie entre las API de gráficos de Windows](surface-sharing-between-windows-graphics-apis.md) | Proporciona información general técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, Direct3D 10 y Direct3D 9Ex. Si ya tiene conocimientos prácticos de estas API, este documento puede ayudarle a usar varias API para representarlas en la misma superficie en una aplicación diseñada para los sistemas operativos Windows 7 o Windows Vista. En este tema también se proporcionan instrucciones de prácticas recomendadas y punteros a recursos adicionales. |
| [Guía de ALABEo](directx-warp.md) | Proporciona una guía de Windows Advanced Rasterization Platform (WARP), un rasterizador de software de alta velocidad. |
| [API de gráficos en Windows](graphics-apis-in-windows-vista.md) | Describe las características y las API de gráficos de Windows. |
| [Implementación de Direct3D 11 para desarrolladores de juegos](direct3d11-deployment.md) | Describe cómo implementar los componentes de Direct3D 11 en un sistema. |
| [Infraestructura de gráficos de DirectX (DXGI): procedimientos recomendados](dxgi-best-practices.md) | Describe los problemas relacionados con la migración de API de Direct3D 9 a características y API de DXGI de varias versiones de DXGI. |
| [Uso de DirectX con pantallas de alto rango dinámico y color avanzado](high-dynamic-range.md) | En este tema se proporciona información general técnica sobre la representación de contenido de Direct3D 11 y Direct3D 12 de rango dinámico alto en una pantalla de HDR10 con compatibilidad con el color avanzado de Windows 10. |