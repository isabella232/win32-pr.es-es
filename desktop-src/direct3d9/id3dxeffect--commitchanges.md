---
description: Propaga los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.
ms.assetid: 3a779b63-c106-4a81-afeb-82bd6e556de4
title: 'ID3DXEffect:: CommitChanges (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: 41516c52b29dfe277cc857e44003de7783282a3a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280351"
---
# <a name="id3dxeffectcommitchanges-method"></a>ID3DXEffect:: CommitChanges (método)

Propaga los cambios de estado que se producen dentro de un paso activo al dispositivo antes de la representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CommitChanges();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**ID3DXEffect:: setx**](id3dxeffect.md) dentro de un par de coincidencia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) , la aplicación debe llamar a **ID3DXEffect:: commitChanges** antes de cualquier llamada a DrawxPrimitive para propagar los cambios de estado en el dispositivo antes de la representación. Si no se produce ningún cambio de estado dentro de un par de coincidencia **ID3DXEffect:: BeginPass** y **ID3DXEffect:: EndPass** , no es necesario llamar a **ID3DXEffect:: commitChanges**.

Esto es ligeramente diferente para los parámetros compartidos de un efecto clonado. Cuando una técnica está activa en un efecto clonado (es decir, cuando se ha llamado a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) pero no se ha llamado a [**ID3DXEffect:: end**](id3dxeffect--end.md) ), **ID3DXEffect:: commitChanges** actualiza los parámetros que no se comparten según lo esperado. Para actualizar un parámetro compartido (solo para un efecto clonado cuya técnica está activa), llame a **ID3DXEffect:: end** para desactivar la técnica y **ID3DXEffect:: Begin** para reactivar la técnica antes de llamar a **ID3DXEffect:: commitChanges**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




