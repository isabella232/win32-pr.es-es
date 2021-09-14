---
title: CD3DX12_DEPTH_STENCIL_DESC1 estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura D3D12 \_ DEPTH \_ STENCIL \_ DESC1.
ms.assetid: 8EB008F9-212D-486E-9C62-D7BA9D3C6807
keywords:
- CD3DX12_DEPTH_STENCIL_DESC1 estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160453"
---
# <a name="cd3dx12_depth_stencil_desc1-structure"></a>Estructura \_ \_ DESC1 DE STENCIL \_ DEPTH de CD3DX12

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)

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



## <a name="members"></a>Members

<dl> <dt>

**GALERÍA DE SÍMBOLOS DE PROFUNDIDAD DE CD3DX12 \_ \_ \_ DESC1()**
</dt> <dd>

Crea una nueva instancia de CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1, sin inicializar.

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1(const D3D12 \_ DEPTH \_ STENCIL \_ DESC1& o)**
</dt> <dd>

Crea una nueva instancia de un CD3DX12 DEPTH STENCIL DESC1, inicializado con valores copiados de una estructura \_ \_ \_ [**D3D12 \_ DEPTH \_ STENCIL \_ DESC1.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1(const D3D12 \_ DEPTH \_ STENCIL \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de una instancia de CD3DX12 DEPTH STENCIL DESC1, inicializada con valores copiados de una estructura \_ \_ \_ [**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)

y el miembro **DepthBoundsTestEnable** adicional establecido en **FALSE.**

</dd> <dt>

**EXPLICIT CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nueva instancia de una instancia de CD3DX12 DEPTH STENCIL DESC1, inicializada con el estado predeterminado prescrito por \_ \_ \_ D3DX12:

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

**explicit CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1(BOOL depthEnable, Profundidad de \_ \_ D3D12 DEPTH WRITE \_ MASKWriteMask, D3D12 \_ COMPARISON \_ FUNC depthFunc, BOOL stencilEnable, UINT8 stencilReadMask, UINT8 stencilWriteMask, D3D12 \_ STENCIL \_ OP frontStencilFailOp, D3D12 \_ STENCIL \_ OP frontStencilDepthFailOp, \_ \_ D3D12 STENCIL OP frontStencilPassOp, D3D12 \_ COMPARISON \_ FUNC frontStencilFunc, D3D12 \_ STENCIL \_ OP backStencilFailOp, \_ D3D12 STENCIL \_ OP backStencilDepthFailOp, D3D12 \_ STENCIL \_ OP backStencilPassOp, D3D12 \_ COMPARISON \_ FUNC backStencilFunc, BOOL depthBoundsTestEnable)**
</dt> <dd>

Crea una nueva instancia de una instancia de CD3DX12 \_ DEPTH \_ STENCIL DESC1, inicializada con los valores pasados \_ en la lista de parámetros.

</dd> <dt>

**~CD3DX12 \_ DEPTH \_ STENCIL \_ DESC1()**
</dt> <dd>

Destruye una instancia de D3DX12 \_ DEPTH \_ STENCIL \_ DESC1.

</dd> <dt>

**operator const D3D12 \_ DEPTH \_ STENCIL \_ DESC1&() const**
</dt> <dd>

Conversión implícita en una estructura D3D12 \_ DEPTH \_ STENCIL \_ DESC1. Dado que D3D12 DEPTH STENCIL DESC1 es el tipo subyacente de CD3DX12 DEPTH STENCIL DESC1, el objeto simplemente se devuelve como una referencia \_ \_ \_ \_ \_ \_ const D3D12 \_ DEPTH \_ STENCIL \_ DESC1 a sí mismo.

</dd> <dt>

**operator const D3D12 \_ DEPTH \_ STENCIL \_ DESC() const**
</dt> <dd>

Conversión implícita a un valor de estructura D3D12 \_ DEPTH \_ STENCIL \_ DESC. Dado que D3D12 DEPTH STENCIL DESC no es el tipo subyacente de \_ \_ CD3DX12 DEPTH STENCIL DESC1, se crea una nueva instancia de \_ \_ \_ \_ D3D12 \_ DEPTH \_ STENCIL \_ DESC y se devuelve por valor. Tenga en cuenta que D3D12 DEPTH STENCIL DESC no incluye el miembro \_ \_ \_ **DepthBoundsTestEnable,** por lo que este valor se pierde en la conversión.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**GALERÍA DE SÍMBOLOS DE PROFUNDIDAD D3D12 \_ \_ \_ DESC1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc1)
</dt> <dt>

[**D3D12 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_desc)
</dt> </dl>

 

 





