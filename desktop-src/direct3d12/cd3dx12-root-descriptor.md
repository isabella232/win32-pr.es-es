---
title: CD3DX12_ROOT_DESCRIPTOR estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura DESCRIPTOR RAÍZ D3D12. \_ \_
ms.assetid: DB05BAB7-DD30-4EC7-8D66-C0B2D8DD7BAC
keywords:
- CD3DX12_ROOT_DESCRIPTOR estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566184"
---
# <a name="cd3dx12_root_descriptor-structure"></a>Estructura DEL \_ DESCRIPTOR RAÍZ DE CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ DESCRIPTOR \_ RAÍZ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)

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



## <a name="members"></a>Members

<dl> <dt>

**DESCRIPTOR RAÍZ CD3DX12() \_ \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DESCRIPTOR RAÍZ CD3DX12. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ ROOT \_ DESCRIPTOR(const D3D12 \_ ROOT DESCRIPTOR &\_ o)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RAÍZ CD3DX12, inicializado con el contenido de otra estructura DESCRIPTOR \_ \_ [**\_ \_ RAÍZ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)

</dd> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR(UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RAÍZ CD3DX12, \_ \_ inicializando los parámetros siguientes:

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

</dd> <dt>

**inline Init(UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

</dd> <dt>

**static inline Init(D3D12 \_ ROOT \_ DESCRIPTOR &table, UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Tabla \_ de &DESCRIPTOR**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor) RAÍZ

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DESCRIPTOR RAÍZ D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





