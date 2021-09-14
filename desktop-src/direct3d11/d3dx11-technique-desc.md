---
title: D3DX11_TECHNIQUE_DESC estructura (D3dx11effect.h)
description: Describe una técnica de efecto.
ms.assetid: 89690a68-d7e8-4f44-9f67-c55d0a400602
keywords:
- D3DX11_TECHNIQUE_DESC estructura direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_TECHNIQUE_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31158b93b8121ac3393e0935cee31c6361b894d5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060866"
---
# <a name="d3dx11_technique_desc-structure"></a>D3DX11 \_ TECHNIQUE \_ DESC (estructura DESC)

Describe una técnica de efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_TECHNIQUE_DESC {
  LPCSTR Name;
  UINT   Passes;
  UINT   Annotations;
} D3DX11_TECHNIQUE_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de esta técnica (NULL si no es anónimo).

</dd> <dt>

**Pasa**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de pases contenidos en la técnica.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotaciones en esta técnica.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 \_ TECHNIQUE \_ DESC se usa [**con ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

