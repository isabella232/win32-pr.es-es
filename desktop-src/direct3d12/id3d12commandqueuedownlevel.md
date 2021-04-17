---
title: Interfaz ID3D12CommandQueueDownlevel
description: Proporciona un mecanismo presente específico de Windows-7.
keywords:
- Interfaz ID3D12CommandQueueDownlevel
topic_type:
- apiref
api_name:
- ID3D12CommandQueueDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 6f2aee6fd1b0f58469162c640d92aeb187bd9641
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721434"
---
# <a name="id3d12commandqueuedownlevel-interface"></a>Interfaz ID3D12CommandQueueDownlevel

Se puede tener acceso a esta interfaz a través de **QueryInterface** fuera de una [cola de comandos de Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) al usar [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Proporciona un mecanismo presente específico de Windows-7.

### <a name="methods"></a>Métodos

La interfaz **ID3D12CommandQueueDownlevel** tiene estos métodos.

| Método | Descripción |
|:-------|:------------|
| [**Presente**](id3d12commandqueuedownlevel-present.md) | Copia el contenido de un recurso de D3D12 Texture2D en una ventana. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel. h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vea también
* [Direct3D 12 en interfaces de Windows 7](direct3d-12on7-interfaces.md)
* [Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
