---
title: CD3DX12_VIEWPORT estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura VIEWPORT D3D12. \_
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- CD3DX12_VIEWPORT estructura
topic_type:
- apiref
api_name:
- CD3DX12_VIEWPORT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dce5a009dba6b047b599772586db60a022f4c62126a6d58575166b5ca2bec5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808277"
---
# <a name="cd3dx12_viewport-structure"></a>Estructura DE VENTANILLA DE CD3DX12 \_

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ VIEWPORT D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_VIEWPORT  : public D3D12_VIEWPORT{
   CD3DX12_VIEWPORT();
   explicit CD3DX12_VIEWPORT(const D3D12_VIEWPORT& o);
   explicit CD3DX12_VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   explicit CD3DX12_VIEWPORT(ID3D12Resource* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12_MIN_DEPTH, FLOAT maxDepth = D3D12_MAX_DEPTH);
   ~CD3DX12_VIEWPORT();
   operator const D3D12_VIEWPORT&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ VIEWPORT()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una VENTANILLA CD3DX12. \_

</dd> <dt>

**explicit CD3DX12 \_ VIEWPORT(const D3D12 \_ VIEWPORT& o)**
</dt> <dd>

Crea una nueva instancia de UNA VENTANILLA CD3DX12, \_ inicializando los parámetros siguientes:

const D3D12 \_ VIEWPORT& o

</dd> <dt>

**EXPLICIT CD3DX12 \_ VIEWPORT(FLOAT topLeftX, FLOAT topLeftY, FLOAT width, FLOAT height, FLOAT minDepth = D3D12 \_ MIN \_ DEPTH, FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH)**
</dt> <dd>

Crea una nueva instancia de UNA VENTANILLA CD3DX12, \_ inicializando los parámetros siguientes:

FLOAT topLeftX

FLOAT topLeftY

Ancho float

Alto float

FLOAT minDepth = D3D12 \_ MIN \_ DEPTH

FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH

</dd> <dt>

**explicit CD3DX12 \_ VIEWPORT(ID3D12Resource \* pResource, UINT mipSlice = 0, FLOAT topLeftX = 0.0f, FLOAT topLeftY = 0.0f, FLOAT minDepth = D3D12 \_ MIN \_ DEPTH, FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH)**
</dt> <dd>

Crea una nueva instancia de UNA VENTANILLA CD3DX12, \_ inicializando los parámetros siguientes:

ID3D12Resource \* pResource

UINT mipSlice = 0

FLOAT topLeftX = 0,0f

FLOAT topLeftY = 0,0f

FLOAT minDepth = D3D12 \_ MIN \_ DEPTH

FLOAT maxDepth = D3D12 \_ MAX \_ DEPTH

</dd> <dt>

**~CD3DX12 \_ VIEWPORT()**
</dt> <dd>

Destruye una instancia de una ventanilla D3DX12. \_

</dd> <dt>

**operator const D3D12 \_ VIEWPORT&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**VENTANILLA D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





