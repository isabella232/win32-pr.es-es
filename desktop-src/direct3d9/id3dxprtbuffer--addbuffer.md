---
description: Agrega otro búfer a ID3DXPRTBuffer y almacena los resultados en ID3DXPRTBuffer.
ms.assetid: 345412f4-30c5-4c1d-b0ef-6e3e18c4e5ab
title: Método ID3DXPRTBuffer::AddBuffer (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.AddBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffbaffbb47d91b18a6fad9bdee98012fa11fb923a7c7586acf7d7b0cd181bcc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118294118"
---
# <a name="id3dxprtbufferaddbuffer-method"></a>Método ID3DXPRTBuffer::AddBuffer

Agrega otro búfer a [**ID3DXPRTBuffer**](id3dxprtbuffer.md) y almacena los resultados en **ID3DXPRTBuffer.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AddBuffer(
  [in] LPD3DXPRTBUFFER pBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pBuffer* \[ En\]
</dt> <dd>

Tipo: **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Puntero a un búfer que contiene los miembros que se van a agregar a los miembros respectivos del búfer [**ID3DXPRTBuffer.**](id3dxprtbuffer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor.

## <a name="remarks"></a>Comentarios

pBuffer e [**ID3DXPRTBuffer**](id3dxprtbuffer.md) deben tener el mismo número de muestras, coeficientes y canales de color; De lo contrario, se producirá un error en el método .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> </dl>

 

 




