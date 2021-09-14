---
title: CD3DX12_CLEAR_VALUE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura CLEAR VALUE de D3D12. \_ \_
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- CD3DX12_CLEAR_VALUE estructura
topic_type:
- apiref
api_name:
- CD3DX12_CLEAR_VALUE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b9dc7afc62c6e9a3e229e6f5bdc4287bf4b85a9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060803"
---
# <a name="cd3dx12_clear_value-structure"></a>Estructura CLEAR VALUE de CD3DX12 \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ CLEAR VALUE \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_CLEAR_VALUE  : public D3D12_CLEAR_VALUE{
   CD3DX12_CLEAR_VALUE();
   explicit CD3DX12_CLEAR_VALUE(const D3D12_CLEAR_VALUE &o);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, const FLOAT color[ 4 ]);
   CD3DX12_CLEAR_VALUE(DXGI_FORMAT format, FLOAT depth, UINT8 stencil);
   operator const D3D12_CLEAR_VALUE&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ CLEAR \_ VALUE()**
</dt> <dd>

Crea una nueva instancia de CLEAR VALUE cd3DX12 sin \_ \_ inicializar.

</dd> <dt>

**explicit CD3DX12 \_ CLEAR \_ VALUE(const D3D12 \_ CLEAR VALUE &\_ o)**
</dt> <dd>

Crea una nueva instancia de CLEAR VALUE de CD3DX12, inicializada con el contenido de otra estructura \_ \_ CLEAR VALUE [**\_ \_ de D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE(formato DXGI \_ FORMAT, const FLOAT color \[ 4 \] )**
</dt> <dd>

Crea una nueva instancia de CLEAR VALUE de CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Color FLOAT \[ 4 \]

</dd> <dt>

**CD3DX12 \_ CLEAR \_ VALUE(formato DXGI \_ FORMAT, profundidad FLOAT, galería de símbolos UINT8)**
</dt> <dd>

Crea una nueva instancia de CLEAR VALUE de CD3DX12, \_ \_ inicializando los parámetros siguientes:

[**DXGI \_ Formato FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)

Profundidad FLOAT

Galería de símbolos UINT8

</dd> <dt>

**operator const D3D12 \_ CLEAR \_ VALUE&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**D3D12 \_ CLEAR \_ VALUE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

