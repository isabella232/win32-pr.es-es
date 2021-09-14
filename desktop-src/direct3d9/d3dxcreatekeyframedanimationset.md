---
description: Crea una interfaz de conjunto de animaciones con fotogramas clave ID3DXKeyframedAnimationSet.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Función D3DXCreateKeyframedAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3f3eb45e999d25c776014c3df5824e0468d03ffd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072828"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>Función D3DXCreateKeyframedAnimationSet

Crea una interfaz de conjunto de animaciones con fotogramas clave [**ID3DXKeyframedAnimationSet.**](id3dxkeyframedanimationset.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pName* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del conjunto de animaciones.

</dd> <dt>

*TicksPerSecond* \[ En\]
</dt> <dd>

Tipo: **[ **DOUBLE**](../winprog/windows-data-types.md)**

Número de pasos de fotograma clave que transcurren por segundo.

</dd> <dt>

*Reproducción* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md)**

Tipo del bucle de reproducción del conjunto de animaciones. Vea [**D3DXPLAYBACK \_ TYPE**](./d3dxplayback-type.md).

</dd> <dt>

*NumAnimations* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de conjuntos de animación de escala, rotación y traducción (SRT).

</dd> <dt>

*NumCallbackKeys* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de claves de devolución de llamada.

</dd> <dt>

*pCallKeys* \[ En\]
</dt> <dd>

Tipo: **const [**LPD3DXKEY \_ CALLBACK**](d3dxkey-callback.md) \***

Puntero a una estructura [**de devolución de llamada D3DXKEY \_**](d3dxkey-callback.md) que almacena datos de devolución de llamada de usuario.

</dd> <dt>

*ppAnimationSet* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Dirección de un puntero a la interfaz de conjunto de animación enmarcada en clave [**ID3DXKeyframedAnimationSet.**](id3dxkeyframedanimationset.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
