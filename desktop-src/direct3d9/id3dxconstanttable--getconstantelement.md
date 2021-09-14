---
description: Obtiene una constante de una matriz de constantes. Una matriz se forma de elementos .
ms.assetid: 20a61207-b0e1-455d-9b65-0fade543d1cf
title: Método ID3DXConstantTable::GetConstantElement (D3DX9Shader.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964792"
---
# <a name="id3dxconstanttablegetconstantelement-method"></a>Método ID3DXConstantTable::GetConstantElement

Obtiene una constante de una matriz de constantes. Una matriz se forma de elementos .

## <a name="syntax"></a>Sintaxis


```C++
D3DXHANDLE GetConstantElement(
  [in] D3DXHANDLE hConstant,
  [in] UINT       Index
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la matriz de constantes. Este valor puede no ser **NULL.**

</dd> <dt>

*Índice* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Índice de base cero del elemento de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Devuelve un identificador único a la constante de elemento.

## <a name="remarks"></a>Observaciones

Para obtener una constante que no forma parte de una matriz, use [**ID3DXConstantTable::GetConstant**](id3dxconstanttable--getconstant.md) o [**ID3DXConstantTable::GetConstantByName**](id3dxconstanttable--getconstantbyname.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
