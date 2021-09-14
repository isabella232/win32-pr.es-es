---
title: D3DX11_PASS_DESC estructura (D3dx11effect.h)
description: Describe un paso de efecto, que contiene el estado de la canalización.
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
ms.openlocfilehash: 5b4d7f10268db0515b2f7e3772332b34427ba67a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060872"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11 \_ PASS \_ DESC (estructura)

Describe un paso de efecto, que contiene el estado de la canalización.

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



## <a name="members"></a>Members

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de este paso **(NULL si no** es anónimo).

</dd> <dt>

**Anotaciones**
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

Tamaño de singature en bytes.

</dd> <dt>

**StencilRef**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Valor de referencia de galería de símbolos usado en el estado de galería de símbolos de profundidad.

</dd> <dt>

**Máscara de ejemplo**
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

## <a name="remarks"></a>Observaciones

D3DX11 \_ PASS \_ DESC se usa [**con ID3DX11EffectPass::GetDesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

