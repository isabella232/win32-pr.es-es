---
description: Obtiene una descripción del objeto de fuente actual. GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una \_ estructura D3DXFONT DESCW o D3DXFONT \_ Desca, respectivamente.
ms.assetid: 21bcd3e0-3659-4d64-959a-0f2d65850cb1
title: 'ID3DXFont:: GetDesc (método) (D3dx9core. h)'
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
ms.openlocfilehash: 3310971e360fb9994a30d62349d3e7e4b764c7d0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105717747"
---
# <a name="id3dxfontgetdesc-method"></a>ID3DXFont:: GetDesc (método)

Obtiene una descripción del objeto de fuente actual. GetDescW y GetDescA son idénticos a este método, salvo que se devuelve un puntero a una estructura [**D3DXFONT \_ DESCW**](d3dxfont-desc.md) o **D3DXFONT \_ Desca** , respectivamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXFONT_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXFONT \_ DESC**](d3dxfont-desc.md)\***

Puntero a una [**estructura \_ DESC de D3DXFONT**](d3dxfont-desc.md) que describe el objeto de fuente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Este método describe los objetos de fuente Unicode si se define Unicode. De lo contrario, se llama a GetDescA, que devuelve un puntero a la estructura [**\_ Desca de D3DXFONT**](d3dxfont-desc.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXFont](id3dxfont.md)
</dt> </dl>

 

 




