---
title: CD3DX12_BLEND_DESC estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura DESC de D3D12 Blend \_ .
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- Estructura de CD3DX12_BLEND_DESC
topic_type:
- apiref
api_name:
- CD3DX12_BLEND_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddb88ce003f74251c3ce34a2ca47ae2fb55f892d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707777"
---
# <a name="cd3dx12_blend_desc-structure"></a>CD3DX12 \_ Blend ( \_ estructura de DESC)

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura [**\_ \_ DESC de D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_BLEND_DESC  : public D3D12_BLEND_DESC{
   CD3DX12_BLEND_DESC();
   explicit CD3DX12_BLEND_DESC(const D3D12_BLEND_DESC& o);
   explicit CD3DX12_BLEND_DESC(CD3DX12_DEFAULT);
   ~CD3DX12_BLEND_DESC();
   operator const D3D12_BLEND_DESC&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una descripción de CD3DX12 \_ Blend \_ .

</dd> <dt>

**Explicit CD3DX12 \_ Blend \_ DESC (const D3D12 \_ Blend \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de una descripción de CD3DX12 \_ Blend \_ , inicializada con el contenido de otra estructura [**\_ \_ DESC de D3D12 Blend**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc) .

</dd> <dt>

**CD3DX12 \_ Blend Explicit \_ ( \_ valor predeterminado de CD3DX12)**
</dt> <dd>

Crea una nueva instancia de una descripción de CD3DX12 \_ Blend \_ , inicializada con los parámetros predeterminados.



| Estado                                   | Valor predeterminado                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ 0 \] . BlendEnable           | **FALSE**                        |
| RenderTarget \[ 0 \] . LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ 0 \] . SrcBlend              | D3D12 \_ Blend \_ uno                |
| RenderTarget \[ 0 \] . DestBlend             | Cero de D3D12 \_ Blend \_               |
| RenderTarget \[ 0 \] . BlendOp               | Operación de incorporación de D3D12 \_ Blend \_ \_            |
| RenderTarget \[ 0 \] . SrcBlendAlpha         | D3D12 \_ Blend \_ uno                |
| RenderTarget \[ 0 \] . DestBlendAlpha        | Cero de D3D12 \_ Blend \_               |
| RenderTarget \[ 0 \] . BlendOpAlpha          | Operación de incorporación de D3D12 \_ Blend \_ \_            |
| RenderTarget \[ 0 \] . LogicOp               | D3D12 \_ Logical \_ \_           |
| RenderTarget \[ 0 \] . RenderTargetWriteMask | D3D12 \_ de \_ escritura de color \_ habilitar \_ todo |



 

</dd> <dt>

**~ CD3DX12 \_ Blend \_ DESC ()**
</dt> <dd>

Destruye una instancia de una descripción de CD3DX12 \_ Blend \_ .

</dd> <dt>

**Operator const D3D12 \_ Blend \_ DESC& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ Blend \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





