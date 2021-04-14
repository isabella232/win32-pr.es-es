---
description: Desasocia un objeto ID3DXTextureGutterHelper asociado con el objeto ID3DXPRTBuffer.
ms.assetid: 0bd8322a-8af1-4173-bbe3-9134c831cf3a
title: 'ID3DXPRTBuffer:: ReleaseGH (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ReleaseGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9fb7a68f11d21065d6b4911b9ee7f58920aeb25
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424527"
---
# <a name="id3dxprtbufferreleasegh-method"></a>ID3DXPRTBuffer:: ReleaseGH (método)

Desasocia un objeto [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) asociado con el objeto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseGH();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK.

## <a name="remarks"></a>Observaciones

Este método libera el puntero a la interfaz [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) .

Debe asegurarse de que el número de llamadas a [**ID3DXPRTBuffer:: AttachGH**](id3dxprtbuffer--attachgh.md) coincide con el número de llamadas **ID3DXPRTBuffer:: ReleaseGH** . Después de llamar a **ID3DXPRTBuffer:: ReleaseGH**, ya no se debe usar el puntero pGH devuelto por **ID3DXPRTBuffer:: AttachGH** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::AttachGH**](id3dxprtbuffer--attachgh.md)
</dt> </dl>

 

 




