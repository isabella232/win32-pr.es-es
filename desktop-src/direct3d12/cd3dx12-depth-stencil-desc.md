---
title: CD3DX12_DEPTH_STENCIL_DESC estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ DEPTH \_ STENCIL \_ DESC.
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- CD3DX12_DEPTH_STENCIL_DESC estructura
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f36a071251a12c4d27d06586775c01759b88d38
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160454"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>Estructura \_ \_ DESC de STENCIL \_ DEPTH de CD3DX12

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**D3D12 \_ DEPTH \_ STENCIL \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_DEPTH_STENCIL_DESC  : public D3D12_DEPTH_STENCIL_DESC{
   CD3DX12_DEPTH_STENCIL_DESC();
   explicit CD3DX12_DEPTH_STENCIL_DESC(const D3D12_DEPTH_STENCIL_DESC& o);
   explicit CD3DX12_DEPTH_STENCIL_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_DEPTH_STENCIL_DESC(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc);
   ~CD3DX12_DEPTH_STENCIL_DESC();
   operator const D3D12_DEPTH_STENCIL_DESC&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE CD3DX12 \_ \_ \_ DESC()**
</dt> <dd>

Crea una nueva instancia sin inicializar de D3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de D3DX12 DEPTH STENCIL DESC, inicializada con el contenido de otra estructura \_ \_ \_ [**D3D12 \_ DEPTH \_ STENCIL \_ DESC.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nueva instancia de D3DX12 \_ DEPTH \_ STENCIL \_ DESC, inicializada con parámetros predeterminados.

``` syntax
        DepthEnable = TRUE;  
        DepthWriteMask = D3D12_DEPTH_WRITE_MASK_ALL;  
        DepthFunc = D3D12_COMPARISON_FUNC_LESS;  
        StencilEnable = FALSE;  
        StencilReadMask = D3D12_DEFAULT_STENCIL_READ_MASK;  
        StencilWriteMask = D3D12_DEFAULT_STENCIL_WRITE_MASK;  
        const D3D12_DEPTH_STENCILOP_DESC defaultStencilOp =  
        { D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_STENCIL_OP_KEEP, D3D12_COMPARISON_FUNC_ALWAYS };  
        FrontFace = defaultStencilOp;  
        BackFace = defaultStencilOp;  
```

</dd> <dt>

**explicit CD3DX12 \_ DEPTH \_ STENCIL \_ DESC(BOOL depthEnable, D3D12 \_ DEPTH WRITE MASK \_ \_ depthWriteMask, D3D12 \_ COMPARISON \_ FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ STENCIL \_ OP frontStencilFailOp, D3D12 \_ STENCIL \_ OP frontStencilDepthFailOp, D3D12 \_ STENCIL \_ OP frontStencilPassOp, D3D12 \_ COMPARISON \_ FUNC frontStencilFunc, D3D12 \_ STENCIL \_ OP backStencilFailOp, D3D12 \_ STENCIL \_ OP backStencilDepthFailOp, D3D12 \_ STENCIL \_ OP backStencilPassOp, D3D12 \_ COMPARISON \_ FUNC backStencilFunc)**
</dt> <dd>

Crea una nueva instancia de D3DX12 \_ DEPTH \_ STENCIL \_ DESC, inicializando los parámetros siguientes:

PROFUNDIDAD DE BOOLEnable

[**D3D12 \_ DEPTH \_ WRITE \_ MASK**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) depthFunc

BOOL stencilEnable

UINT8 stencilReadMask

UINT8 stencilWriteMask

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) frontStencilPassOp

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) frontStencilFunc

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilDepthFailOp

[**D3D12 \_ STENCIL \_ OP**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) backStencilPassOp

[**D3D12 \_ COMPARISON \_ FUNC**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) backStencilFunc

</dd> <dt>

**~CD3DX12 \_ DEPTH \_ STENCIL \_ DESC()**
</dt> <dd>

Destruye una instancia de cd3DX12 \_ DEPTH \_ STENCIL \_ DESC.

</dd> <dt>

**operator const D3D12 \_ DEPTH \_ STENCIL \_ DESC&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





