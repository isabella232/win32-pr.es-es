---
title: Artículos sobre gráficos de DirectX
description: Artículos sobre gráficos de DirectX
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5562b4b7dafc899d1c6a827cfd2e240a20013be7a31f225cdd41893d967748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095505"
---
# <a name="directx-graphics-articles"></a>Artículos sobre gráficos de DirectX

## <a name="purpose"></a>Propósito

Esta sección contiene artículos técnicos que describen la compatibilidad recién agregada de WARP y Windows 7 con el modo de volteo Presente y sus estadísticas presentes asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio. Esta sección también contiene artículos técnicos sobre las API de gráficos de Windows, la porción de las API de Direct3D 9 a las API de Microsoft Infraestructura de gráficos de DirectX (DXGI) y cómo implementar Direct3D 11.

Para obtener más información sobre Direct3D, [vea Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Audiencia de desarrolladores

Estos artículos técnicos son para desarrolladores de aplicaciones de gráficos DirectX.

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [Actualización de plataforma para Windows 7](platform-update-for-windows-7.md) | Describe qué componentes de la pila Windows 8 gráficos están disponibles y en qué medida, a través de la actualización de plataforma [para Windows 7](https://support.microsoft.com/kb/2670838). |
| [Mejoras de Direct3D 9Ex](direct3d-9ex-improvements.md) | Describe Windows compatibilidad recién agregada de 7 con el modo de volteo presente y sus estadísticas presentes asociadas en Direct3D 9Ex y Administrador de ventanas de escritorio. Las aplicaciones de destino incluyen aplicaciones de presentación basadas en vídeo o en fotogramas. Las aplicaciones que usan direct3D 9Ex Flip Mode Present reducen la carga de recursos del sistema cuando DWM está habilitado. Presentar mejoras de estadísticas asociadas con el modo de volteo presente permite que las aplicaciones Direct3D 9Ex controle mejor la tasa de presentación al proporcionar comentarios en tiempo real y mecanismos de corrección. Se incluyen explicaciones detalladas y punteros a recursos de ejemplo. |
| [Uso compartido de la superficie entre las API de gráficos de Windows](surface-sharing-between-windows-graphics-apis.md) | Proporciona información general técnica sobre la interoperabilidad mediante el uso compartido de superficies entre las API de gráficos de Windows, como Direct3D 11, Direct2D, Direct3D 10 y Direct3D 9Ex. Si ya tiene conocimientos prácticos de estas API, este documento puede ayudarle a usar varias API para representarse en la misma superficie en una aplicación diseñada para los sistemas operativos Windows 7 o Windows Vista. En este tema también se proporcionan instrucciones de procedimientos recomendados y punteros a recursos adicionales. |
| [Guía de WARP](directx-warp.md) | Proporciona una guía de Windows Advanced Rasterization Platform (WARP), un rasterizador de software de alta velocidad. |
| [API de gráficos en Windows](graphics-apis-in-windows-vista.md) | Describe Windows y API de gráficos. |
| [Implementación de Direct3D 11 para desarrolladores de juegos](direct3d11-deployment.md) | Describe cómo implementar los componentes de Direct3D 11 en un sistema. |
| [Infraestructura de gráficos de DirectX (DXGI): Procedimientos recomendados](dxgi-best-practices.md) | Describe los problemas relacionados con la porción de las API de Direct3D 9 a las API de DXGI y las características de varias versiones de DXGI. |
| [Uso de DirectX con pantallas de alto rango dinámico y color avanzado](high-dynamic-range.md) | En este tema se proporciona información técnica sobre la representación de contenido de direct3D 11 y Direct3D 12 de alto rango dinámico en una pantalla DE HDR10 Windows 10 compatibilidad avanzada con colores. |
