---
title: CD3DX12_SHADER_BYTECODE estructura (D3dx12.h)
description: Estructura auxiliar para permitir la inicialización sencilla de una estructura \_ \_ BYTECODE de SOMBREADOR D3D12.
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- CD3DX12_SHADER_BYTECODE estructura
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566176"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>Estructura BYTECODE del SOMBREADOR CD3DX12 \_ \_

Estructura auxiliar para permitir la inicialización sencilla de una [**estructura \_ \_ BYTECODE de SOMBREADOR D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

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



## <a name="members"></a>Members

<dl> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE()**
</dt> <dd>

Crea una nueva instancia sin inicializar de un CÓDIGO DE BYTES DE SOMBREADOR CD3DX12. \_ \_

</dd> <dt>

**EXPLICIT CD3DX12 \_ SHADER \_ BYTECODE(const D3D12 \_ SHADER \_ BYTECODE &o)**
</dt> <dd>

Crea una nueva instancia de UN CÓDIGO DE BYTES DE SOMBREADOR CD3DX12, inicializado con el contenido de otra estructura \_ \_ [**\_ \_ BYTECODE del SOMBREADOR D3D12.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE(ID3DBlob \* pShaderBlob)**
</dt> <dd>

Crea una nueva instancia de UN SOMBREADOR CD3DX12 \_ \_ BYTECODE, inicializando los parámetros siguientes:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE(const void \* \_ pShaderBytecode, SIZE \_ T bytecodeLength)**
</dt> <dd>

Crea una nueva instancia de UN SOMBREADOR CD3DX12 \_ \_ BYTECODE, inicializando los parámetros siguientes:

void \* \_ pShaderBytecode

SIZE \_ T bytecodeLength

</dd> <dt>

**operator const D3D12 \_ SHADER \_ BYTECODE&() const**
</dt> <dd>

Define el & de paso por referencia para el tipo de estructura primaria.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CÓDIGO DE BYTES DEL SOMBREADOR D3D12 \_ \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Estructuras auxiliares de D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

