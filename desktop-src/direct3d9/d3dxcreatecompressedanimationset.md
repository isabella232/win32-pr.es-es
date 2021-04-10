---
description: Crea una interfaz de conjunto de animaciones con fotogramas clave ID3DXCompressedAnimationSet que almacena los datos de fotogramas clave en un formato comprimido.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Función D3DXCreateCompressedAnimationSet (D3dx9anim. h)
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
ms.openlocfilehash: 8aab23466cecf43a50a4136eb0b3d93a271dcb0e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003844"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>D3DXCreateCompressedAnimationSet función)

Crea una interfaz de conjunto de animaciones con fotogramas clave [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que almacena los datos de fotogramas clave en un formato comprimido.

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

*pName* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntero al nombre del conjunto de animaciones.

</dd> <dt>

*TicksPerSecond* \[ de\]
</dt> <dd>

Tipo: **[ **Double**](../winprog/windows-data-types.md)**

Número de TICs de fotogramas clave que transcurren por segundo.

</dd> <dt>

*Reproducción* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DXPLAYBACK \_ Type**](./d3dxplayback-type.md)**

Tipo del bucle de reproducción establecido de la animación. Consulte [**\_ tipo de D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

*pCompressedData* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Puntero al búfer de [**ID3DXBuffer**](id3dxbuffer.md) que almacena el conjunto de animación como datos comprimidos.

</dd> <dt>

*NumCallbackKeys* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de claves de devolución de llamada.

</dd> <dt>

*pCallKeys* \[ de\]
</dt> <dd>

Tipo: **[**LPD3DXKEY de \_ devolución de llamada**](d3dxkey-callback.md) const \***

Puntero a una estructura de [**\_ devolución de llamada D3DXKEY**](d3dxkey-callback.md) que almacena los datos de devolución de llamada del usuario.

</dd> <dt>

*ppAnimationSet* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Dirección de un puntero a la interfaz [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) que almacena los datos de conjuntos de animación fotogramas clave en un formato comprimido.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los valores siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de animación](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
