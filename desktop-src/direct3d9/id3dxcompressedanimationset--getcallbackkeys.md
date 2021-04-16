---
description: Rellena una matriz con los datos de clave de devolución de llamada utilizados para la animación de fotogramas clave.
ms.assetid: 0dc30c1f-9ffb-42ec-8074-84293f16c344
title: 'ID3DXCompressedAnimationSet:: GetCallbackKeys (método) (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCallbackKeys
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fe56a3dbdd7d019deb5d7111fa592470bffd244d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105678802"
---
# <a name="id3dxcompressedanimationsetgetcallbackkeys-method"></a>ID3DXCompressedAnimationSet:: GetCallbackKeys (método)

Rellena una matriz con los datos de clave de devolución de llamada utilizados para la animación de fotogramas clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCallbackKeys(
  [out] LPD3DXKEY_CALLBACK pCallbackKeys
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pCallbackKeys* \[ enuncia\]
</dt> <dd>

Tipo: **[ **\_ devolución de llamada LPD3DXKEY**](d3dxkey-callback.md)**

Puntero a una matriz asignada por el usuario de estructuras de [**\_ devolución de llamada de D3DXKEY**](d3dxkey-callback.md) que el método va a rellenar con los datos de devolución de llamada.

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

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> <dt>

[**ID3DXCompressedAnimationSet::GetNumCallbackKeys**](id3dxcompressedanimationset--getnumcallbackkeys.md)
</dt> </dl>

 

 




