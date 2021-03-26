---
title: Excepciones
description: En este tema se describen las excepciones cuando se usa Direct3D 11 en hardware de nivel inferior.
ms.assetid: b3f85036-8572-40ee-b522-3b677443b840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97920ae42347cf618b22df82abc3b6e06bd5200d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359353"
---
# <a name="exceptions"></a>Excepciones

Algunas características de Direct3D 11 no se especifican por completo en los niveles de características. En este tema se describen las excepciones cuando se usa Direct3D 11 en hardware de nivel inferior. Es posible que se agregara una característica después de definir el nivel de característica (y requiere un controlador actualizado) o que distintas GPU implementen implementaciones muy distintas. Las excepciones de nivel de característica se pueden recopilar en los grupos siguientes:

-   [Formatos extendidos](#extended-formats)
-   [Suavizado de contorno de muestreo múltiple](#multisample-anti-aliasing)
-   [Tamaños de Texture2D](#texture2d-sizes)
-   [Comportamiento especial de los adaptadores para el nivel de características 9](#special-behavior-of-adapters-for-feature-level-9)
-   [Temas relacionados](#related-topics)

En la sección de [referencia de 10Level9 se](d3d11-graphics-reference-10level9.md) enumeran las diferencias entre el comportamiento de varios métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) y [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) en distintos niveles de características de 10Level9.

## <a name="extended-formats"></a>Formatos extendidos

Un formato extendido es un formato de píxel agregado a Direct3D 10,1 y Direct3D 11 para los niveles de característica 10 \_ 0 y 10 \_ 1. Un formato extendido requiere un controlador actualizado (para Direct3D 10 \_ 1 o inferior). Use [**ID3D11Device:: CheckFormatSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkformatsupport) y [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) para consultar la compatibilidad con estos formatos extendidos.

Un formato extendido:

-   Agrega compatibilidad para el orden BGRA de los recursos por componente de 8 bits.
-   Permite la conversión de un búfer de cadena de intercambio de valor entero. Esto permite que una aplicación agregue o quite el \_ sufijo sRGB o se represente en una cadena de intercambio de sesgo de XR \_ .
-   Agrega compatibilidad opcional para el \_ formato de DXGI \_ R10G10B10 \_ XR de \_ polarización \_ a2 \_ UNORM.
-   Garantiza que una \_ \_ \_ cadena de intercambio Float de formato DXGI R16G16B16A16 se presenta como si los datos contenidos no estuvieran codificados en sRGB.

El conjunto completo de formatos extendidos es totalmente compatible o no compatible, con la excepción del formato de \_ sesgo de XR. El formato de sesgo de XR \_ es:

-   No compatible en ningún nivel de 9
-   Opcional en el nivel 10 \_ 0 o 10 \_ 1
-   Garantizado en el \_ nivel 11 0

## <a name="multisample-anti-aliasing"></a>Suavizado de contorno de muestreo múltiple

Las implementaciones de MSAA tienen poco en común entre las implementaciones de GPU. El nivel de característica 10,1 agregó algunos mínimos definidos, pero en niveles de características inferiores, MSAA debe probarse explícitamente mediante [**ID3D11Device:: CheckMultisampleQualityLevels**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkmultisamplequalitylevels).

## <a name="texture2d-sizes"></a>Tamaños de Texture2D

Sin embargo, un nivel de característica garantiza que se puede crear un tamaño mínimo; no obstante, una aplicación puede crear texturas más grandes hasta el tamaño máximo admitido por la GPU. Una aplicación debe esperar un error de un método como [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) si se supera un máximo.

## <a name="special-behavior-of-adapters-for-feature-level-9"></a>Comportamiento especial de los adaptadores para el nivel de características 9

Los tres niveles de características más bajos nivel de características de D3D, nivel de característica 9 \_ \_ \_ \_ 1, nivel de características \_ \_ de D3D \_ 9 \_ 2 y \_ nivel de característica de D3D \_ \_ 9 \_ 3, comparten un archivo dll de implementación común y tratan el argumento [**IDXGIAdapter**](/windows/desktop/api/dxgi/nn-dxgi-idxgiadapter) en D3D11CreateDevice \[ AndSwapchain \] como adaptador de plantilla y crean su propio adaptador como parte de la creación del dispositivo. Esto significa que el **IDXGIAdapter** que se pasa a la rutina de creación no será el mismo adaptador que el que se recuperó del dispositivo a través de IDXGIDevice:: GetAdapter. El impacto de esto es que los **IDXGIOutputs** enumerados desde el adaptador pasado no se pueden usar para entrar en pantalla completa con cualquier dispositivo de nivel 9, ya que esas salidas no son propiedad del adaptador del dispositivo. Es recomendable descartar el adaptador de plantilla que se ha pasado y recuperar el adaptador creado por el dispositivo mediante IDXGIDevice:: GetAdapter, donde se puede recuperar [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) mediante QueryInterface desde la interfaz de dispositivo Direct3D.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Direct3D 11 en hardware de nivel inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> </dl>

 

 