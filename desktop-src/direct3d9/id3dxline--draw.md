---
description: Dibuja una franja de líneas en el espacio de la pantalla. La entrada está en forma de una matriz que define los puntos (de D3DXVECTOR2) en la franja de línea.
ms.assetid: 10ad5af5-fb57-46ef-a89f-7a05dcf58826
title: ID3DXLine::D método RAW (D3dx9core. h)
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698378"
---
# <a name="id3dxlinedraw-method"></a>ID3DXLine::D método sin formato

Dibuja una franja de líneas en el espacio de la pantalla. La entrada está en forma de una matriz que define los puntos (de [**D3DXVECTOR2**](d3dxvector2.md)) en la franja de línea.

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

*pVertexList* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXVECTOR2**](d3dxvector2.md) \***

Matriz de vértices que forman la línea. Vea [**D3DXVECTOR2**](d3dxvector2.md).

</dd> <dt>

*dwVertexListCount* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices en la lista de vértices.

</dd> <dt>

*Color* \[ de de\]
</dt> <dd>

Tipo: **[ **D3DCOLOR**](d3dcolor.md)**

Color de la línea. Vea [**D3DCOLOR**](d3dcolor.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXLine](id3dxline.md)
</dt> </dl>

 

 
