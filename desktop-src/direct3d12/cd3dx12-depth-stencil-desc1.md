---
title: CD3DX12_DEPTH_STENCIL_DESC1 estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura DESC1 de D3D12 Depth \_ \_ .
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- Estructura de CD3DX12_DEPTH_STENCIL_DESC1
topic_type:
- apiref
api_name:
- CD3DX12_DEPTH_STENCIL_DESC1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c05ec4f3ca85ccfcebb6a13dbe408ba05c64e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649383"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>CD3DX12 de estarcido de profundidad de la \_ \_ \_ estructura DESC1

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ \_ DESC1 de D3D12 Depth**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_DEPTH_STENCIL_DESC1  : public D3D12_DEPTH_STENCIL_DESC1{
  CD3DX12_DEPTH_STENCIL_DESC1 CD3DX12_DEPTH_STENCIL_DESC1();
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC1& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(const D3D12_DEPTH_STENCIL_DESC& o);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(CD3DX12_DEFAULT);
  CD3DX12_DEPTH_STENCIL_DESC1 explicit CD3DX12_DEPTH_STENCIL_DESC1(BOOL depthEnable, D3D12_DEPTH_WRITE_MASK depthWriteMask, D3D12_COMPARISON_FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12_STENCIL_OP frontStencilFailOp, D3D12_STENCIL_OP frontStencilDepthFailOp, D3D12_STENCIL_OP frontStencilPassOp, D3D12_COMPARISON_FUNC frontStencilFunc, D3D12_STENCIL_OP backStencilFailOp, D3D12_STENCIL_OP backStencilDepthFailOp, D3D12_STENCIL_OP backStencilPassOp, D3D12_COMPARISON_FUNC backStencilFunc, BOOL depthBoundsTestEnable);
                              ~CD3DX12_DEPTH_STENCIL_DESC1();
                              operator const D3D12_DEPTH_STENCIL_DESC1&() const;
                              operator const D3D12_DEPTH_STENCIL_DESC() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ DESC1 ()**
</dt> <dd>

Crea una instancia nueva, no inicializada, de una galería de símbolos de profundidad de CD3DX12 \_ \_ \_ DESC1.

</dd> <dt>

**Galería de \_ símbolos de profundidad CD3DX12 explícita \_ \_ DESC1 (const D3D12 \_ Depth \_ estarcido \_ DESC1&)**
</dt> <dd>

Crea una nueva instancia de una galería de símbolos de profundidad de CD3DX12 \_ \_ \_ DESC1, inicializada con los valores copiados de una estructura de [**estarcido de \_ profundidad D3D12 \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1) .

</dd> <dt>

**Galería de \_ símbolos de profundidad CD3DX12 explícita \_ \_ DESC1 (const D3D12 \_ Depth \_ estarcido \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores copiados de una estructura de descripción de la [**Galería de \_ \_ símbolos \_ D3D12 Depth**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc) .

y el miembro **DepthBoundsTestEnable** adicional establecido en **false**.

</dd> <dt>

**Galería de símbolos de profundidad de CD3DX12 explícita \_ \_ \_ DESC1 ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de una galería de símbolos de profundidad de CD3DX12 \_ \_ \_ DESC1, inicializada con el estado predeterminado indicado por D3DX12:

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
    DepthBoundsTestEnable = FALSE;
          
```

</dd> <dt>

**\_ \_ Galería de símbolos de profundidad de CD3DX12 explícita \_ DESC1 (bool depthEnable, D3D12 \_ Depth \_ \_ Mask Mask depthWriteMask, D3D12 \_ Comparison \_ FUNC DEPTHFUNC, bool STENCILENABLE, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ stencil OP frontStencilFailOp, \_ D3D12 \_ cliché \_ OP frontStencilDepthFailOp, D3D12 stencil \_ OP \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ frontStencilPassOp, D3D12 Comparison frontStencilFunc, D3D12, backStencilFailOp, D3D12, backStencilDepthFailOp de estarcido OP D3D12)**
</dt> <dd>

Crea una nueva instancia de una \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, inicializada con los valores pasados en la lista de parámetros.

</dd> <dt>

**~ CD3DX12 de la \_ Galería de símbolos de profundidad \_ \_ DESC1 ()**
</dt> <dd>

Destruye una instancia de una galería de \_ símbolos de profundidad de D3DX12 \_ \_ DESC1.

</dd> <dt>

**operador const D3D12 \_ Depth \_ esténcil \_ DESC1& () Const**
</dt> <dd>

Conversión implícita a una \_ estructura DESC1 de D3D12 Depth \_ \_ . Dado que \_ \_ la Galería \_ de símbolos de profundidad de D3D12 DESC1 es el tipo subyacente de la \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, el objeto simplemente se devuelve como una \_ \_ \_ referencia de D3D12 de estarcido de profundidad const DESC1.

</dd> <dt>

**operador const D3D12 \_ Depth \_ estarcido \_ DESC () Const**
</dt> <dd>

Conversión implícita a un \_ valor de \_ estructura DESC de estarcido D3D12 Depth \_ . Dado \_ que D3D12 Depth \_ stencil \_ no es el tipo subyacente de CD3DX12 \_ Depth \_ stencil \_ DESC1, se crea una nueva instancia de la galería de símbolos de profundidad D3D12 \_ \_ \_ y se devuelve por valor. Tenga en cuenta \_ que \_ la descripción de la galería de símbolos de profundidad \_ de D3D12 no incluye el miembro **DepthBoundsTestEnable** , por lo que este valor se pierde en la conversión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**Galería de símbolos de profundidad de D3D12 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**D3D12 de la \_ Galería de símbolos de profundidad \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





