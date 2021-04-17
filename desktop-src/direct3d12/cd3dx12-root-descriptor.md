---
title: CD3DX12_ROOT_DESCRIPTOR estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura de descriptor raíz D3D12.
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 710064436e0287b570700ff5812b728ca62be56d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718492"
---
# <a name="cd3dx12_root_descriptor-structure"></a>CD3DX12 \_ \_ estructura de descriptor raíz

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_DESCRIPTOR  : public D3D12_ROOT_DESCRIPTOR{
       CD3DX12_ROOT_DESCRIPTOR();
       explicit CD3DX12_ROOT_DESCRIPTOR(const D3D12_ROOT_DESCRIPTOR &o);
       CD3DX12_ROOT_DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Descriptor raíz CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ \_ descriptor raíz CD3DX12.

</dd> <dt>

**descriptor de raíz de CD3DX12 explícito \_ \_ ( \_ \_ &o descriptor de raíz const D3D12)**
</dt> <dd>

Crea una nueva instancia de un \_ \_ descriptor raíz CD3DX12, inicializada con el contenido de otra estructura de [**\_ \_ descriptor raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) .

</dd> <dt>

**\_ \_ Descriptor raíz de CD3DX12 (uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Crea una nueva instancia de un \_ \_ descriptor raíz CD3DX12, inicializando los parámetros siguientes:

UINT shaderRegister

rechace UINT registerSpace = 0

</dd> <dt>

**Init en línea (UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

rechace UINT registerSpace = 0

</dd> <dt>

**Init inline init (D3D12 \_ root \_ descriptor &Table, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Tabla de &de \_ descriptor raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)

UINT shaderRegister

rechace UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Descriptor raíz de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





