---
title: Interfaz ID3D12DeviceDownlevel
description: Proporciona una consulta de estadísticas de memoria específica de Windows-7.
keywords:
- Interfaz ID3D12DeviceDownlevel
topic_type:
- apiref
api_name:
- ID3D12DeviceDownlevel
api_location:
- D3D12.dll
api_type:
- COM
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
ms.openlocfilehash: 401cbd0045211ef51e3ef6b06042262964ae2ec5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721433"
---
# <a name="id3d12devicedownlevel-interface"></a>Interfaz ID3D12DeviceDownlevel

Se puede tener acceso a esta interfaz a través de **QueryInterface** fuera de un [dispositivo de Direct3D 12](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) cuando se usa [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/). Proporciona una consulta de estadísticas de memoria específica de Windows-7.

### <a name="methods"></a>Métodos

La interfaz **ID3D12DeviceDownlevel** tiene estos métodos.

| Método | Descripción |
|:-------|:------------|
| [**QueryVideoMemoryInfo**](id3d12devicedownlevel-queryvideomemoryinfo.md) | Proporciona estadísticas de memoria en Windows 7. |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel. h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vea también
* [Direct3D 12 en interfaces de Windows 7](direct3d-12on7-interfaces.md)
* [Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
