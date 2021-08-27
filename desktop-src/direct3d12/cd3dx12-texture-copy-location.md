---
title: CD3DX12_TEXTURE_COPY_LOCATION estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura TEXTURE COPY LOCATION de D3D12. \_ \_ \_
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- CD3DX12_TEXTURE_COPY_LOCATION estructura
topic_type:
- apiref
api_name:
- CD3DX12_TEXTURE_COPY_LOCATION
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d0a1ee179d2400bc04df9c3214d97d3c7a861357f33b7805e492a24f769bdba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120119645"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>Estructura DE UBICACIÓN DE COPIA DE TEXTURA DE CD3DX12 \_ \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura TEXTURE COPY LOCATION \_ \_ \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_TEXTURE_COPY_LOCATION  : public D3D12_TEXTURE_COPY_LOCATION{
   CD3DX12_TEXTURE_COPY_LOCATION();
   explicit CD3DX12_TEXTURE_COPY_LOCATION(const D3D12_TEXTURE_COPY_LOCATION &o);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, D3D12_PLACED_SUBRESOURCE_FOOTPRINT const& Footprint);
   CD3DX12_TEXTURE_COPY_LOCATION(ID3D12Resource* pRes, UINT Sub);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**UBICACIÓN DE COPIA DE \_ TEXTURA CD3DX12() \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de una UBICACIÓN DE COPIA DE TEXTURA CD3DX12. \_ \_ \_

</dd> <dt>

**explicit CD3DX12 \_ TEXTURE \_ COPY \_ LOCATION(const D3D12 \_ TEXTURE COPY LOCATION &\_ \_ o)**
</dt> <dd>

Crea una nueva instancia de UNA UBICACIÓN DE COPIA DE TEXTURA CD3DX12, inicializada con el contenido de otra estructura \_ \_ \_ [**D3D12 \_ TEXTURE \_ COPY \_ LOCATION.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)

</dd> <dt>

**UBICACIÓN DE COPIA DE \_ TEXTURA DE CD3DX12(ID3D12Resource \_ \_ \* pRes)**
</dt> <dd>

Crea una nueva instancia de una instancia de TEXTURE COPY LOCATION de CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Pres

</dd> <dt>

**UBICACIÓN DE COPIA DE TEXTURA DE \_ \_ \_ CD3DX12(ID3D12Resource \* pRes, D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT const& Footprint)**
</dt> <dd>

Crea una nueva instancia de una instancia de TEXTURE COPY LOCATION de CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Pres

[**D3D12 \_ PLACED \_ SUBRESOURCE \_ FOOTPRINT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& Footprint

</dd> <dt>

**UBICACIÓN DE COPIA DE \_ TEXTURA \_ DE \_ CD3DX12(ID3D12Resource \* pRes, UINT Sub)**
</dt> <dd>

Crea una nueva instancia de una instancia de TEXTURE COPY LOCATION de CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* Pres

UINT Sub

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UBICACIÓN DE COPIA DE TEXTURA D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





