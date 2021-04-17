---
title: CD3DX12_SHADER_BYTECODE estructura (D3dx12. h)
description: Una estructura auxiliar para habilitar la inicialización sencilla de una \_ estructura de código de bytes del sombreador D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Estructura de CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717597"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>CD3DX12 \_ estructura de código de byte del sombreador \_

Una estructura auxiliar para habilitar la inicialización sencilla de una estructura de [**\_ código de \_ bytes del sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

## <a name="syntax"></a>Sintaxis


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>Miembros

<dl> <dt>

**\_ \_ Código de bytes del sombreador CD3DX12 ()**
</dt> <dd>

Crea una nueva instancia no inicializada de un \_ código de bytes de sombreador CD3DX12 \_ .

</dd> <dt>

**código de \_ bytes del sombreador CD3DX12 explícito \_ (const D3D12 \_ sombreador de \_ bytes &o)**
</dt> <dd>

Crea una nueva instancia de un \_ código de bytes de sombreador CD3DX12 \_ , inicializada con el contenido de otra estructura de [**código de \_ \_ bytes del sombreador de D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**\_Código de bytes del sombreador de CD3DX12 \_ (ID3DBlob \* pShaderBlob)**
</dt> <dd>

Crea una nueva instancia de un \_ código de bytes de sombreador CD3DX12 \_ , inicializando los siguientes parámetros:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**\_ \_ Código de bytes del sombreador CD3DX12 (const void \* \_ PShaderBytecode, size \_ T bytecodeLength)**
</dt> <dd>

Crea una nueva instancia de un \_ código de bytes de sombreador CD3DX12 \_ , inicializando los siguientes parámetros:

void \* \_ pShaderBytecode

TAMAÑO \_ T bytecodeLength

</dd> <dt>

**operador const D3D12 \_ código de \_ byte del sombreador& () Const**
</dt> <dd>

Define el & operador de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Código de bytes del sombreador D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

