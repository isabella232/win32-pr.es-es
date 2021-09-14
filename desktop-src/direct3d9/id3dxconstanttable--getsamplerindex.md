---
description: Devuelve el índice del muestreador.
ms.assetid: vs|directx_sdk|~\id3dxconstanttable__getsamplerindex.htm
title: Método ID3DXConstantTable::GetSamplerIndex (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetSamplerIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f803b6e129ac20b8a22ed2393ab941698c02d3d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964787"
---
# <a name="id3dxconstanttablegetsamplerindex-method"></a>Método ID3DXConstantTable::GetSamplerIndex

Devuelve el índice del muestreador.

## <a name="syntax"></a>Sintaxis


```C++
UINT GetSamplerIndex(
  [out] D3DXHANDLE hConstant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hConstant* \[ out\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador del muestreador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Devuelve el número de índice del muestreador de la tabla constante.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
