---
description: Rellena una matriz con los datos de clave de escala que se usan para la animación de fotogramas clave.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: 'ID3DXKeyframedAnimationSet:: GetScaleKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 88c907bc9b45b1203917b092f565096be3ed1fb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718469"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>ID3DXKeyframedAnimationSet:: GetScaleKeys (método)

Rellena una matriz con los datos de clave de escala que se usan para la animación de fotogramas clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Animación* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de animación.

</dd> <dt>

*pScaleKeys* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntero a una matriz asignada por el usuario de vectores de [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método va a rellenar con datos de escala de animación.

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
