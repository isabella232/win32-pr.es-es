---
description: Vuelve a muestrear un búfer ID3DXPRTBuffer de entrada y lo guarda en un búfer de salida. Este método se puede usar para convertir un búfer de vértices en un búfer de textura y viceversa. También se puede usar para convertir búferes de canal único en búferes de 3 canales y viceversa.
ms.assetid: 78015044-38a9-4c08-a690-28f6427dae8c
title: Método ID3DXPRTEngine::ResampleBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ResampleBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c8517d04be1d63159a2548935f3e09c12e646775
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966703"
---
# <a name="id3dxprtengineresamplebuffer-method"></a>Método ID3DXPRTEngine::ResampleBuffer

Vuelve a muestrear un búfer [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de entrada y lo guarda en un búfer de salida. Este método se puede usar para convertir un búfer de vértices en un búfer de textura y viceversa. También se puede usar para convertir búferes de canal único en búferes de 3 canales y viceversa.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ResampleBuffer(
  [in]      LPD3DXPRTBUFFER pBufferIn,
  [in, out] LPD3DXPRTBUFFER pBufferOut
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBufferIn* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero al búfer [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) entrada.

</dd> <dt>

*pBufferOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero al búfer [**ID3DXPRTBuffer de**](id3dxprtbuffer.md) salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 




