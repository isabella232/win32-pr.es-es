---
title: D3D12_DOWNLEVEL_PRESENT_FLAGS enumeración
description: Marcas que se pasan al método ID3D12CommandQueueDownlevel::P resent.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570889"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a>Enumeración D3D12 \_ DOWNLEVEL \_ PRESENT \_ FLAGS

Marcas que se pasan a [**la función ID3D12CommandQueueDownlevel::P resent**](id3d12commandqueuedownlevel-present.md) para modificar el comportamiento.

## <a name="syntax"></a>Sintaxis

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a>Constantes

**D3D12 \_ DOWNLEVEL \_ PRESENT \_ FLAG \_ NONE**

No hay opciones seleccionadas.

**D3D12 \_ DOWNLEVEL \_ PRESENT \_ FLAG \_ WAIT \_ FOR \_ VBLANK**

La **operación** Present no se hará hasta que se haya producido una VSync desde la última vez que **hizo** la presentación.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|--------|------------------|
| Encabezado | d3d12downlevel.h |
| Archivo DLL    | D3D12.dll (solo Windows 7) |

## <a name="see-also"></a>Consulte también
* [ID3D12CommandQueueDownlevel](id3d12commandqueuedownlevel.md)
* [Enumeraciones de Direct3D 12 en Windows 7](direct3d-12on7-enumerations.md)
* [Direct3D 12 en Windows 7 (d3d12downlevel.h)](direct3d-12on7-reference.md)
* [Direct3D 12 en Windows 7](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
