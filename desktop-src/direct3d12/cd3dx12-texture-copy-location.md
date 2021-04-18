---
title: CD3DX12_TEXTURE_COPY_LOCATION estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de ubicación de la copia de textura de D3D12 \_ \_ \_ .
ms.assetid: 8BA93729-2FFB-4C09-88B0-779049BAF385
keywords:
- Estructura de CD3DX12_TEXTURE_COPY_LOCATION
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
ms.openlocfilehash: f5143137f92e38662660588dd89a527f59644126
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707767"
---
# <a name="cd3dx12_texture_copy_location-structure"></a>CD3DX12 \_ \_ estructura de ubicación de copia de textura \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de ubicación de la [**\_ copia de textura de \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

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

**CD3DX12 \_ Ubicación de copia de textura \_ \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ Ubicación de copia de textura CD3DX12 \_ \_ .

</dd> <dt>

**Ubicación de copia de textura de CD3DX12 explícita \_ \_ \_ (const D3D12 \_ Ubicación de copia de textura \_ \_ &o)**
</dt> <dd>

Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializada con el contenido de otra estructura de [**Ubicación de copia de textura de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location) .

</dd> <dt>

**CD3DX12 \_ Ubicación de copia de textura \_ \_ (ID3D12Resource \* )**
</dt> <dd>

Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

</dd> <dt>

**\_ \_ \_ Ubicación de copia de textura de CD3DX12 (ID3D12Resource \* , D3D12 \_ colocada en la \_ superficie de Subrecursos \_ const& superficie)**
</dt> <dd>

Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

[**D3D12 \_ \_ \_ Superficie de Subrecursos colocada**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint) const& superficie

</dd> <dt>

**CD3DX12 \_ \_ \_ Ubicación de copia de textura (ID3D12RESOURCE \* pRes, uint sub)**
</dt> <dd>

Crea una nueva instancia de una ubicación de copia de textura de CD3DX12 \_ \_ \_ , inicializando los siguientes parámetros:

[**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) \* pRes

UINT sub

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ \_ Ubicación de copia de textura \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





