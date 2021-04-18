---
title: Interfaces de la capa de depuración
description: Las siguientes interfaces se declaran en d3d12sdklayers. h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e37dbe2e3348a500a8898d1e1076d2fafde66768
ms.sourcegitcommit: 0aa1dd7577961438a1b3172f3a92fb11cbf359f1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2020
ms.locfileid: "105651344"
---
# <a name="debug-layer-interfaces"></a>Depurar interfaces de capa

Las siguientes interfaces se definen en `d3d12sdklayers.h` .

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**ID3D12Debug**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Una interfaz de depuración controla la configuración de depuración y valida el estado de la canalización. Solo se puede usar si la capa de depuración está activada. |
| [**ID3D12Debug1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Agrega la validación basada en GPU y la sincronización de colas de comandos dependientes a la capa de depuración. |
| [**ID3D12Debug2**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Agrega niveles configurables de la validación de GPU-Based. |
| [**ID3D12Debug3**](/windows/desktop/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Agrega a la validación basada en GPU de la capa de depuración, la sincronización de la cola de comandos dependiente y los niveles configurables de la validación basada en GPU. |
| [**ID3D12DebugCommandList**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Proporciona métodos para supervisar y depurar una lista de comandos. |
| [**ID3D12DebugCommandList1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Esta interfaz permite modificar la configuración de la capa de depuración de la lista de comandos adicional. |
| [**ID3D12DebugCommandQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Proporciona métodos para supervisar y depurar una cola de comandos. |
| [**ID3D12DebugDevice**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Esta interfaz representa un dispositivo de gráficos para la depuración. |
| [**ID3D12DebugDevice1**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Especifica la configuración del nivel de depuración para todo el dispositivo. |
| [**ID3D12InfoQueue**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Una interfaz de cola de información almacena, recupera y filtra los mensajes de depuración. La cola está formada por una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional. |
| [**ID3D12SharingContract**](/windows/desktop/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Parte de un contrato entre las capas de diagnóstico de D3D11On12 y las herramientas de diagnóstico de gráficos. |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno de programación de Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referencia de la capa de depuración](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>