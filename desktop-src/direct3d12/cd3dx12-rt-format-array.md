---
title: CD3DX12_RT_FORMAT_ARRAY estructura (D3dx12. h)
description: Estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de \_ matriz de formato D3D12 RT \_ .
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- Estructura de CD3DX12_RT_FORMAT_ARRAY
topic_type:
- apiref
api_name:
- CD3DX12_RT_FORMAT_ARRAY
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c05b7ae9e51d2d6b2a43f45dc83bda2074f6b734
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718486"
---
# <a name="cd3dx12_rt_format_array-structure"></a>Estructura de la matriz de formato CD3DX12 \_ RT \_ \_

Estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_Matriz de formato CD3DX12 RT \_ \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ matriz de formato RT de CD3DX12 \_ \_ .

</dd> <dt>

**matriz de \_ formato RT CD3DX12 explícita \_ \_ (const D3D12 \_ RT \_ format \_ array& o)**
</dt> <dd>

Crea una nueva instancia de una \_ matriz de formato CD3DX12 RT \_ \_ , inicializada con los valores copiados de una estructura de [**\_ \_ \_ matriz de formato D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) .

</dd> <dt>

**matriz de \_ formato RT CD3DX12 explícita \_ \_ (const DXGI \_ format \* pFormats, uint NumFormats)**
</dt> <dd>

Crea una nueva instancia de una \_ matriz de formato CD3DX12 RT \_ \_ , inicializada con los valores pasados en la lista de parámetros. El contenido de la matriz especificado por el parámetro *pFormats* se copia en la matriz de miembros **RTFormats**. Se supone que la matriz especificada por *pFormats* tiene el mismo tamaño que **RTFormats**.

</dd> <dt>

**Operator const D3D12 \_ RT \_ FORMAT \_ array& () Const**
</dt> <dd>

Conversión implícita a una estructura de [**\_ matriz de \_ formato \_ D3D12 RT**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) . Dado que \_ \_ \_ la matriz de formato D3D12 RT es el tipo subyacente de la \_ Galería de símbolos de profundidad CD3DX12 \_ \_ DESC1, el objeto simplemente se devuelve como una referencia de matriz de formato const D3D12 \_ RT \_ \_ a sí misma.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**\_Matriz de \_ formato D3D12 RT \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





