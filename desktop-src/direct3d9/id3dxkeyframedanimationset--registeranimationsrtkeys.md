---
description: Registre los datos de fotogramas clave de escala, rotación y traducción (SRT) de una animación.
ms.assetid: 10e5b391-1529-4952-abbb-ef560a35d667
title: Método ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.RegisterAnimationSRTKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07ec4db0bb02eb0a177375fc37af67264f1368b2ab952c0b170580112e4dbf40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987375"
---
# <a name="id3dxkeyframedanimationsetregisteranimationsrtkeys-method"></a>Método ID3DXKeyframedAnimationSet::RegisterAnimationSRTKeys

Registre los datos de fotogramas clave de escala, rotación y traducción (SRT) de una animación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT RegisterAnimationSRTKeys(
  [in]        LPCSTR               pName,
  [in]        UINT                 NumScaleKeys,
  [in]        UINT                 NumRotationKeys,
  [in]        UINT                 NumTranslationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pScaleKeys,
  [in]  const LPD3DXKEY_QUATERNION *pRotationKeys,
  [in]  const LPD3DXKEY_VECTOR3    *pTranslationKeys,
  [out]       DWORD                *pAnimationIndex
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre de animación.

</dd> <dt>

*NumScaleKeys* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de claves de escalado.

</dd> <dt>

*NumRotationKeys* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de claves de rotación.

</dd> <dt>

*NumTranslationKeys* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de claves de traducción.

</dd> <dt>

*pScaleKeys* \[ En\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Dirección de un puntero a una matriz asignada por el usuario de vectores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método rellena con datos de escala.

</dd> <dt>

*pRotationKeys* \[ En\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ QUATERNION**](d3dxkey-quaternion.md) \***

Dirección de un puntero a una matriz asignada por el usuario de [**\_ cuaterniones D3DXKEY QUATERNION**](d3dxkey-quaternion.md) que el método rellena con datos de rotación.

</dd> <dt>

*pTranslationKeys* \[ En\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) \***

Dirección de un puntero a una matriz asignada por el usuario de vectores [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md) que el método rellena con datos de traducción.

</dd> <dt>

*pAnimationIndex* \[ out\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Devuelve el índice de animación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor: D3DERR \_ INVALIDCALL

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
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumRotationKeys**](id3dxkeyframedanimationset--getnumrotationkeys.md)
</dt> <dt>

[**ID3DXKeyframedAnimationSet::GetNumTranslationKeys**](id3dxkeyframedanimationset--getnumtranslationkeys.md)
</dt> </dl>

 

 
