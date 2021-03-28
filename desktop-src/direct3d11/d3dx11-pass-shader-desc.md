---
title: D3DX11_PASS_SHADER_DESC estructura (D3dx11effect. h)
description: Describe un paso de efecto.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC estructura de Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_SHADER_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cac6e842dabeaabc60451737fae56eb2cb61915
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987199"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>D3DX11 \_ ( \_ estructura de Desc del sombreador de paso) \_

Describe un paso de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_PASS_SHADER_DESC {
  ID3DX11EffectShaderVariable *pShaderVariable;
  UINT                        ShaderIndex;
} D3DX11_PASS_SHADER_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pShaderVariable**
</dt> <dd>

Tipo: **[ **ID3DX11EffectShaderVariable**](id3dx11effectshadervariable.md)\***

</dd> <dd>

Variable de la que procede este sombreador.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Elemento de pShaderVariable (si es una matriz) o 0 si no es aplicable.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 \_ Pass \_ Shader \_ desc se usa con los métodos [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc.

Si se trata de una asignación de sombreador en línea, la interfaz devuelta será una variable de sombreador anónima, que no se puede recuperar de ninguna otra manera. Su nombre en la descripción de la variable será "$Anonymous". Si no hay ninguna asignación de este tipo en el bloque Pass, pShaderVariable! = **null**, pero pShaderVariable->IsValid () = = **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

