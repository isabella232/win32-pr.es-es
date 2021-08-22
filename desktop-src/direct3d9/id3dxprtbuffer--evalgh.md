---
description: Aplica los datos de los medianes de textura almacenados a un búfer de textura ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: Método ID3DXPRTBuffer::EvalGH (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7c01eee9659bc650c6e914f17932fd12dca703150d69908511c37b4d7e0a41cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119493035"
---
# <a name="id3dxprtbufferevalgh-method"></a>Método ID3DXPRTBuffer::EvalGH

Aplica los datos de los medianes de textura almacenados a [**un búfer de textura ID3DXPRTBuffer.**](id3dxprtbuffer.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , se devolverá el siguiente valor.

## <a name="remarks"></a>Comentarios

Este método realiza una llamada interna a [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) para recuperar y aplicar datos de medianera de textura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




