---
title: CD3DX12_RASTERIZER_DESC estructura (D3dx12.h)
description: Una estructura auxiliar para permitir la inicialización sencilla de una estructura \_ DESC de RASTERIZER \_ D3D12.
ms.assetid: 28AA8256-1CAF-484F-B219-0F0461BA947C
keywords:
- CD3DX12_RASTERIZER_DESC estructura
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
ms.openlocfilehash: faa95dde87aea8e3c61d0d1fb6de6845f33717f6a46db4df7996a23afd7590b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119729435"
---
# <a name="cd3dx12_rasterizer_desc-structure"></a>Estructura \_ DESC de RASTERIZER CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ \_ DESC de RASTERIZER D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)

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

**CD3DX12 \_ RASTERIZER \_ DESC()**
</dt> <dd>

Crea una nueva instancia de UNSC RASTERIZER CD3DX12 \_ \_ sin inicializar.

</dd> <dt>

**EXPLICIT CD3DX12 \_ RASTERIZER \_ DESC(const D3D12 \_ RASTERIZER \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de un DESC RASTERIZER CD3DX12, inicializado con el contenido de otra estructura \_ \_ [**\_ \_ DESC de RASTERIZER D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)

</dd> <dt>

**EXPLICIT CD3DX12 \_ RASTERIZER \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nueva instancia de UN \_ DESC RASTERIZER CD3DX12, \_ inicializado con parámetros predeterminados.

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

**EXPLICIT CD3DX12 \_ RASTERIZER \_ DESC(D3D12 \_ FILL MODE \_ fillMode, D3D12 \_ CULL MODE \_ cullMode, BOOL frontCounterClockwise, INT depthBias, FLOAT depthBiasClamp, FLOAT slopeScaledDepthBias, BOOL depthClipEnable, BOOL multisampleEnable, BOOL antialiasedLineEnable, UINT forcedSampleCount, D3D12 \_ CONSERVATIVE \_ RASTERIZATION MODE \_ conservativeRaster)**
</dt> <dd>

Crea una nueva instancia de CD3DX12 \_ RASTERIZER \_ DESC, inicializando los parámetros siguientes:

[**D3D12 \_ FILL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) fillMode

[**D3D12 \_ CULL \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode) cullMode

BOOL frontCounterClockwise

INT depthBias

Float depthBiasClamp

FLOAT slopeScaledDepthBias

BOOL depthClipEnable

BOOL multisampleEnable

BOOL antialiasedLineEnable

UINT forcedSampleCount

[**D3D12 \_ CONSERVATIVE \_ RASTERIZATION \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) conservativeRaster

</dd> <dt>

**~CD3DX12 \_ RASTERIZER \_ DESC()**
</dt> <dd>

Destruye una instancia de un \_ DESC RASTERIZER CD3DX12. \_

</dd> <dt>

**operator const D3D12 \_ RASTERIZER \_ DESC&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ RASTERIZER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





