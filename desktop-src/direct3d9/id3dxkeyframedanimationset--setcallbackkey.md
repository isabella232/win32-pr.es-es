---
description: Establece información sobre una devolución de llamada específica en el conjunto de animaciones.
ms.assetid: 899f3a85-c878-4eeb-8bda-fc4e9083bd1f
title: 'ID3DXKeyframedAnimationSet:: SetCallbackKey (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.SetCallbackKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49d3373e0ab0fa221e707ca6eda9ac9bb468a5a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280485"
---
# <a name="id3dxkeyframedanimationsetsetcallbackkey-method"></a>ID3DXKeyframedAnimationSet:: SetCallbackKey (método)

Establece información sobre una devolución de llamada específica en el conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetCallbackKey(
  [in]  UINT               Animation,
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Animación* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de animación.

</dd> <dt>

*pCallbackKeys* \[ enuncia\]
</dt> <dd>

Tipo: **[ **\_ devolución de llamada LPD3DXKEY**](d3dxkey-callback.md)**

Puntero a la [**función de devolución de llamada**](d3dxkey-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
