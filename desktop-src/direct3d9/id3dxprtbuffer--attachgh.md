---
description: Asocia un objeto ID3DXTextureGutterHelper al objeto ID3DXPRTBuffer.
ms.assetid: 095fea82-ac7a-42fa-990a-084715c73823
title: 'ID3DXPRTBuffer:: AttachGH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AttachGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1ba5afa238107d60620291b50b8f184eb4e5d361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707964"
---
# <a name="id3dxprtbufferattachgh-method"></a>ID3DXPRTBuffer:: AttachGH (método)

Asocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) al objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachGH(
  [in] LPD3DXTEXTUREGUTTERHELPER pGH
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pGH* \[ de\]
</dt> <dd>

Tipo: **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)**

Puntero a la interfaz [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) de un objeto que contiene los datos de medianil de textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Observaciones

El recuento de referencias del objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) se incrementará automáticamente en uno. Se liberarán todos los punteros de **ID3DXTextureGutterHelper** existentes.

Debe asegurarse de que el número de llamadas a **ID3DXPRTBuffer:: AttachGH** coincide con el número de llamadas [**ID3DXPRTBuffer:: ReleaseGH**](id3dxprtbuffer--releasegh.md) . Después de llamar a **ID3DXPRTBuffer:: ReleaseGH**, ya no se debe usar el puntero pGH devuelto por **ID3DXPRTBuffer:: AttachGH** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::ReleaseGH**](id3dxprtbuffer--releasegh.md)
</dt> </dl>

 

 




