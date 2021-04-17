---
title: CD3DX12_RESOURCE_ALLOCATION_INFO estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de información de asignación de recursos de D3D12 \_ \_ .
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- Estructura de CD3DX12_RESOURCE_ALLOCATION_INFO
topic_type:
- apiref
api_name:
- CD3DX12_RESOURCE_ALLOCATION_INFO
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08542c7460b2fadf381f85dc271167258e31fb46
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717608"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>CD3DX12 \_ \_ estructura de información de asignación de recursos \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**información de asignación de recursos de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RESOURCE_ALLOCATION_INFO  : public D3D12_RESOURCE_ALLOCATION_INFO{
   CD3DX12_RESOURCE_ALLOCATION_INFO();
   explicit CD3DX12_RESOURCE_ALLOCATION_INFO(const D3D12_RESOURCE_ALLOCATION_INFO& o);
   CD3DX12_RESOURCE_ALLOCATION_INFO(UINT64 size, UINT64 alignment);
   operator const D3D12_RESOURCE_ALLOCATION_INFO&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**Información de asignación de recursos de CD3DX12 \_ \_ \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de la información de asignación de recursos de CD3DX12 \_ \_ \_ .

</dd> <dt>

**información de \_ asignación de recursos CD3DX12 explícita \_ \_ (const D3D12 \_ información de asignación de recursos \_ \_& o)**
</dt> <dd>

Crea una nueva instancia de una \_ información de asignación de recursos CD3DX12 \_ \_ , inicializada con el contenido de otra estructura de información de [**\_ asignación de recursos \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info) .

</dd> <dt>

**\_ \_ \_ Información de asignación de recursos CD3DX12 (tamaño UINT64, alineación UInt64)**
</dt> <dd>

Crea una nueva instancia de una \_ información de asignación de recursos CD3DX12 \_ \_ , inicializando los siguientes parámetros:

UINT64 size

Alineación UINT64

</dd> <dt>

**operador const D3D12 \_ información de asignación de recursos \_ \_& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Información de \_ asignación de recursos de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





