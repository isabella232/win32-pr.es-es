---
title: D3DX11_EFFECT_SHADER_DESC estructura (D3dx11effect. h)
description: Describe un sombreador de efectos.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c518d4f7930d0651e519d23218121b8ed4bed288
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103914801"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>D3DX11 \_ efecto de la \_ estructura de Descripción del sombreador \_

Describe un sombreador de efectos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_EFFECT_SHADER_DESC {
  const BYTE *pInputSignature;
  BOOL       IsInline;
  const BYTE *pBytecode;
  UINT       BytecodeLength;
  LPCSTR     SODecls[D3D11_SO_STREAM_COUNT];
  UINT       RasterizedStream;
  UINT       NumInputSignatureEntries;
  UINT       NumOutputSignatureEntries;
  UINT       NumPatchConstantSignatureEntries;
} D3DX11_EFFECT_SHADER_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pInputSignature**
</dt> <dd>

Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Se pasa a CreateInputLayout. Solo es válido en un sombreador de vértices o sombreador de geometría. Vea [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**True** si el sombreador está definido en línea; en caso contrario, **false**.

</dd> <dt>

**pBytecode**
</dt> <dd>

Tipo: **const [**byte**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Código de bytes del sombreador.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Longitud de pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Cadena de declaración de salida de flujo (para el sombreador de geometría con el fin de hacerlo).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indica qué secuencia se rasteriza. Los sombreadores de geometría D3D11 pueden generar hasta cuatro flujos de datos, uno de los cuales se puede rasterizar.

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas de la firma de entrada.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas de la firma de salida.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas de la firma de la constante patch.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 \_ Effect \_ Shader \_ desc se usa con [**ID3DX11EffectShaderVariable:: GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

