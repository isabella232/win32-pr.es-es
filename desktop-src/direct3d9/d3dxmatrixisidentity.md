---
description: Determina si una matriz es una matriz de identidad.
ms.assetid: 00f72d08-5d4b-4310-8167-e6b6371d24fd
title: Función D3DXMatrixIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0c2ca91f74512b432d7cc18b28cef44d713cfc11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362686"
---
# <a name="d3dxmatrixisidentity-function"></a>D3DXMatrixIsIdentity función)

Determina si una matriz es una matriz de identidad.

## <a name="syntax"></a>Sintaxis


```C++
BOOL D3DXMatrixIsIdentity(
  _In_ const D3DXMATRIX *pM
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*p. m* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) cuya identidad se probará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Si la matriz es una matriz de identidad, esta función devuelve **true**. De lo contrario, esta función devuelve **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[**D3DXMatrixIdentity**](d3dxmatrixidentity.md)
</dt> </dl>

 

 
