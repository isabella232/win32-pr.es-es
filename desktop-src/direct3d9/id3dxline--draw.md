---
description: Dibuja una franja de líneas en el espacio de la pantalla. La entrada tiene el formato de una matriz que define puntos (de D3DXVECTOR2) en la franja de líneas.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: Método ID3DXLine::D raw (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Draw
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0a7492fb2128e0d9ec402d5211c20d5569ceb506
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060584"
---
# <a name="id3dxlinedraw-method"></a>Método ID3DXLine::D raw

Dibuja una franja de líneas en el espacio de la pantalla. La entrada tiene el formato de una matriz que define puntos [**(de D3DXVECTOR2)**](d3dxvector2.md)en la franja de líneas.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Draw(
  [in] const D3DXVECTOR2 *pVertexList,
  [in]       DWORD       dwVertexListCount,
  [in]       D3DCOLOR    Color
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVertexList* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Matriz de vértices que forma la línea. Vea [**D3DXVECTOR2**](d3dxvector2.md).

</dd> <dt>

*dwVertexListCount* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices en la lista de vértices.

</dd> <dt>

*Color* \[ En\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Color de la línea. Vea [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
