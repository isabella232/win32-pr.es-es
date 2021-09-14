---
title: CD3DX12_ROOT_DESCRIPTOR1 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ ROOT \_ DESCRIPTOR1.
ms.assetid: 664822BF-5C27-4541-953F-219894547A6C
keywords:
- CD3DX12_ROOT_DESCRIPTOR1 estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126965023"
---
# <a name="cd3dx12_root_descriptor1-structure"></a>Estructura CD3DX12 \_ ROOT \_ DESCRIPTOR1

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**D3D12 \_ ROOT \_ DESCRIPTOR1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)

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



## <a name="members"></a>Members

<dl> <dt>

**DESCRIPTOR RAÍZ \_ CD3DX121() \_**
</dt> <dd>

Crea una nueva instancia sin inicializar de un DESCRIPTOR RAÍZ CD3DX121. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ ROOT \_ DESCRIPTOR1(const D3D12 \_ ROOT \_ DESCRIPTOR1 &o)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RAÍZ CD3DX12, inicializado con el contenido de otra estructura \_ \_ [**D3D12 \_ ROOT \_ DESCRIPTOR1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)

</dd> <dt>

**CD3DX12 \_ ROOT \_ DESCRIPTOR1(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAG \_ NONE)**
</dt> <dd>

Crea una nueva instancia de un DESCRIPTOR RAÍZ \_ \_ CD3DX12, inicializando los parámetros siguientes:

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

</dd> <dt>

**inline Init(UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT \_ DESCRIPTOR \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

</dd> <dt>

**static inline Init(D3D12 \_ ROOT \_ DESCRIPTOR1 &table, UINT shaderRegister, UINT registerSpace = 0, D3D12 \_ ROOT DESCRIPTOR \_ \_ FLAGS flags = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ Tabla \_ raíz descriptor1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1) &raíz

Sombreador UINTRegistrar

UINT registerSpace = 0

[**D3D12 \_ MARCAS \_ DE DESCRIPTOR RAÍZ \_ FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ ROOT DESCRIPTOR FLAG \_ \_ \_ NONE

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DESCRIPTOR RAÍZ D3D121 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_descriptor1)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





