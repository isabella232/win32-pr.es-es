---
title: GUID de atributos de adaptador de DXCore
description: 'Los siguientes GUID de atributo de adaptador se declaran en `dxcore_interface.h` , y se usan con los métodos [IDXCoreAdapterFactory:: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) y [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) .'
keywords:
- DXCore, atributo Adapter, GUID
topic_type:
- apiref
api_name:
- DXCore adapter attribute GUIDs
api_location:
- dxcore_interface.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: a532552f144dfc21aa5d6a368aecd915d30b40c8
ms.sourcegitcommit: 8737f32d64e5f01c1d38aab92736e4088d6c446e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/31/2021
ms.locfileid: "106098492"
---
# <a name="dxcore-adapter-attribute-guids"></a>GUID de atributos de adaptador de DXCore

Los siguientes GUID de atributo de adaptador se declaran en `dxcore_interface.h` , y se usan con los métodos [IDXCoreAdapterFactory:: CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) y [IDXCoreAdapter:: IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) . Para cualquier adaptador dado, es posible que se apliquen uno o varios de los atributos.

| GUID | Valor |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Especifica un adaptador que admite su uso con las API de gráficos de [Direct3D 11](/windows/win32/direct3d11) . No se garantizan las características específicas, ni tampoco se garantiza que el sistema operativo de su configuración actual admita estas API. | 0x8c47866b, 0x7583, 0x450d, 0xF0, 0xF0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4B |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Especifica un adaptador que admite su uso con las API de gráficos de [Direct3D 12](/windows/win32/direct3d12) . No se garantizan las características específicas, ni tampoco se garantiza que el sistema operativo de su configuración actual admita estas API. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9E, 0x33, 0x1b, 0x47, 0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Especifica un adaptador que admite su uso con las API de proceso de [Direct3D 12 Core](../direct3d12/core-feature-levels.md) . No se garantizan las características específicas, ni tampoco se garantiza que el sistema operativo de su configuración actual admita estas API. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xAA, 0x23, 0xa6, 0xde, 0x1b, 0xE0, 0x90 |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | dxcore_interface. h |

## <a name="see-also"></a>Consulte también

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Referencia de DXCore](./dxcore-reference.md)
* [Uso de DXCore para enumerar adaptadores](./dxcore-enum-adapters.md)
* [Gráficos de Direct3D 12](../direct3d12/direct3d-12-graphics.md)
