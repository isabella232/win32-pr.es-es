---
description: Crea una interfaz de conjunto de animaciones con fotogramas clave ID3DXCompressedAnimationSet que almacena los datos del fotograma clave en un formato comprimido.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Función D3DXCreateCompressedAnimationSet (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acca9d1b697bb9b06b47aa75948ca74ec00cc7ecb919334c01cf874293cb495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299290"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>Función D3DXCreateCompressedAnimationSet

Crea una interfaz de conjunto de animaciones con fotogramas clave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que almacena los datos del fotograma clave en un formato comprimido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
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

*pCompressedData* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntero al búfer [**ID3DXBuffer que**](id3dxbuffer.md) almacena el conjunto de animaciones como datos comprimidos.

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

Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Dirección de un puntero a la interfaz [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que almacena los datos del conjunto de animación enmarcado clave en un formato comprimido.

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

 

 
