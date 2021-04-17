---
title: CD3DX12_ROOT_CONSTANTS estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de constantes raíz D3D12 \_ .
ms.assetid: 2F517DCE-BC0C-4678-9C25-D826036F99A8
keywords:
- Estructura de CD3DX12_ROOT_CONSTANTS
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
ms.openlocfilehash: a7a1f81a429b083400adad60f316cc90c4ede1d9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717604"
---
# <a name="cd3dx12_root_constants-structure"></a>CD3DX12 \_ \_ estructura de constantes raíz

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ \_ constantes raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

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

**\_Constantes raíz CD3DX12 \_ ()**
</dt> <dd>

Crea una nueva instancia no inicializada de una \_ constante raíz CD3DX12 \_ .

</dd> <dt>

**constantes de raíz CD3DX12 explícitas \_ \_ (constantes de raíz const D3D12 \_ \_ &o)**
</dt> <dd>

Crea una nueva instancia de una \_ constante raíz CD3DX12 \_ , inicializada con el contenido de otra estructura [**de \_ \_ constantes raíz D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) .

</dd> <dt>

**\_Constantes raíz CD3DX12 \_ (uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Crea una nueva instancia de una \_ constante CD3DX12 raíz \_ , inicializando los parámetros siguientes:

UINT num32BitValues

UINT shaderRegister

rechace UINT registerSpace = 0

</dd> <dt>

**Init en línea (UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

UINT num32BitValues

UINT shaderRegister

rechace UINT registerSpace = 0

</dd> <dt>

**Init inline init (D3D12 \_ root \_ constants &ROOTCONSTANTS, uint NUM32BITVALUES, uint SHADERREGISTER, uint registerSpace = 0)**
</dt> <dd>

Especifica una función que inicializa los parámetros siguientes:

[**D3D12 \_ \_Constantes raíz**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants) &rootConstants

UINT num32BitValues

UINT shaderRegister

rechace UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Constantes raíz \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_constants)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





