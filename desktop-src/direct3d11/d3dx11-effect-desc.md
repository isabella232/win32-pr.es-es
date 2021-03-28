---
title: D3DX11_EFFECT_DESC estructura (D3dx11effect. h)
description: Describe un efecto.
ms.assetid: 2efde608-26e0-4234-92d8-dc3ef2a29d89
keywords:
- D3DX11_EFFECT_DESC estructura de Direct3D 11
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
ms.openlocfilehash: 4d43b37d13a8b3f076cc3c5967dac9a95ed18a5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104987229"
---
# <a name="d3dx11_effect_desc-structure"></a>D3DX11 \_ Effect ( \_ estructura de DESC)

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de búferes de constantes en este efecto.

</dd> <dt>

**GlobalVariables**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de variables globales en este efecto.

</dd> <dt>

**InterfaceVariables**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de interfaces globales en este efecto.

</dd> <dt>

**Descrita**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de técnicas de este efecto.

</dd> <dt>

**Grupos**
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de grupos en este efecto.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 \_ efecto \_ desc se usa con [**ID3DX11Effect:: GetDesc**](id3dx11effect-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Effects 11 estructuras](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

