---
title: Introducción a multithreading en Direct3D 11
description: El multithreading está diseñado para mejorar el rendimiento mediante la realización de trabajos mediante uno o varios subprocesos al mismo tiempo.
ms.assetid: b4bef1e4-8d34-455c-8aed-01af974c66c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527b78d8b29a507247c8eb067c20739004ace687
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104358995"
---
# <a name="introduction-to-multithreading-in-direct3d-11"></a>Introducción a multithreading en Direct3D 11

El multithreading está diseñado para mejorar el rendimiento mediante la realización de trabajos mediante uno o varios subprocesos al mismo tiempo.

En el pasado, a menudo esto se ha hecho generando un único subproceso principal para la representación y uno o más subprocesos para realizar el trabajo de preparación, como la creación de objetos, la carga, el procesamiento, etc. Sin embargo, con la sincronización integrada en Direct3D 11, el objetivo detrás de multithreading es utilizar cada ciclo de CPU y GPU sin hacer que un procesador espere a otro procesador (en particular, no hacer que la GPU espere porque afecta directamente a la velocidad de fotogramas). Al hacerlo, puede generar la mayor cantidad de trabajo manteniendo la mejor velocidad de fotogramas. El concepto de un solo fotograma para la representación ya no es necesario, ya que la API implementa la sincronización.

Multithreading requiere algún tipo de sincronización. Por ejemplo, si varios subprocesos que se ejecutan en una aplicación deben tener acceso a un contexto de dispositivo único ([**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)), la aplicación debe usar algún mecanismo de sincronización, como las secciones críticas, para sincronizar el acceso a ese contexto de dispositivo. Esto se debe a que el procesamiento de los comandos de representación (que normalmente se realizan en la GPU) y la generación de los comandos de representación (normalmente se realiza en la CPU a través de la creación de objetos, la carga de datos, el cambio de estado, el procesamiento de datos) suelen usar los mismos recursos (texturas, sombreadores, estado de canalización, etc.) La organización del trabajo entre varios subprocesos requiere sincronización para impedir que un subproceso modifique o lea datos que otro subproceso está modificando.

Aunque el uso de un contexto de dispositivo ([**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)) no es seguro para subprocesos, el uso de un dispositivo Direct3D 11 ([**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)) es seguro para subprocesos. Dado que cada **ID3D11DeviceContext** es de un solo subproceso, solo un subproceso puede llamar a **ID3D11DeviceContext** a la vez. Si varios subprocesos deben tener acceso a un único **ID3D11DeviceContext**, deben usar algún mecanismo de sincronización, como las secciones críticas, para sincronizar el acceso a ese **ID3D11DeviceContext**. Sin embargo, no es necesario que varios subprocesos usen secciones críticas o primitivas de sincronización para tener acceso a un único **ID3D11Device**. Por lo tanto, si una aplicación usa **ID3D11Device** para crear objetos de recursos, no es necesario que la aplicación use la sincronización para crear varios objetos de recursos al mismo tiempo.

La compatibilidad con multithreading divide la API en dos áreas funcionales distintas:

-   [Creación de objetos con multithreading](overviews-direct3d-11-render-multi-thread-create.md)
-   [Representación inmediata y diferida](overviews-direct3d-11-render-multi-thread-render.md)

El rendimiento del multithreading depende de la compatibilidad del controlador. [Cómo: comprobar la compatibilidad con controladores](overviews-direct3d-11-render-multi-thread-support.md) proporciona más información sobre cómo consultar el controlador y qué significan los resultados.

Direct3D 11 se ha diseñado desde el principio para admitir el multithreading. Direct3D 10 implementa compatibilidad limitada para el multithreading mediante el [nivel seguro para subprocesos](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers). En esta página se enumeran las diferencias de comportamiento entre las dos versiones de DirectX: [diferencias de subprocesos entre versiones de Direct3D](overviews-direct3d-11-render-multi-thread-differences.md).

## <a name="multithreading-and-dxgi"></a>Multithreading y DXGI

Solo un subproceso a la vez debe utilizar el contexto inmediato. Sin embargo, la aplicación también debe usar ese mismo subproceso para las operaciones de infraestructura de gráficos de Microsoft DirectX (DXGI), especialmente cuando la aplicación realiza llamadas a [**IDXGISwapChain::P método reenviado**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) .

> [!Note]  
> No es válido utilizar un contexto inmediato simultáneamente con la mayoría de las funciones de la interfaz de DXGI. En el caso de los SDK de DirectX de marzo de 2009 y versiones posteriores, las únicas funciones de DXGI que son seguras son [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref), [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)y [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

 

Para obtener más información sobre el uso de DXGI con varios subprocesos, consulte [consideraciones de multiproceso](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Multithreading](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 