---
title: Excepciones
description: En este tema se describen las excepciones al usar Direct3D 11 en hardware de nivel inferior.
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cc525aa170d5479b0a35f94f7adf682db8ddf40cb52d63c3cdb2575a0fd4790
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913446"
---
# <a name="exceptions"></a>Excepciones

Algunas características de Direct3D 11 no se especifican completamente por niveles de características. En este tema se describen las excepciones al usar Direct3D 11 en hardware de nivel inferior. Quizás se agregó una característica después de definir el nivel de característica (y requiere un controlador actualizado) o quizás diferentes GPU implementen implementaciones muy diferentes. Las excepciones de nivel de característica se pueden recopilar en los grupos siguientes:

-   [Formatos extendidos](#extended-formats)
-   [Suavizado de alias de múltiples muestras](#multisample-anti-aliasing)
-   [Tamaños de Texture2D](#texture2d-sizes)
-   [Comportamiento especial de los adaptadores para el nivel de característica 9](#special-behavior-of-adapters-for-feature-level-9)
-   [Temas relacionados](#related-topics)

En la sección 10Level9 Reference (Referencia de [10Level9)](d3d11-graphics-reference-10level9.md) se enumeran las diferencias entre el comportamiento de los distintos métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en varios niveles de características de 10Level9.

## <a name="extended-formats"></a>Formatos extendidos

Un formato extendido es un formato de píxel agregado a Direct3D 10.1 y Direct3D 11 para los niveles de características 10 0 y \_ 10 \_ 1. Un formato extendido requiere un controlador actualizado (para Direct3D 10 \_ 1 o inferior). Use [**ID3D11Device::CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) e [**ID3D11Device::CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) para consultar la compatibilidad con estos formatos extendidos.

Un formato extendido:

-   Agrega compatibilidad con el orden BGRA de recursos de 8 bits por componente.
-   Permite la conversión de un búfer de cadena de intercambio de valor entero. Esto permite que una aplicación agregue o quite el sufijo \_ SRGB o se represente en una cadena de intercambio \_ de BIAS de XR.
-   Agrega compatibilidad opcional con DXGI \_ FORMAT \_ R10G10B10 \_ XR \_ BIAS \_ A2 \_ UNORM.
-   Garantiza que se presenta una cadena de intercambio DXGI \_ FORMAT \_ R16G16B16A16 FLOAT como si los datos contenidos no se codificasen \_ en sRGB.

El conjunto completo de formatos extendidos es totalmente compatible o no se admite, a excepción del formato \_ BIAS XR. El formato \_ BIAS XR es:

-   No compatible en cualquier nivel 9
-   Opcional en el nivel 10 \_ 0 o 10 \_ 1
-   Garantizado en el nivel 11 \_ 0

## <a name="multisample-anti-aliasing"></a>Suavizado de alias de múltiples muestras

Las implementaciones de MSAA tienen poco en común entre las implementaciones de GPU. Nivel de característica 10.1 agregó algunos minima bien definidos, pero en niveles de características inferiores, MSAA debe probarse explícitamente mediante [**ID3D11Device::CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels).

## <a name="texture2d-sizes"></a>Tamaños de Texture2D

Un nivel de característica garantiza que se puede crear un tamaño mínimo; sin embargo, una aplicación puede crear texturas más grandes hasta el tamaño completo admitido por la GPU. Una aplicación debe esperar un error de un método como [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) si se supera un máximo.

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>Comportamiento especial de los adaptadores para el nivel de característica 9

Los tres niveles más bajos de características D3D FEATURE LEVEL 9 1, D3D FEATURE LEVEL 9 2 y D3D FEATURE LEVEL 9 3, comparten un archivo DLL de implementación común y tratan el argumento \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) a D3D11CreateDevice \[ AndSwapchain \] como un adaptador de plantilla y crean su propio adaptador como parte de la creación del dispositivo. Esto significa que **el IDXGIAdapter** pasado a la rutina de creación no será el mismo adaptador que el recuperado del dispositivo a través de IDXGIDevice::GetAdapter. El impacto de esto es que los **IDXGIOutputs enumerados** desde el adaptador pasado no se pueden usar para entrar en pantalla completa con ningún dispositivo de nivel 9, ya que esas salidas no son propiedad del adaptador del dispositivo. Es una buena práctica descartar el adaptador de plantilla pasado y recuperar el adaptador creado del dispositivo mediante IDXGIDevice::GetAdapter, donde [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) se puede recuperar mediante QueryInterface desde la interfaz de dispositivo Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 