---
description: Rellena una matriz con datos de clave de escala utilizados para la animación de fotogramas clave.
ms.assetid: 0d595510-6d8c-4bc9-b5ca-0d6f73be3439
title: Método ID3DXKeyframedAnimationSet::GetScaleKeys (D3dx9anim.h)
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
ms.openlocfilehash: 1158195ae84f8215869571fc400950a6dfd475fc37050572ffb5e3e77f96d719
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493515"
---
# <a name="id3dxkeyframedanimationsetgetscalekeys-method"></a>Método ID3DXKeyframedAnimationSet::GetScaleKeys

Rellena una matriz con datos de clave de escala utilizados para la animación de fotogramas clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetScaleKeys(
  [in] UINT              Animation,
  [in] LPD3DXKEY_VECTOR3 pScaleKeys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Animación* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de animación.

</dd> <dt>

*pScaleKeys* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntero a una matriz asignada por el usuario de vectores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método va a rellenar con datos de escala de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumScaleKeys**](id3dxkeyframedanimationset--getnumscalekeys.md)
</dt> </dl>

 

 
