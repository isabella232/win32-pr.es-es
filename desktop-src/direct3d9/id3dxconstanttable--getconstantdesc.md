---
description: Obtiene un puntero a una matriz de descripciones constantes en la tabla constante.
ms.assetid: bd407fd6-b1cc-4197-ae98-1c2ca74d2ad0
title: Método ID3DXConstantTable::GetConstantDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetConstantDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e5574c72fabd7561da0c60c903ae815faaebbfd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126969648"
---
# <a name="id3dxconstanttablegetconstantdesc-method"></a>Método ID3DXConstantTable::GetConstantDesc

Obtiene un puntero a una matriz de descripciones constantes en la tabla constante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetConstantDesc(
  [in]      D3DXHANDLE        hConstant,
  [in, out] D3DXCONSTANT_DESC *pDesc,
  [in, out] UINT              *pCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de una constante. Vea [D3DXHANDLE.](dx9-graphics-reference-effects-constants.md)

</dd> <dt>

*pDesc* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)\***

Devuelve un puntero a una matriz de descripciones. Vea [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md).

</dd> <dt>

*pCount* \[ in, out\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)\***

La entrada proporcionada debe ser el tamaño máximo de la matriz. La salida es el número de elementos que se rellenan en la matriz cuando se devuelve la función.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="remarks"></a>Observaciones

**ID3DXConstantTable::GetConstantDesc** a veces devolverá un [**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md) con un recuento de registros \_ de 0. Esto ocurrirá con una constante que aparece en más de un conjunto de registros, pero no tiene espacio en \_ ese conjunto de registros asignado.

Dado que un muestreador puede aparecer más de una vez en una tabla constante, este método puede devolver una matriz de descripciones, cada una con un índice de registro diferente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetDesc**](id3dxconstanttable--getdesc.md)
</dt> </dl>

 

 
