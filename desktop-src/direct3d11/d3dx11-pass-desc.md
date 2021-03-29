---
title: D3DX11_PASS_DESC estructura (D3dx11effect. h)
description: Describe un paso de efecto, que contiene el estado de la canalización.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC estructura de Direct3D 11
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987204"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11 \_ Pass \_ DESC (estructura)

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



## <a name="members"></a>Miembros

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de este paso (**null** si no es anónimo).

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotaciones de este paso.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Tipo: **[ **byte**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Signatura del sombreador de vértices o del sombreador de geometría (si no hay ningún sombreador de vértices) o **null** si no existe ninguno.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Tipo: **[ **tamaño \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Tamaño de Singature en bytes.

</dd> <dt>

**StencilRef**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

El valor de referencia de la galería de símbolos usado en el estado de la galería de símbolos de profundidad.

</dd> <dt>

**SampleMask**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

La máscara de ejemplo para el estado de Blend.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Tipo: **[ **float**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Factores de mezcla por componente (RGBA) para el estado de Blend.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 \_ Pass \_ desc se usa con [**ID3DX11EffectPass:: GetDesc**](id3dx11effectpass-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

