---
title: CD3DX12_RESOURCE_ALLOCATION_INFO estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura DE INFORMACIÓN DE ASIGNACIÓN DE RECURSOS \_ \_ \_ D3D12.
ms.assetid: 81FC8D0E-2C15-42D3-9E06-1FE193F707C6
keywords:
- CD3DX12_RESOURCE_ALLOCATION_INFO estructura
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
ms.openlocfilehash: 63915f2fa05950ad96bc621b9887b1c4fe23149e22ba408767d111f7b74d6927
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729225"
---
# <a name="cd3dx12_resource_allocation_info-structure"></a>Estructura DE INFORMACIÓN DE ASIGNACIÓN DE \_ RECURSOS \_ CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una estructura DE INFORMACIÓN DE ASIGNACIÓN DE RECURSOS [**\_ \_ D3D12. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

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

**CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una INFORMACIÓN DE ASIGNACIÓN DE RECURSOS CD3DX12. \_ \_ \_

</dd> <dt>

**explicit CD3DX12 \_ RESOURCE \_ ALLOCATION \_ INFO(const D3D12 \_ RESOURCE ALLOCATION INFO& \_ \_ o)**
</dt> <dd>

Crea una nueva instancia de UNA INFORMACIÓN DE ASIGNACIÓN DE RECURSOS CD3DX12, inicializada con el contenido de otra estructura DE INFORMACIÓN DE ASIGNACIÓN DE RECURSOS \_ \_ \_ [**\_ \_ \_ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)

</dd> <dt>

**INFORMACIÓN DE ASIGNACIÓN DE RECURSOS CD3DX12 \_ \_ \_ (tamaño UINT64, alineación UINT64)**
</dt> <dd>

Crea una nueva instancia de UNA INFORMACIÓN DE ASIGNACIÓN DE RECURSOS CD3DX12, \_ \_ \_ inicializando los parámetros siguientes:

Tamaño de UINT64

Alineación de UINT64

</dd> <dt>

**operator const D3D12 \_ RESOURCE \_ ALLOCATION INFO \_&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**INFORMACIÓN DE ASIGNACIÓN DE RECURSOS D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_resource_allocation_info)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





