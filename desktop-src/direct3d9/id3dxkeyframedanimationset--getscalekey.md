---
description: Obtiene información de escala para un fotograma clave específico del conjunto de animaciones.
ms.assetid: 7f4a0bf3-2922-4fd7-bb85-b387d3e983a7
title: Método ID3DXKeyframedAnimationSet::GetScaleKey (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.GetScaleKey
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 199b5596e05bd013f3384c2a182bbe8e905cb609ae869c194d811fb97d3d254b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119121162"
---
# <a name="id3dxkeyframedanimationsetgetscalekey-method"></a>Método ID3DXKeyframedAnimationSet::GetScaleKey

Obtiene información de escala para un fotograma clave específico del conjunto de animaciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetScaleKey(
  [in] UINT              Animation,
  [in] UINT              Key,
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

*Clave* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Fotograma clave.

</dd> <dt>

*pScaleKeys* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXKEY \_ VECTOR3**](d3dxkey-vector3.md)**

Puntero a los datos de escala. Vea [**D3DXKEY \_ VECTOR3**](d3dxkey-vector3.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
