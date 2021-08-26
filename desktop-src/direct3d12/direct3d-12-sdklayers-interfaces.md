---
title: Interfaces de la capa de depuración
description: Las interfaces siguientes se declaran en d3d12sdklayers.h.
ms.assetid: 9BD5910A-8FF2-4540-BB8E-8EA5C10528CE
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5d7e16d6c593f2dcfcc46266102ac15a61386ef
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812878"
---
# <a name="debug-layer-interfaces"></a>Interfaces de capa de depuración

Las interfaces siguientes se definen en `d3d12sdklayers.h` .

## <a name="in-this-section"></a>En esta sección

| Tema | Descripción |
|-|-|
| [**ID3D12Debug**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug) | Una interfaz de depuración controla la configuración de depuración y valida el estado de la canalización. Solo se puede usar si la capa de depuración está activada. |
| [**ID3D12Debug1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debug1) | Agrega la validación basada en GPU y la sincronización de la cola de comandos dependientes a la capa de depuración. |
| [**ID3D12Debug2**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug2) | Agrega niveles configurables de GPU-Based validación. |
| [**ID3D12Debug3**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug3) | Agrega a la capa de depuración validación basada en GPU, sincronización de cola de comandos dependiente y niveles configurables de validación basada en GPU. |
| [**ID3D12Debug4**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug4) | Agrega la capacidad de deshabilitar la capa de depuración. |
| [**ID3D12Debug5**](/windows/win32/api/D3D12sdklayers/nn-d3d12sdklayers-id3d12debug5) | Agrega a la capa de depuración la capacidad de configurar el nombre automático de los objetos. |
| [**ID3D12DebugCommandList**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist) | Proporciona métodos para supervisar y depurar una lista de comandos. |
| [**ID3D12DebugCommandList1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandlist1) | Esta interfaz permite modificar la configuración adicional de la capa de depuración de la lista de comandos. |
| [**ID3D12DebugCommandQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugcommandqueue) | Proporciona métodos para supervisar y depurar una cola de comandos. |
| [**ID3D12DebugDevice**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice) | Esta interfaz representa un dispositivo gráfico para la depuración. |
| [**ID3D12DebugDevice1**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12debugdevice1) | Especifica la configuración de la capa de depuración en todo el dispositivo. |
| [**ID3D12InfoQueue**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12infoqueue) | Una interfaz de cola de información almacena, recupera y filtra los mensajes de depuración. La cola consta de una cola de mensajes, una pila de filtros de almacenamiento opcional y una pila de filtros de recuperación opcional. |
| [**ID3D12SharingContract**](/windows/win32/api/d3d12sdklayers/nn-d3d12sdklayers-id3d12sharingcontract) | Parte de un contrato entre las capas de diagnóstico D3D11On12 y las herramientas de diagnóstico de gráficos. |

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración del entorno de programación de Direct3D 12](directx-12-programming-environment-set-up.md)
</dt> <dt>

[Referencia de la capa de depuración](direct3d-12-sdklayers-reference.md)
</dt> <dt>

[Referencia de Direct3D 12](direct3d-12-reference.md)
</dt> </dl>