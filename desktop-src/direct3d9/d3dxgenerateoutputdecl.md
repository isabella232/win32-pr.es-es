---
description: Genera una declaración de vértice de salida a partir de la declaración de entrada. La declaración de salida está pensada para su uso por las funciones de teselación de malla.
ms.assetid: 528b0da3-fc31-4872-98f2-31e03c1cae5e
title: Función D3DXGenerateOutputDecl (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGenerateOutputDecl
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ce3fed752e74df3afa812c228a174503e20c6adf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127567916"
---
# <a name="d3dxgenerateoutputdecl-function"></a>Función D3DXGenerateOutputDecl

Genera una declaración de vértice de salida a partir de la declaración de entrada. La declaración de salida está pensada para su uso por las funciones de teselación de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXGenerateOutputDecl(
  _Out_       D3DVERTEXELEMENT9 *pOutput,
  _In_  const D3DVERTEXELEMENT9 *pInput
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOutput* \[ out\]
</dt> <dd>

Tipo: **[ **D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***

Puntero a la declaración de vértice de salida. Vea [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> <dt>

*pInput* \[ En\]
</dt> <dd>

Tipo: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Puntero a la declaración de vértice de entrada. Vea [**D3DVERTEXELEMENT9.**](d3dvertexelement9.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes valores: D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




