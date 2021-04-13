---
description: Compila una matriz usando los desplazamientos especificados.
ms.assetid: 1cb713d5-b994-4496-a506-89451be09fb2
title: Función D3DXMatrixTranslation (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixTranslation
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c74d56eaa0e41bc6ce9060ff291885a8a5c05a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104362556"
---
# <a name="d3dxmatrixtranslation-function-d3dx9mathh"></a>Función D3DXMatrixTranslation (D3dx9math. h)

Compila una matriz usando los desplazamientos especificados.

## <a name="syntax"></a>Sintaxis


```C++
D3DXMATRIX* D3DXMatrixTranslation(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      x,
  _In_    FLOAT      y,
  _In_    FLOAT      z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pOut* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a la estructura [**D3DXMATRIX**](d3dxmatrix.md) que es el resultado de la operación.

</dd> <dt>

*x* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Desplazamiento de la coordenada X.

</dd> <dt>

*y* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Desplazamiento de la coordenada Y.

</dd> <dt>

*z* \[ en\]
</dt> <dd>

Tipo: **[ **float**](../winprog/windows-data-types.md)**

Desplazamiento de la coordenada Z.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **D3DXMATRIX**](d3dxmatrix.md)\***

Puntero a una estructura [**D3DXMATRIX**](d3dxmatrix.md) que contiene una matriz de transformación traducida.

## <a name="remarks"></a>Observaciones

El valor devuelto para esta función es el mismo valor que se devuelve en el parámetro *pOut* . De esta manera, D3DXMATRIXTranslation se puede usar como parámetro de otra función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9math. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones matemáticas](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
