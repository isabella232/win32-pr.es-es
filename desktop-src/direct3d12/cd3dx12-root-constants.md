---
title: CD3DX12_ROOT_CONSTANTS estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ \_ CONSTANTS RAÍZ D3D12.
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- CD3DX12_ROOT_CONSTANTS estructura
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_CONSTANTS
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ece9dade9bd1e833657c26d84d426d04a63ebce786280b3d76f21e10bc07b3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118098478"
---
# <a name="cd3dx12_root_constants-structure"></a>Estructura DE CONSTANTES \_ RAÍZ CD3DX12 \_

Estructura auxiliar para permitir la inicialización sencilla de una estructura [**\_ \_ CONSTANTS RAÍZ D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_ROOT_CONSTANTS  : public D3D12_ROOT_CONSTANTS{
       CD3DX12_ROOT_CONSTANTS();
       explicit CD3DX12_ROOT_CONSTANTS(const D3D12_ROOT_CONSTANTS &o);
       CD3DX12_ROOT_CONSTANTS(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void inline Init(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
  void static inline Init(D3D12_ROOT_CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0);
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**CD3DX12 \_ ROOT \_ CONSTANTS()**
</dt> <dd>

Crea una nueva instancia sin inicializar de una CONSTANTE RAÍZ CD3DX12. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ ROOT \_ CONSTANTS(const D3D12 \_ ROOT \_ CONSTANTS &o)**
</dt> <dd>

Crea una nueva instancia de CD3DX12 ROOT CONSTANTS, inicializada con el contenido de otra estructura \_ \_ [**D3D12 \_ ROOT \_ CONSTANTS.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)

</dd> <dt>

**CD3DX12 \_ ROOT \_ CONSTANTS(UINT num32BitValues, sombreador UINTRegister, UINT registerSpace = 0)**
</dt> <dd>

Crea una nueva instancia de CD3DX12 \_ ROOT \_ CONSTANTS, inicializando los parámetros siguientes:

UINT num32BitValues

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

</dd> <dt>

**inline Init(UINT num32BitValues, sombreador UINTRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT num32BitValues

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

</dd> <dt>

**static inline Init(D3D12 \_ ROOT \_ CONSTANTS &rootConstants, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ ROOT \_ CONSTANTS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants

UINT num32BitValues

Sombreador UINTRegistrar

(opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONSTANTES RAÍZ D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





