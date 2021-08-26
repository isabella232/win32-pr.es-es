---
description: Propagar los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: Método ID3DXEffect::CommitChanges (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CommitChanges
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5b81cd2674e08473358e031b827528121537264df11dba54c6a1f610ac054ee4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951765"
---
# <a name="id3dxeffectcommitchanges-method"></a>Método ID3DXEffect::CommitChanges

Propagar los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**ID3DXEffect::Setx**](id3dxeffect.md) dentro de un par de coincidencias [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect::EndPass,**](id3dxeffect--endpass.md) la aplicación debe llamar a **ID3DXEffect::CommitChanges** antes de cualquier llamada DrawxPrimitive para propagar los cambios de estado al dispositivo antes de la representación. Si no se produce ningún cambio de estado dentro de un par de **coincidencias ID3DXEffect::BeginPass** e **ID3DXEffect::EndPass,** no es necesario llamar a **ID3DXEffect::CommitChanges**.

Esto es ligeramente diferente para cualquier parámetro compartido en un efecto clonado. Cuando una técnica está activa en un efecto clonado (es decir, cuando se ha llamado a [**ID3DXEffect::Begin**](id3dxeffect--begin.md) pero no se ha llamado a [**ID3DXEffect::End),**](id3dxeffect--end.md) **ID3DXEffect::CommitChanges** actualiza los parámetros que no se comparten según lo previsto. Para actualizar un parámetro compartido (solo para un efecto clonado cuya técnica está activa), llame a **ID3DXEffect::End** para desactivar la técnica e **ID3DXEffect::Begin** para reactivar la técnica antes de llamar a **ID3DXEffect::CommitChanges**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




