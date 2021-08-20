---
title: D3DX11_EFFECT_DESC estructura (D3dx11effect.h)
description: Describe un efecto.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC estructura direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_EFFECT_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3f2c3a205a4849aed755bee01302da813cccf77bbf8255036f287d488b76591
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989995"
---
# <a name="d3dx11_effect_desc-structure"></a>D3DX11 \_ EFFECT \_ DESC (estructura)

Describe un efecto.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_EFFECT_DESC {
  UINT ConstantBuffers;
  UINT GlobalVariables;
  UINT InterfaceVariables;
  UINT Techniques;
  UINT Groups;
} D3DX11_EFFECT_DESC;
```



## <a name="members"></a>Miembros

<dl> <dt>

**ConstantBuffers**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de búferes constantes en este efecto.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de variables globales en este efecto.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de interfaces globales en este efecto.

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de técnicas en este efecto.

</dd> <dt>

**Grupos**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de grupos en este efecto.

</dd> </dl>

## <a name="remarks"></a>Comentarios

D3DX11 \_ EFFECT \_ DESC se usa [**con ID3DX11Effect::GetDesc**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

