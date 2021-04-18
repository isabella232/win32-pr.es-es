---
title: CD3DX12_VIEWPORT estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de la ventanilla de D3D12 \_ .
ms.assetid: 1A824F54-596B-450E-A191-B60FBBBB60ED
keywords:
- Estructura de CD3DX12_VIEWPORT
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
ms.openlocfilehash: da29adc50b62bd645070d9667bec1e5c7ce7ab15
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718485"
---
# <a name="cd3dx12_viewport-structure"></a>CD3DX12 (estructura de la \_ ventanilla)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de la [**\_ ventanilla de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport) .

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

**CD3DX12 \_ ventanilla ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ ventanilla CD3DX12.

</dd> <dt>

**ventanilla CD3DX12 explícita \_ (const D3D12 \_ viewport& o)**
</dt> <dd>

Crea una nueva instancia de una ventanilla de CD3DX12 \_ , inicializando los siguientes parámetros:

const D3D12 \_ VIEWPORT& o

</dd> <dt>

**CD3DX12 \_ de ventanilla explícita (float topLeftX, Float Lefty, Float width, Float height, Float minDepth = D3D12 \_ min \_ Depth, Float maxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Crea una nueva instancia de una ventanilla de CD3DX12 \_ , inicializando los siguientes parámetros:

FLOAT topLeftX

FLOAT izquierda

Ancho flotante

Alto de FLOAT

FLOAT minDepth = D3D12 \_ min \_ Depth

FLOAT maxDepth = D3D12 \_ Max \_ Depth

</dd> <dt>

**CD3DX12 \_ de ventanilla explícita (ID3D12Resource \* PreSource, uint mipSlice = 0, Float topLeftX = 0.0 f, Float Lefty = 0.0 f, Float MINDEPTH = D3D12 \_ min \_ Depth, Float maxDepth = D3D12 \_ Max \_ Depth)**
</dt> <dd>

Crea una nueva instancia de una ventanilla de CD3DX12 \_ , inicializando los siguientes parámetros:

\*Código fuente de ID3D12Resource

UINT mipSlice = 0

FLOAT topLeftX = 0.0 f

FLOAT izquierda = 0.0 f

FLOAT minDepth = D3D12 \_ min \_ Depth

FLOAT maxDepth = D3D12 \_ Max \_ Depth

</dd> <dt>

**~ CD3DX12 \_ ventanilla ()**
</dt> <dd>

Destruye una instancia de una ventanilla de D3DX12 \_ .

</dd> <dt>

**Operator const D3D12 \_ VIEWPORT& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Ventanilla de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_viewport)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





