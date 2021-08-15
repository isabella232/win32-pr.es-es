---
title: D3DX11_PASS_SHADER_DESC estructura (D3dx11effect.h)
description: Describe un paso de efecto.
ms.assetid: 4676ad80-1b21-4e8b-8cec-f530ef0b9fd7
keywords:
- D3DX11_PASS_SHADER_DESC estructura direct3D 11
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
ms.openlocfilehash: 8ec7328ce346b51c3315086dcc193f421081dd77fc3a169bc448fba10bc7fa3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118536848"
---
# <a name="d3dx11_pass_shader_desc-structure"></a>D3DX11 \_ PASS \_ SHADER \_ DESC (estructura DESC)

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

Variable de la que provenía este sombreador.

</dd> <dt>

**ShaderIndex**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Elemento de pShaderVariable (si es una matriz) o 0 si no es aplicable.

</dd> </dl>

## <a name="remarks"></a>Comentarios

D3DX11 PASS SHADER DESC se usa con los métodos \_ \_ \_ [**ID3DX11EffectPass**](id3dx11effectpass.md) Get \* ShaderDesc.

Si se trata de una asignación de sombreador en línea, la interfaz devuelta será una variable de sombreador anónima, que no se puede recuperar de ninguna otra manera. Su nombre en la descripción de la variable será "$Anonymous". Si no hay ninguna asignación de este tipo en el bloque de paso, pShaderVariable != **NULL**, pero pShaderVariable->IsValid() == **FALSE**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

