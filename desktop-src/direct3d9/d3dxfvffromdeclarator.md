---
description: Devuelve un código de formato de vértice flexible (FVF) de un declarador.
ms.assetid: 4f30087e-0042-44bc-a7a5-5386b18fcad7
title: Función D3DXFVFFromDeclarator (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFVFFromDeclarator
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fdaf6f80340a08562ed644ee44ac92c42874d149
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362567"
---
# <a name="d3dxfvffromdeclarator-function"></a>D3DXFVFFromDeclarator función)

Devuelve un código de formato de vértice flexible (FVF) de un declarador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXFVFFromDeclarator(
  _In_  const LPD3DVERTEXELEMENT9 *pDeclaration,
  _Out_       DWORD               *pFVF
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDeclaration* \[ de\]
</dt> <dd>

Tipo: **const [**LPD3DVERTEXELEMENT9**](d3dvertexelement9.md) \***

Matriz de elementos [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , que describe el código FVF.

</dd> <dt>

*pFVF* \[ enuncia\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a un valor DWORD que representa la combinación devuelta de [D3DFVF](d3dfvf.md) que describe el formato de vértice devuelto por el declarador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Se producirá un error en esta función para cualquier declarador que no se asigne directamente a un FVF.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXDeclaratorFromFVF**](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
