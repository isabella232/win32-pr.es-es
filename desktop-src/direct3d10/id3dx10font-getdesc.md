---
description: Obtiene una descripción del objeto de fuente actual.
ms.assetid: f08beb35-351f-4087-a2db-097843463291
title: 'ID3DX10Font:: GetDesc (método) (D3DX10. h)'
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
ms.openlocfilehash: 59a7e361ebb6254fcc49eab30ff44ab39c38fd76
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105670251"
---
# <a name="id3dx10fontgetdesc-method"></a>ID3DX10Font:: GetDesc (método)

Obtiene una descripción del objeto de fuente actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [in] D3DX10_FONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ de\]
</dt> <dd>

Type: **[ **D3DX10 \_ Font \_ DESC**](d3dx10-font-desc.md)\***

Puntero a una estructura de [**\_ \_ DESC de fuente D3DX10**](d3dx10-font-desc.md) que describe el objeto de fuente. Si se define Unicode, se devuelve un puntero a un DESCW de D3DX10FONT \_ ; de lo contrario, se devuelve un puntero a D3DX10FONT \_ Desca.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método describe los objetos de fuente Unicode si se define Unicode. De lo contrario, se llama a GetDescA, que devuelve un puntero a la \_ estructura Desca de D3DX10FONT.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Font](id3dx10font.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




