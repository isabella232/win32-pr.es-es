---
title: CD3DX12_CLEAR_VALUE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de valores sin cifrar D3D12 \_ .
ms.assetid: C3E2FAF4-79C4-49CA-B7D3-1FED69C8F7A7
keywords:
- Estructura de CD3DX12_CLEAR_VALUE
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105649389"
---
# <a name="cd3dx12_clear_value-structure"></a>CD3DX12 \_ estructura de valor sin borrar \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ valores sin cifrar D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

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



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ Borrar \_ valor ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ valor Clear de CD3DX12 \_ .

</dd> <dt>

**valor Clear de CD3DX12 explícito \_ \_ (const D3D12 \_ Clear \_ Value &o)**
</dt> <dd>

Crea una nueva instancia de un valor de CD3DX12 \_ Clear \_ , inicializado con el contenido de otra estructura [**D3D12 \_ Clear \_ Value**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value) .

</dd> <dt>

**CD3DX12 \_ Clear \_ Value ( \_ formato de formato de DXGI, const float color \[ 4 \] )**
</dt> <dd>

Crea una nueva instancia de un valor de CD3DX12 \_ Clear \_ , inicializando los siguientes parámetros:

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Color FLOAT \[ 4 \]

</dd> <dt>

**CD3DX12 \_ Clear \_ Value ( \_ formato de formato de DXGI, profundidad de Float, Galería de símbolos UINT8)**
</dt> <dd>

Crea una nueva instancia de un valor de CD3DX12 \_ Clear \_ , inicializando los siguientes parámetros:

[**DXGI \_**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) Formato de formato

Profundidad de FLOAT

Galería de símbolos UINT8

</dd> <dt>

**Operator const D3D12 \_ Clear \_ Value& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**D3D12 \_ Borrar \_ valor**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_clear_value)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

