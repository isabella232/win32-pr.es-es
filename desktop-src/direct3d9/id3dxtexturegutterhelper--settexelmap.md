---
description: Establece las coordenadas de textura (u, v) de cada texel.
ms.assetid: b1f8f5d6-568f-4868-87c9-9d6b1034d898
title: Método ID3DXTextureGutterHelper::SetTexelMap (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetTexelMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c95ca7bff03cdd44e5bd5a331c696534e9a9ad43deacc49c181eb97fbc5ee9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491935"
---
# <a name="id3dxtexturegutterhelpersettexelmap-method"></a>Método ID3DXTextureGutterHelper::SetTexelMap

Establece las coordenadas de textura (u, v) de cada texel.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetTexelMap(
  [in] D3DXVECTOR2 *pTexelData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pTexelData* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXVECTOR2**](d3dxvector2.md)\***

Puntero a la ubicación en coordenadas de textura de píxel (u, v) donde se encuentra cada textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor. D3DERR \_ INVALIDCALL

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 




