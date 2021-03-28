---
title: Introducción a un dispositivo en Direct3D 11
description: El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o más contextos. Esta separación está diseñada para facilitar el multithreading.
ms.assetid: b9b45d18-f7b7-40f9-ae4e-576ca7a6eba7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b03333c6594f17d85fee28880e46928241e06c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104983686"
---
# <a name="introduction-to-a-device-in-direct3d-11"></a>Introducción a un dispositivo en Direct3D 11

El modelo de objetos de Direct3D 11 separa la funcionalidad de creación y representación de recursos en un dispositivo y uno o más contextos. Esta separación está diseñada para facilitar el multithreading.

-   [Dispositivo](#introduction-to-a-device-in-direct3d-11)
-   [Contexto de dispositivo](#device-context)
    -   [Contexto inmediato](#immediate-context)
    -   [Contexto diferido](#deferred-context)
-   [Consideraciones sobre los subprocesos](#threading-considerations)
-   [Temas relacionados](#related-topics)

## <a name="device"></a>Dispositivo

Un dispositivo se usa para crear recursos y para enumerar las capacidades de un adaptador de pantalla. En Direct3D 11, un dispositivo se representa con una interfaz [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

Cada aplicación debe tener al menos un dispositivo, mientras que la mayoría de las aplicaciones solo crea un dispositivo. Cree un dispositivo para uno de los controladores de hardware instalados en el equipo mediante una llamada a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) y especifique el tipo de controlador con la marca de [**\_ \_ tipo de controlador D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) . Cada dispositivo puede usar uno o más contextos de dispositivo, en función de la funcionalidad deseada.

## <a name="device-context"></a>Contexto de dispositivo

Un contexto de dispositivo contiene la circunstancia o la configuración en la que se usa un dispositivo. Más concretamente, se usa un contexto de dispositivo para establecer el estado de la canalización y generar comandos de representación mediante los recursos que pertenecen a un dispositivo. Direct3D 11 implementa dos tipos de contextos de dispositivo, uno para la representación inmediata y otro para la representación diferida; ambos contextos se representan con una interfaz [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

### <a name="immediate-context"></a>Contexto inmediato

Un contexto inmediato se representa directamente en el controlador. Cada dispositivo tiene uno y solo un contexto inmediato que puede recuperar datos de la GPU. Un contexto inmediato se puede usar para representar (o reproducir) inmediatamente una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md).

Hay dos maneras de obtener un contexto inmediato:

-   Llamando a [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) o [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).
-   Llamando a [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).

### <a name="deferred-context"></a>Contexto diferido

Un contexto diferido registra los comandos de GPU en una [lista de comandos](overviews-direct3d-11-render-multi-thread-command-list.md). Un contexto diferido se utiliza principalmente para el multithreading y no es necesario para una aplicación de un solo subproceso. Un subproceso de trabajo suele usar un contexto diferido en lugar del subproceso principal de representación. Cuando se crea un contexto diferido, no hereda ningún estado del contexto inmediato.

Para obtener un contexto diferido, llame a [**ID3D11Device:: CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).

Cualquier contexto: inmediato o aplazado se puede usar en cualquier subproceso, siempre que el contexto solo se use en un subproceso cada vez.

## <a name="threading-considerations"></a>Consideraciones sobre los subprocesos

En esta tabla se resaltan las diferencias en el modelo de subprocesos de Direct3D 11 de versiones anteriores de Direct3D.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferencias entre Direct3D 11 y versiones anteriores de Direct3D:<br/> Todos los métodos de interfaz <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> son de subprocesos libres, lo que significa que es seguro tener varios subprocesos que llaman a las funciones al mismo tiempo.<br/>
<ul>
<li>Todas las interfaces derivadas de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>(<a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer"><strong>ID3D11Buffer</strong></a>, <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11query"><strong>ID3D11Query</strong></a>, etc.) son de subprocesamiento libre.</li>
<li>Direct3D 11 divide la creación y representación de recursos en dos interfaces. Map, unmapping, Begin, end y GetData se implementan en <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> porque <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11device"><strong>ID3D11Device</strong></a> define fuertemente el orden de las operaciones. Las interfaces <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11resource"><strong>ID3D11Resource</strong></a> y <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous"><strong>ID3D11Asynchronous</strong></a> también implementan métodos para operaciones de subprocesamiento libre.</li>
<li>Los métodos de <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext"><strong>ID3D11DeviceContext</strong></a> (excepto los que existen en <a href="/windows/desktop/api/D3D11/nn-d3d11-id3d11devicechild"><strong>ID3D11DeviceChild</strong></a>) no son de subprocesos libres, es decir, requieren un único subproceso. Solo un subproceso puede llamar a cualquiera de sus métodos (dibujar, copiar, asignar, etc.) de forma segura a la vez.</li>
<li>En general, el subprocesamiento libre minimiza el número de primitivas de sincronización utilizadas y su duración. Sin embargo, una aplicación que usa la sincronización durante mucho tiempo puede afectar directamente a la cantidad de simultaneidad que una aplicación puede esperar alcanzar.</li>
</ul>
Los métodos de interfaz ID3D10Device no están diseñados para ser de subprocesamiento libre. ID3D10Device implementa toda la funcionalidad de creación y representación (como hace ID3D9Device en Direct3D 9). Map y unmapping se implementan en las interfaces derivadas de ID3D10Resource, Begin, end y GetData se implementan en las interfaces derivadas de ID3D10Asynchronous.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> </dl>

 

 





