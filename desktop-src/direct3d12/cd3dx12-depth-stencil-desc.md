---
title: CD3DX12_DEPTH_STENCIL_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de descripción de la galería de símbolos de profundidad de D3D12 \_ \_ \_ .
ms.assetid: D3DB04C3-4564-45A4-830A-E63B8D308B33
keywords:
- Estructura de CD3DX12_DEPTH_STENCIL_DESC
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649386"
---
# <a name="cd3dx12_depth_stencil_desc-structure"></a>CD3DX12 \_ Descripción de la galería de símbolos de profundidad \_ \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de descripción de la [**Galería de símbolos de profundidad de D3D12 \_ \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ ()**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ \_ .

</dd> <dt>

**Galería de símbolos de profundidad de CD3DX12 explícita \_ \_ \_ DESC (const D3D12 \_ Depth \_ estarcido \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de una descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ \_ , inicializada con el contenido de otra estructura de la [**Galería de \_ símbolos de profundidad \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

</dd> <dt>

**Galería de símbolos de profundidad de CD3DX12 explícita \_ \_ \_ DESC ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de una descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ \_ , inicializada con los parámetros predeterminados.

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

**CD3DX12 de la \_ Galería de símbolos de profundidad de profundidad explícita \_ \_ (bool depthEnable, D3D12 \_ profundidad de escritura de profundidad \_ \_ depthWriteMask, D3D12 \_ Comparison \_ FUNC DEPTHFUNC, bool STENCILENABLE, UINT8 StencilReadMask, UINT8 stencilWriteMask, D3D12 \_ ESTÉNCIL \_ OP frontStencilFailOp, D3D12 stencil OP frontStencilDepthFailOp, D3D12 ESTÉNCIL OP frontStencilPassOp, D3D12 Comparison \_ \_ \_ \_ \_ \_ frontStencilFunc, D3D12 \_ \_ , \_ \_ \_ \_ \_ \_ backStencilFailOp**
</dt> <dd>

Crea una nueva instancia de una \_ Descripción de la galería de símbolos de profundidad de D3DX12 \_ \_ , inicializando los siguientes parámetros:

BOOL depthEnable

[**D3D12 \_ \_ \_ Máscara de escritura de profundidad**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_depth_write_mask) depthWriteMask

[**D3D12 \_ DepthFunc \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) de función de comparación

BOOL stencilEnable

UINT8 stencilReadMask

UINT8 stencilWriteMask

[**D3D12 \_ FrontStencilFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido

[**D3D12 \_ FrontStencilDepthFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido

[**D3D12 \_ FrontStencilPassOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido

[**D3D12 \_ FrontStencilFunc \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) de función de comparación

[**D3D12 \_ BackStencilFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido

[**D3D12 \_ BackStencilDepthFailOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido

[**D3D12 \_ BackStencilPassOp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_stencil_op) de la operación de estarcido

[**D3D12 \_ BackStencilFunc \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) de función de comparación

</dd> <dt>

**~ CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ ()**
</dt> <dd>

Destruye una instancia de una descripción de la galería de símbolos de profundidad de CD3DX12 \_ \_ \_ .

</dd> <dt>

**operador const D3D12 \_ Depth \_ estarcido \_ DESC& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 de la \_ Galería de símbolos de profundidad \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





