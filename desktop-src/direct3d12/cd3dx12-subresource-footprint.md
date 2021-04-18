---
title: CD3DX12_SUBRESOURCE_FOOTPRINT estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de superficie de SUBRECURSO D3D12 \_ .
ms.assetid: 17266FB0-41B5-4A70-A896-206B54F5E76F
keywords:
- Estructura de CD3DX12_SUBRESOURCE_FOOTPRINT
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717596"
---
# <a name="cd3dx12_subresource_footprint-structure"></a>\_Estructura de superficie de SUBrecurso de CD3DX12 \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ superficie de subrecurso D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**\_Superficie de SUBrecursos de CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ superficie de SUBRECURSO CD3DX12 \_ .

</dd> <dt>

**superficie de subrecurso CD3DX12 explícita \_ \_ ( \_ espacio de Subrecurso const D3D12 \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ superficie de SUBrecurso de CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ \_ superficie de subrecurso de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint) .

</dd> <dt>

**\_Superficie de SUBrecursos de CD3DX12 \_ ( \_ formato de formato de DXGI, ancho uint, alto de UINT, profundidad uint, uint rowPitch)**
</dt> <dd>

Crea una nueva instancia de una \_ superficie de subrecurso de CD3DX12 \_ , inicializando los siguientes parámetros:

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Ancho de UINT

Alto de UINT

Profundidad de UINT

UINT rowPitch

</dd> <dt>

**\_superficie de SUBrecurso de CD3DX12 explícita \_ (const D3D12 \_ \_ de DESC& resDesc, uint rowPitch)**
</dt> <dd>

Crea una nueva instancia de una \_ superficie de subrecurso de CD3DX12 \_ , inicializando los siguientes parámetros:

[**D3D12 \_& de \_ DESC de recursos**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_desc) resDesc

UINT rowPitch

</dd> <dt>

**operador const D3D12 \_ subresource \_ superficie& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Superficie de SUBrecursos de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_footprint)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

