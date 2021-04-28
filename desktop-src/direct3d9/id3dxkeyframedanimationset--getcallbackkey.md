---
description: 'Método ID3DXKeyframedAnimationSet::GetCallbackKey: obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.'
ms.assetid: a1d3ca96-2852-420a-aa5c-a434970e5523
title: Método ID3DXKeyframedAnimationSet::GetCallbackKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f3ebbf93bd482a2259ffdaaf272c65b5e86d5270
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090323"
---
# <a name="id3dxkeyframedanimationsetgetcallbackkey-method"></a>Método ID3DXKeyframedAnimationSet::GetCallbackKey

Obtiene información sobre una devolución de llamada específica en el conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Animación* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de animación.

</dd> <dt>

*pCallbackKeys* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md)**

Puntero a la [**función de devolución de llamada**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
