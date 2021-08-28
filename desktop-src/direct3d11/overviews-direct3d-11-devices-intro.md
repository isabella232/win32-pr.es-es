---
title: Introducción a un dispositivo en Direct3D 11
description: El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o varios contextos. esta separación está diseñada para facilitar el multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f9459574ad7d8732714ac54519294ae232e4d8d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475711"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Introducción a un dispositivo en Direct3D 11

El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o varios contextos. esta separación está diseñada para facilitar el multithreading.

-   [Dispositivo](#introduction-to-a-device-in-direct3d-11)
-   [Contexto del dispositivo](#device-context)
    -   [Contexto inmediato](#immediate-context)
    -   [Contexto diferido](#deferred-context)
-   [Consideraciones sobre los subprocesos](#threading-considerations)
-   [Temas relacionados](#related-topics)

## <a name="device"></a>Dispositivo

Un dispositivo se usa para crear recursos y enumerar las funcionalidades de un adaptador de pantalla. En Direct3D 11, un dispositivo se representa con una [**interfaz ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

Cada aplicación debe tener al menos un dispositivo, la mayoría de las aplicaciones solo crean un dispositivo. Cree un dispositivo para uno de los controladores de hardware instalados en el equipo mediante una llamada a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y especifique el tipo de controlador con la marca [**D3D \_ DRIVER \_ TYPE.**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) Cada dispositivo puede usar uno o varios contextos de dispositivo, en función de la funcionalidad deseada.

## <a name="device-context"></a>Contexto del dispositivo

Un contexto de dispositivo contiene la circunstancia o la configuración en la que se usa un dispositivo. Más concretamente, se usa un contexto de dispositivo para establecer el estado de canalización y generar comandos de representación mediante los recursos propiedad de un dispositivo. Direct3D 11 implementa dos tipos de contextos de dispositivo, uno para la representación inmediata y el otro para la representación diferida; ambos contextos se representan con una [**interfaz ID3D11DeviceContext.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

### <a name="immediate-context"></a>Contexto inmediato

Un contexto inmediato se representa directamente en el controlador. Cada dispositivo tiene un único contexto inmediato que puede recuperar datos de la GPU. Se puede usar un contexto inmediato para representar inmediatamente (o reproducir) una lista [de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).

Hay dos maneras de obtener un contexto inmediato:

-   Mediante una llamada [**a D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Mediante una [**llamada a ID3D11Device::GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Contexto diferido

Un contexto diferido registra los comandos de GPU en una [lista de comandos.](overviews-direct3d-11-render-multi-thread-command-list.md) Un contexto diferido se usa principalmente para multithreading y no es necesario para una aplicación de un solo subproceso. Un subproceso de trabajo suele usar un contexto diferido en lugar del subproceso de representación principal. Cuando se crea un contexto diferido, no hereda ningún estado del contexto inmediato.

Para obtener un contexto diferido, llame a [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Cualquier contexto (inmediato o diferido) se puede usar en cualquier subproceso, siempre y cuando el contexto solo se utilice en un subproceso a la vez.

## <a name="threading-considerations"></a>Consideraciones sobre los subprocesos

En esta tabla se resaltan las diferencias en el modelo de subprocesos de Direct3D 11 con respecto a las versiones anteriores de Direct3D.




| | | Diferencias entre Direct3D 11 y versiones anteriores de Direct3D:<br /> Todos los métodos de interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> son de subproceso libre, lo que significa que es seguro que varios subprocesos llamen a las funciones al mismo tiempo.<br /><ul><li>Todas las interfaces derivadas de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a><a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>(ID3D11Buffer,</strong></a> <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query,</strong></a>etc.) son de subproceso libre.</li><li>Direct3D 11 divide la creación y representación de recursos en dos interfaces. Map, Unmap, Begin, End y GetData se implementan en <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> porque <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> define fuertemente el orden de las operaciones. Las interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> e <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> también implementan métodos para operaciones sin subprocesos.</li><li>Los <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>métodos ID3D11DeviceContext</strong></a> (excepto los que existen en <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild)</strong></a>no son de subproceso libre, es decir, requieren un único subproceso. Solo un subproceso puede llamar de forma segura a cualquiera de sus métodos (Draw, Copy, Map, etc.) a la vez.</li><li>En general, el subprocesamiento libre minimiza el número de primitivas de sincronización usadas, así como su duración. Sin embargo, una aplicación que usa la sincronización que se mantiene durante mucho tiempo puede afectar directamente a la simultaneidad que una aplicación puede esperar lograr.</li></ul>Los métodos de interfaz ID3D10Device no están diseñados para ser de subproceso libre. ID3D10Device implementa todas las funciones de creación y representación (al igual que ID3D9Device en Direct3D 9). Map y Unmap se implementan en interfaces derivadas de ID3D10Resource, Begin, End y GetData que se implementan en interfaces derivadas de ID3D10Asynchronous.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





