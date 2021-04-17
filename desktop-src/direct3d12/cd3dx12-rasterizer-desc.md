---
title: CD3DX12_RASTERIZER_DESC estructura (D3dx12. h)
description: Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una \_ estructura DESC de rasterizador D3D12 \_ .
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- Estructura de CD3DX12_RASTERIZER_DESC
topic_type:
- apiref
api_name:
- CD3DX12_RASTERIZER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 078b9e92d25cb5309b4cd97d35586192a37eed90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717610"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>CD3DX12 ( \_ estructura de Descripción del rasterizador) \_

Una estructura de aplicación auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ DESC de rasterizador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RASTERIZER_DESC  : public D3D12_RASTERIZER_DESC{
   CD3DX12_RASTERIZER_DESC();
   explicit CD3DX12_RASTERIZER_DESC(const D3D12_RASTERIZER_DESC& o);
   explicit CD3DX12_RASTERIZER_DESC(CD3DX12_DEFAULT);
   explicit CD3DX12_RASTERIZER_DESC(D3D12_FILL_MODE fillMode, D3D12_CULL_MODE cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12_CONSERVATIVE_RASTERIZATION_MODE conservativeRaster);
   ~CD3DX12_RASTERIZER_DESC();
   operator const D3D12_RASTERIZER_DESC&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ rasterizador \_ DESC ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ Descripción de rasterizador CD3DX12 \_ .

</dd> <dt>

**CD3DX12 de \_ rasterizador explícito \_ (const D3D12 de \_ rasterización de la \_&)**
</dt> <dd>

Crea una nueva instancia de una descripción de CD3DX12 de \_ rasterizador \_ , que se inicializa con el contenido de otra estructura de [**\_ \_ DESC del rasterizador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) .

</dd> <dt>

**CD3DX12 de \_ rasterizador explícito \_ ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de una descripción de CD3DX12 de \_ rasterizador \_ , inicializada con los parámetros predeterminados.

``` syntax
        FillMode = D3D12_FILL_MODE_SOLID;  
        CullMode = D3D12_CULL_MODE_BACK;  
        FrontCounterClockwise = FALSE;  
        DepthBias = D3D12_DEFAULT_DEPTH_BIAS;  
        DepthBiasClamp = D3D12_DEFAULT_DEPTH_BIAS_CLAMP;  
        SlopeScaledDepthBias = D3D12_DEFAULT_SLOPE_SCALED_DEPTH_BIAS;  
        DepthClipEnable = TRUE;  
        MultisampleEnable = FALSE;  
        AntialiasedLineEnable = FALSE;  
        ForcedSampleCount = 0;  
        ConservativeRaster = D3D12_CONSERVATIVE_RASTERIZATION_MODE_OFF;  
```

</dd> <dt>

**CD3DX12 de \_ rasterización Explicit \_ ( \_ \_ modo de relleno D3D12 fillMode, \_ D3D12 \_ modo de reselección CullMode, bool FrontCounterClockwise, int DepthBias, Float DepthBiasClamp, Float SlopeScaledDepthBias, BOOL DepthClipEnable, bool MultisampleEnable, bool antialiasedLineEnable, uint forcedSampleCount, D3D12 el \_ modo de \_ rasterización conservador \_ conservativeRaster)**
</dt> <dd>

Crea una nueva instancia de una descripción de CD3DX12 de \_ rasterizador \_ , inicializando los siguientes parámetros:

[**D3D12 \_ \_Modo de relleno**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_ \_Modo de selección**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode

BOOL frontCounterClockwise

INT depthBias

FLOAT depthBiasClamp

FLOAT slopeScaledDepthBias

BOOL depthClipEnable

BOOL multisampleEnable

BOOL antialiasedLineEnable

UINT forcedSampleCount

[**D3D12 \_ \_ \_ Modo de rasterización conservador**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~ CD3DX12 \_ rasterizador \_ DESC ()**
</dt> <dd>

Destruye una instancia de una descripción de CD3DX12 de \_ rasterizador \_ .

</dd> <dt>

**Operator const D3D12 \_ rasterizador \_ DESC& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Descripción de D3D12 \_ rasterizador \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





