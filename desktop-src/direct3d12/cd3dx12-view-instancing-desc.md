---
title: CD3DX12_VIEW_INSTANCING_DESC estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_view_instancing_desc) estructura.
keywords:
- CD3DX12_VIEW_INSTANCING_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_VIEW_INSTANCING_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2021
ms.openlocfilehash: 51c9f5caf5bedf9712001420993393a2dcfa6870
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969819"
---
# <a name="cd3dx12_view_instancing_desc-structure"></a>CD3DX12_VIEW_INSTANCING_DESC estructura

Estructura auxiliar para permitir la inicialización sencilla de una [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) estructura.

## <a name="syntax"></a>Sintaxis

```cpp
struct CD3DX12_VIEW_INSTANCING_DESC : public D3D12_VIEW_INSTANCING_DESC
{
    CD3DX12_VIEW_INSTANCING_DESC();
    explicit CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC& o) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT) noexcept;
    explicit CD3DX12_VIEW_INSTANCING_DESC(
        UINT InViewInstanceCount,
        const D3D12_VIEW_INSTANCE_LOCATION* InViewInstanceLocations,
        D3D12_VIEW_INSTANCING_FLAGS InFlags) noexcept;
};
```

## <a name="members"></a>Members

`CD3DX12_VIEW_INSTANCING_DESC`

Constructor predeterminado. Crea una nueva instancia sin inicializar de un **CD3DX12_VIEW_INSTANCING_DESC**.

`CD3DX12_VIEW_INSTANCING_DESC(const D3D12_VIEW_INSTANCING_DESC&)`

Constructor que crea una nueva instancia de un **CD3DX12_VIEW_INSTANCING_DESC** inicializado con el contenido de una [**D3DX12_VIEW_INSTANCING_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) estructura.

`CD3DX12_VIEW_INSTANCING_DESC(CD3DX12_DEFAULT)`

Constructor que crea una nueva instancia de un **CD3DX12_VIEW_INSTANCING_DESC** inicializado con estos valores.

|Miembro de datos|value|
|-|-|
|ViewInstanceCount|0|
|pViewInstanceLocations|nullptr|
|Marcas|D3D12_VIEW_INSTANCING_FLAG_NONE|

`CD3DX12_VIEW_INSTANCING_DESC(UINT, const D3D12_VIEW_INSTANCE_LOCATION*, D3D12_VIEW_INSTANCING_FLAGS)`

Constructor que crea una nueva instancia de un **CD3DX12_VIEW_INSTANCING_DESC** inicializado con los parámetros pasados a ella.

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado | [D3dx12.h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Consulte también

* [D3DX12_VIEW_INSTANCING_DESC](/windows/win32/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc)
* [Estructuras auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
