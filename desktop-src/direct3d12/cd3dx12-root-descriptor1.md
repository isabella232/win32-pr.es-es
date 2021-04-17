---
title: CD3DX12_ROOT_DESCRIPTOR1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ \_ estructura DESCRIPTOR1 raíz D3D12.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- Estructura de CD3DX12_ROOT_DESCRIPTOR1
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_DESCRIPTOR1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66cb64509c82c11180ca3e1d2937dff5d077897d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718489"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>CD3DX12 \_ raíz \_ DESCRIPTOR1 estructura

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ DESCRIPTOR1 raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_DESCRIPTOR1  : public D3D12_ROOT_DESCRIPTOR1{
       CD3DX12_ROOT_DESCRIPTOR1();
       explicit CD3DX12_ROOT_DESCRIPTOR1(const D3D12_ROOT_DESCRIPTOR1 &o);
       CD3DX12_ROOT_DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
  void static inline Init(D3D12_ROOT_DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_DESCRIPTOR1 raíz CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ DESCRIPTOR1 raíz CD3DX12 \_ .

</dd> <dt>

**CD3DX12 \_ raíz explícita \_ DESCRIPTOR1 (const D3D12 \_ raíz \_ DESCRIPTOR1 &)**
</dt> <dd>

Crea una nueva instancia de un \_ DESCRIPTOR1 raíz CD3DX12 \_ , inicializada con el contenido de otra [**estructura \_ \_ DESCRIPTOR1 raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) .

</dd> <dt>

**CD3DX12 \_ root \_ DESCRIPTOR1 (uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flag \_ Flags = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None)**
</dt> <dd>

Crea una nueva instancia de un \_ DESCRIPTOR1 raíz CD3DX12 \_ , inicializando los parámetros siguientes:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

</dd> <dt>

**Inicialización en línea (UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ raíz \_ descriptor marcas \_ Flags = D3D12 \_ marcador de \_ descriptor raíz \_ \_ ninguno)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

</dd> <dt>

**Static inline init (D3D12 \_ raíz \_ DESCRIPTOR1 &Table, uint SHADERREGISTER, uint registerSpace = 0, D3D12 \_ root \_ descriptor Flags \_ = D3D12 \_ \_ marcador de descriptor raíz \_ \_ None)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Tabla de &raíz \_ DESCRIPTOR1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)

UINT shaderRegister

UINT registerSpace = 0

[**D3D12 \_ Marcas \_ de \_ descriptor raíz**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) marcas = \_ marcador de \_ descriptor raíz D3D12 \_ \_ ninguno

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_DESCRIPTOR1 raíz \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





