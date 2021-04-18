---
title: Enumeración D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Marcas pasadas a ID3D12CommandQueueDownlevel::P método reenviado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721438"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>D3D12 \_ \_ enumeración de marcas de presencia de nivel inferior \_

Marcas pasadas a [**ID3D12CommandQueueDownlevel::P función reenviar**](id3d12commandqueuedownlevel-present.md) para modificar el comportamiento.

## <a name="syntax"></a>Sintaxis

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Constantes

**Marca de D3D12 de \_ nivel inferior \_ presente \_ \_ ninguno**

No hay opciones seleccionadas.

**D3D12 \_ \_ \_ marca de presentación \_ de nivel inferior \_ de espera para \_ VBLANK**

La operación **present** no se realizará hasta que se haya producido una sincronización de errores desde la última vez que **presente** el Ed.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel. h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Vea también
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Enumeraciones de Direct3D 12 en Windows 7](direct3d-12on7-enumerations.md)
* [Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
