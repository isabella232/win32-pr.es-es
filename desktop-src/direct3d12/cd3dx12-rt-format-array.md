---
title: CD3DX12_RT_FORMAT_ARRAY estructura (D3dx12.h)
description: Una estructura auxiliar para permitir la inicialización sencilla de una estructura de matriz D3D12 \_ RT \_ \_ FORMAT.
ms.assetid: E890DD33-599F-4B20-BD15-2734867788E5
keywords:
- CD3DX12_RT_FORMAT_ARRAY estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566177"
---
# <a name="cd3dx12_rt_format_array-structure"></a>Estructura de MATRIZ DE FORMATO DE CD3DX12 \_ RT \_ \_

Una estructura auxiliar para permitir la inicialización sencilla de una [**estructura de matriz D3D12 \_ RT \_ FORMAT. \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_RT_FORMAT_ARRAY  : public D3D12_RT_FORMAT_ARRAY{
  CD3DX12_RT_FORMAT_ARRAY CD3DX12_RT_FORMAT_ARRAY();
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const D3D12_RT_FORMAT_ARRAY& o);
  CD3DX12_RT_FORMAT_ARRAY explicit CD3DX12_RT_FORMAT_ARRAY(const DXGI_FORMAT* pFormats, UINT NumFormats);
                          operator const D3D12_RT_FORMAT_ARRAY&() const;
};
```



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ RT \_ FORMAT \_ ARRAY()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una MATRIZ DE FORMATO DE CD3DX12 \_ \_ \_ RT.

</dd> <dt>

**explicit CD3DX12 \_ RT \_ FORMAT \_ ARRAY(const D3D12 \_ RT FORMAT ARRAY& \_ \_ o)**
</dt> <dd>

Crea una nueva instancia de cd3DX12 RT FORMAT ARRAY, inicializada con valores copiados de una estructura \_ \_ \_ [**D3D12 \_ RT \_ FORMAT \_ ARRAY.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)

</dd> <dt>

**explicit CD3DX12 \_ RT \_ FORMAT \_ ARRAY(const DXGI \_ FORMAT \* pFormats, UINT NumFormats)**
</dt> <dd>

Crea una nueva instancia de cd3DX12 RT FORMAT ARRAY, inicializada con los \_ \_ valores \_ pasados en la lista de parámetros. El contenido de la matriz especificada por el *parámetro pFormats* se copia en la matriz miembro **RTFormats**. Se supone que la matriz especificada por *pFormats* tiene el mismo tamaño que **RTFormats.**

</dd> <dt>

**operator const D3D12 \_ RT \_ FORMAT ARRAY \_&() const**
</dt> <dd>

Conversión implícita a una estructura de MATRIZ DE FORMATO RT de [**D3D12 \_ \_ \_ RT.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array) Dado que D3D12 RT FORMAT ARRAY es el tipo subyacente de \_ \_ \_ CD3DX12 \_ DEPTH STENCIL DESC1, el objeto simplemente se devuelve como una referencia \_ \_ const D3D12 RT FORMAT ARRAY a \_ \_ \_ sí mismo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> <dt>

[**MATRIZ DE FORMATO D3D12 \_ RT \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rt_format_array)
</dt> </dl>

 

 





