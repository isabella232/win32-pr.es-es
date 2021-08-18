---
description: Obtiene el búfer de datos que almacena los datos comprimidos de animación de fotogramas clave.
ms.assetid: cb42a4c8-6420-4694-9921-0d36cfe960e5
title: Método ID3DXCompressedAnimationSet::GetCompressedData (D3dx9anim.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet.GetCompressedData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e3290dcc9e9baeaa688117d8a98918e7df814a34812cb66791b2c8021a50f788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987595"
---
# <a name="id3dxcompressedanimationsetgetcompresseddata-method"></a>Método ID3DXCompressedAnimationSet::GetCompressedData

Obtiene el búfer de datos que almacena los datos comprimidos de animación de fotogramas clave.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetCompressedData(
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppCompressedData* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Dirección de un puntero al búfer de datos [**ID3DXBuffer que**](id3dxbuffer.md) recibe datos comprimidos de animación de fotogramas clave.

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

[ID3DXCompressedAnimationSet](id3dxcompressedanimationset.md)
</dt> </dl>

 

 




