---
title: CD3DX12_RANGE estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una estructura de intervalo de D3D12 \_ .
ms.assetid: 5D5192BF-D14C-487B-A214-F8428E82AF0E
keywords:
- Estructura de CD3DX12_RANGE
topic_type:
- apiref
api_name:
- CD3DX12_RANGE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b6b92cd24a981d48252f5ad457f7ac0320e2d7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718500"
---
# <a name="cd3dx12_range-structure"></a>Estructura de intervalo de CD3DX12 \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RANGE  : public D3D12_RANGE{
   CD3DX12_RANGE();
   explicit CD3DX12_RANGE(const D3D12_RANGE &o);
   CD3DX12_RANGE(SIZE_T begin, SIZE_T end);
   operator const D3D12_RANGE&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Intervalo CD3DX12 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un intervalo de CD3DX12 \_ .

</dd> <dt>

**intervalo de CD3DX12 explícito \_ (const D3D12 \_ Range &o)**
</dt> <dd>

Crea una nueva instancia de un intervalo de CD3DX12 \_ , inicializada con el contenido de otra estructura de [**\_ intervalo de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range) .

</dd> <dt>

**\_Intervalo CD3DX12 (tamaño \_ t inicio, tamaño \_ t final)**
</dt> <dd>

Crea una nueva instancia de un intervalo de CD3DX12 \_ , inicializando los siguientes parámetros:

TAMAÑO \_ T Inicio

TAMAÑO \_ T final

</dd> <dt>

**Operator const D3D12 \_ RANGE& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Intervalo D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_range)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





