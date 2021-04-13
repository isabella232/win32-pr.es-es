---
description: Finaliza un paso activo.
ms.assetid: e20b3e0f-db9f-48e8-ab4e-761a5861f3ce
title: 'ID3DXEffect:: EndPass (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.EndPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 5cdba799f282e56bbe4565a4792906fd835e5c6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362601"
---
# <a name="id3dxeffectendpass-method"></a>ID3DXEffect:: EndPass (método)

Finaliza un paso activo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EndPass();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Este método siempre devuelve el valor S \_ correcto.

## <a name="remarks"></a>Observaciones

Una aplicación señala el final de la representación de un paso activo mediante una llamada a **ID3DXEffect:: EndPass**. Cada **ID3DXEffect:: EndPass** debe formar parte de un par coincidente de las llamadas a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) y **ID3DXEffect:: EndPass** .

Cada par coincidente de las llamadas a [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) y **ID3DXEffect:: EndPass** debe encontrarse dentro de un par coincidente de [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) y [**ID3DXEffect:: end**](id3dxeffect--end.md) calls.

Si la aplicación cambia cualquier estado de efecto mediante cualquiera de los métodos [**Effect:: setx**](id3dxeffect.md) dentro de un par de coincidencia [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) / **ID3DXEffect:: EndPass** , la aplicación debe llamar a [**ID3DXEffect:: commitChanges**](id3dxeffect--commitchanges.md) antes de cualquier llamada a DrawxPrimitive para propagar los cambios de estado en el dispositivo antes de la representación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> </dl>

 

 




