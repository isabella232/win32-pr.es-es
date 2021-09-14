---
title: D3DX11_GROUP_DESC estructura (D3dx11effect.h)
description: Describe un grupo de efectos.
ms.assetid: 9d4dd5f6-76a5-456d-b464-131b89953ef1
keywords:
- D3DX11_GROUP_DESC estructura direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_GROUP_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431daf0a14a465ee3533f1497278ddcd85b08a79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060882"
---
# <a name="d3dx11_group_desc-structure"></a>D3DX11 \_ GROUP \_ DESC (estructura)

Describe un grupo de efectos.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _D3DX11_GROUP_DESC {
  LPCSTR Name;
  UINT   Techniques;
  UINT   Annotations;
} D3DX11_GROUP_DESC;
```



## <a name="members"></a>Members

<dl> <dt>

**Nombre**
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Nombre de este grupo (solo **NULL si** es global).

</dd> <dt>

**Técnicas**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de técnicas contenidas en el grupo.

</dd> <dt>

**Anotaciones**
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Número de anotaciones de este grupo.

</dd> </dl>

## <a name="remarks"></a>Observaciones

D3DX11 \_ GROUP DESC se usa con \_ [**ID3DX11EffectTechnique::GetDesc**](id3dx11effecttechnique-getdesc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|-------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Estructuras de efectos 11](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

