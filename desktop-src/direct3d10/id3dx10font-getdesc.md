---
description: Obtenga una descripción del objeto de fuente actual.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: Método ID3DX10Font::GetDesc (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDesc
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d684a0bf485db441a0a6bf23cd36496cc13fdfe766eaa890682259b76b3800c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990445"
---
# <a name="id3dx10fontgetdesc-method"></a>Método ID3DX10Font::GetDesc

Obtenga una descripción del objeto de fuente actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ En\]
</dt> <dd>

Tipo: **[ **D3DX10 \_ FONT \_ DESC**](d3dx10-font-desc.md)\***

Puntero a una [**estructura \_ \_ DESC FONT de D3DX10**](d3dx10-font-desc.md) que describe el objeto de fuente. Si se define UNICODE, se devuelve un puntero a D3DX10FONT DESCW; de lo contrario, se devuelve un puntero \_ a D3DX10FONT \_ DESCA.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método describe los objetos de fuente Unicode si se define UNICODE. De lo contrario, se llama a GetDescA, que devuelve un puntero a la estructura D3DX10FONT \_ DESCA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




