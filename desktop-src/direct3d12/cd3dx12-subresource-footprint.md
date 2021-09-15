---
title: CD3DX12_SUBRESOURCE_FOOTPRINT estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ SUBRESOURCE \_ FOOTPRINT.
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- CD3DX12_SUBRESOURCE_FOOTPRINT estructura
topic_type:
- apiref
api_name:
- CD3DX12_SUBRESOURCE_FOOTPRINT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab58e9a007d736222d9525d7a064456a1a9a7f14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566669"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>Estructura CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura D3D12 \_ SUBRESOURCE \_ FOOTPRINT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_SUBRESOURCE_FOOTPRINT  : public D3D12_SUBRESOURCE_FOOTPRINT{
   CD3DX12_SUBRESOURCE_FOOTPRINT();
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_SUBRESOURCE_FOOTPRINT &o);
   CD3DX12_SUBRESOURCE_FOOTPRINT(DXGI_FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch);
   explicit CD3DX12_SUBRESOURCE_FOOTPRINT(const D3D12_RESOURCE_DESC& resDesc, UINT rowPitch);
   operator const D3D12_SUBRESOURCE_FOOTPRINT&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una SUPERFICIE \_ DE SUBRECURSO CD3DX12. \_

</dd> <dt>

**SUPERFICIE DE SUBCURSO CD3DX12 \_ \_ explícita(const D3D12 \_ \_ SUBRESOURCE FOOTPRINT &o)**
</dt> <dd>

Crea una nueva instancia de una SUPERFICIE DE SUBCURSO CD3DX12, inicializada con el contenido de otra estructura DE SUPERFICIE \_ \_ DE [**\_ SUBCURSO \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)

</dd> <dt>

**CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(DXGI \_ FORMAT format, UINT width, UINT height, UINT depth, UINT rowPitch)**
</dt> <dd>

Crea una nueva instancia de UNA SUPERFICIE DE SUBCURSO CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Ancho de UINT

Alto de UINT

Profundidad UINT

RowPitch de UINT

</dd> <dt>

**EXPLICIT CD3DX12 \_ SUBRESOURCE \_ FOOTPRINT(const D3D12 \_ RESOURCE \_ DESC& resDesc, UINT rowPitch)**
</dt> <dd>

Crea una nueva instancia de UNA SUPERFICIE DE SUBCURSO CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**D3D12 \_ RESOURCE \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc)& resDesc

RowPitch de UINT

</dd> <dt>

**operator const D3D12 \_ SUBRESOURCE \_ FOOTPRINT&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SUPERFICIE DE SUBRECURSO D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

