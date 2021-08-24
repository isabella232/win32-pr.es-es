---
description: Obtiene una descripción del objeto de fuente actual. GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una estructura D3DXFONT \_ DESCW o D3DXFONT \_ DESCA, respectivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: Método ID3DXFont::GetDesc (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a2961c69e47bb46eaf782e8f5d4dbfe0be2d82a49f00f98c36b1ee7b141e962b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119675435"
---
# <a name="id3dxfontgetdesc-method"></a>Método ID3DXFont::GetDesc

Obtiene una descripción del objeto de fuente actual. GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una estructura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ DESCA,** respectivamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

Puntero a una [**estructura D3DXFONT \_ DESC**](d3dxfont-desc.md) que describe el objeto de fuente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el siguiente valor: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

Este método describe los objetos de fuente Unicode si se define UNICODE. De lo contrario, se llama a GetDescA, que devuelve un puntero a la estructura [**D3DXFONT \_ DESCA.**](d3dxfont-desc.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




