---
title: D3DX11_PASS_DESC estructura (D3dx11effect.h)
description: Describe un paso de efecto, que contiene el estado de canalización.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC estructura direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f00cc28e6ab901073e30abd2554046d61144c42af2217869c0b87dc6c19d29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124950"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11 \_ PASS \_ DESC (estructura)

Describe un paso de efecto, que contiene el estado de canalización.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de este paso **(NULL si** no es anónimo).

</dd> <dt>

**anotaciones**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotaciones en este paso.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Tipo: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Firma del sombreador de vértices o del sombreador de geometría (si no hay ningún sombreador de vértices) o **NULL** si no existe ninguno.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Tipo: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño de la singature en bytes.

</dd> <dt>

**StencilRef**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de referencia de galería de símbolos usado en el estado de galería de símbolos de profundidad.

</dd> <dt>

**SampleMask**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Máscara de ejemplo para el estado de mezcla.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Tipo: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Factores de combinación por componente (RGBA) para el estado de mezcla.

</dd> </dl>

## <a name="remarks"></a>Comentarios

D3DX11 \_ PASS \_ DESC se usa [**con ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

