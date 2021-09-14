---
title: CD3DX12_BLEND_DESC estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ \_ DESC BLEND de D3D12.
ms.assetid: D37BB62E-904B-4953-9119-21F3B37570C0
keywords:
- CD3DX12_BLEND_DESC estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060805"
---
# <a name="cd3dx12_blend_desc-structure"></a>Estructura \_ DESC de BLEND CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ \_ DESC BLEND de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)

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



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ BLEND \_ DESC()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un \_ DESC de BLEND \_ CD3DX12.

</dd> <dt>

**EXPLICIT CD3DX12 \_ BLEND \_ DESC(const D3D12 \_ BLEND \_ DESC& o)**
</dt> <dd>

Crea una nueva instancia de un DESC BLEND CD3DX12, inicializado con el contenido de otra estructura \_ \_ [**\_ \_ DESC de BLEND D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)

</dd> <dt>

**EXPLICIT CD3DX12 \_ BLEND \_ DESC(CD3DX12 \_ DEFAULT)**
</dt> <dd>

Crea una nueva instancia de UN \_ \_ DESC BLEND CD3DX12, inicializado con parámetros predeterminados.



| State                                   | Valor predeterminado                    |
|-----------------------------------------|----------------------------------|
| AlphaToCoverageEnable                   | **FALSE**                        |
| IndependentBlendEnable                  | **FALSE**                        |
| RenderTarget \[ \] 0. BlendEnable           | **FALSE**                        |
| RenderTarget \[ \] 0. LogicOpEnable         | **FALSE**                        |
| RenderTarget \[ \] 0. SrcBlend              | D3D12 \_ BLEND \_ ONE                |
| RenderTarget \[ \] 0. DestBlend             | D3D12 \_ BLEND \_ ZERO               |
| RenderTarget \[ \] 0. BlendOp               | D3D12 \_ BLEND \_ OP \_ ADD            |
| RenderTarget \[ \] 0. SrcBlendAlpha         | D3D12 \_ BLEND \_ ONE                |
| RenderTarget \[ \] 0. DestBlendAlpha        | D3D12 \_ BLEND \_ ZERO               |
| RenderTarget \[ \] 0. BlendOpAlpha          | D3D12 \_ BLEND \_ OP \_ ADD            |
| RenderTarget \[ \] 0. LogicOp               | D3D12 \_ LOGIC \_ OP \_ NOOP           |
| RenderTarget \[ \] 0. RenderTargetWriteMask | D3D12 \_ COLOR \_ WRITE \_ ENABLE \_ ALL |



 

</dd> <dt>

**~CD3DX12 \_ BLEND \_ DESC()**
</dt> <dd>

Destruye una instancia de UN CD3DX12 \_ BLEND \_ DESC.

</dd> <dt>

**operator const D3D12 \_ BLEND \_ DESC&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ BLEND \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_blend_desc)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





