---
description: Obtiene una constante de una matriz de constantes. Una matriz se compone de elementos.
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: 'ID3DXConstantTable:: GetConstantElement (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantElement
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5396c70c1c4286223d9f45fb8ab9b73a019becb1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718256"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>ID3DXConstantTable:: GetConstantElement (método)

Obtiene una constante de una matriz de constantes. Una matriz se compone de elementos.

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la matriz de constantes. Este valor no puede ser **null**.

</dd> <dt>

*Índice* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Índice de base cero del elemento de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador único a la constante del elemento.

## <a name="remarks"></a>Observaciones

Para obtener una constante que no forma parte de una matriz, use [**ID3DXConstantTable:: GetConstant**](id3dxconstanttable--getconstant.md) o [**ID3DXConstantTable:: GetConstantByName**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
