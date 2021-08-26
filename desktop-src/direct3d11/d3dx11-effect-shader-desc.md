---
title: D3DX11_EFFECT_SHADER_DESC estructura (D3dx11effect.h)
description: Describe un sombreador de efectos.
ms.assetid: 4377eec6-f331-4cad-bf16-189d6296f886
keywords:
- D3DX11_EFFECT_SHADER_DESC estructura Direct3D 11
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
ms.openlocfilehash: b48695b2e6ff0cca2046606eaad7dbdf137641ce126bd4f5f211e399aaf29d39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096355"
---
# <a name="d3dx11_effect_shader_desc-structure"></a>Estructura \_ \_ DESC DEL SOMBREADOR DE EFECTO D3DX11 \_

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

Tipo: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Se pasa a CreateInputLayout. Solo es válido en un sombreador de vértices o un sombreador de geometría. Vea [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout).

</dd> <dt>

**IsInline**
</dt> <dd>

Tipo: **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

**TRUE** es que el sombreador se define en línea; en caso **contrario, FALSE**.

</dd> <dt>

**pBytecode**
</dt> <dd>

Tipo: **const [**BYTE**](/windows/desktop/WinProg/windows-data-types) \***

</dd> <dd>

Código de bytes del sombreador.

</dd> <dt>

**BytecodeLength**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Longitud de pBytecode.

</dd> <dt>

**SODecls**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Transmitir la cadena de declaración (para el sombreador de geometría con SO).

</dd> <dt>

**RasterizedStream**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Indica qué secuencia está rasterizada. Los sombreadores de geometría D3D11 pueden generar hasta cuatro flujos de datos, uno de los cuales se puede rasterizar.

</dd> <dt>

**NumInputSignatureEntries**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas de la firma de entrada.

</dd> <dt>

**NumOutputSignatureEntries**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas en la firma de salida.

</dd> <dt>

**NumPatchConstantSignatureEntries**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de entradas de la firma de constante de revisión.

</dd> </dl>

## <a name="remarks"></a>Comentarios

D3DX11 EFFECT SHADER DESC se usa \_ \_ con \_ [**ID3DX11EffectShaderVariable::GetShaderDesc**](id3dx11effectshadervariable-getshaderdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

