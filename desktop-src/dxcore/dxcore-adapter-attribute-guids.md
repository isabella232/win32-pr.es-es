---
title: GUID de atributos de adaptador de DXCore
description: Los siguientes GUID de atributo de adaptador se declaran en y se usan con los métodos `dxcore_interface.h` [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter::IsAttributeSupported.](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
keywords:
- DXCore, atributo de adaptador, GUID
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
ms.openlocfilehash: 44b6be239286e13cecbf6eb501b333cba5541f6de1dfd8e217166d9620bdfbd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118279665"
---
# <a name="dxcore-adapter-attribute-guids"></a>GUID de atributos de adaptador de DXCore

Los siguientes GUID de atributo de adaptador se declaran en y se usan con los métodos `dxcore_interface.h` [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md) e [IDXCoreAdapter::IsAttributeSupported.](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md) Para cualquier adaptador determinado, se podrían aplicar uno o varios de los atributos.

| GUID | Valor |
|-|-|
| `DXCORE_ADAPTER_ATTRIBUTE_D3D11_GRAPHICS`. Especifica un adaptador que admite el uso con las API [de gráficos de Direct3D 11.](/windows/win32/direct3d11) No se realiza ninguna garantía sobre características específicas ni se garantiza que el sistema operativo de su configuración actual admita estas API. | 0x8c47866b, 0x7583, 0x450d, 0xf0, 0xf0, 0x6b, 0xad, 0xa8, 0x95, 0xaf, 0x4b |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS`. Especifica un adaptador que admite el uso con las [API de gráficos de Direct3D 12.](/windows/win32/direct3d12) No se realiza ninguna garantía sobre características específicas ni se garantiza que el sistema operativo de su configuración actual admita estas API. | 0x0c9ece4d, 0x2f6e, 0x4f01, 0x8c, 0x96, 0xe8, 0x9e, 0x33, 0x1b, 0x47, 0xb1 |
| `DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE`. Especifica un adaptador que admite el uso con las API de proceso de [Direct3D 12 Core.](../direct3d12/core-feature-levels.md) No se realiza ninguna garantía sobre características específicas ni se garantiza que el sistema operativo de su configuración actual admita estas API. | 0x248e2800, 0xa793, 0x4724, 0xab, 0xaa, 0x23, 0xa6, 0xde, 0x1b, 0xe0, 0x90 |

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-|-|
| Encabezado | dxcore_interface.h |

## <a name="see-also"></a>Consulte también

* [IDXCoreAdapterFactory::CreateAdapterList](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-createadapterlist.md)
* [IDXCoreAdapter::IsAttributeSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isattributesupported.md)
* [Referencia de DXCore](./dxcore-reference.md)
* [Uso de DXCore para enumerar adaptadores](./dxcore-enum-adapters.md)
* [Gráficos de Direct3D 12](../direct3d12/direct3d-12-graphics.md)
