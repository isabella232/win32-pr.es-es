---
description: Obtiene el administrador de estado del efecto.
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: Método ID3DXEffect::GetStateManager (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 6700447485d83f2610149b809065ab02140a2e6cf068508b6571d5132844fb0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121646"
---
# <a name="id3dxeffectgetstatemanager-method"></a>Método ID3DXEffect::GetStateManager

Obtiene el administrador de estado del efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppManager* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***

Devuelve un puntero al administrador de estado. Vea [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Comentarios

[**ID3DXEffectStateManager es**](id3dxeffectstatemanager.md) una interfaz implementada por el usuario que ofrece devoluciones de llamada en una aplicación para establecer el estado del dispositivo a partir de un efecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXEffect](id3dxeffect.md)
</dt> <dt>

[**ID3DXEffect::SetStateManager**](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




