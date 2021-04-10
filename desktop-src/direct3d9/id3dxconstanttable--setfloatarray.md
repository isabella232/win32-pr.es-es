---
description: Establece una matriz de números de punto flotante.
ms.assetid: 7a622dd5-47ed-4166-a6df-f484b03e0b5a
title: 'ID3DXConstantTable:: SetFloatArray (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetFloatArray
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d75d4171ab51859e4095acbe5d3e86d704b1f437
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280355"
---
# <a name="id3dxconstanttablesetfloatarray-method"></a>ID3DXConstantTable:: SetFloatArray (método)

Establece una matriz de números de punto flotante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFloatArray(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const FLOAT             *pf,
  [in]       UINT              Count
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una interfaz [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla de constantes.

</dd> <dt>

*hConstant* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la matriz de constantes. Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*PF* \[ de\]
</dt> <dd>

Tipo: **const [**float**](../winprog/windows-data-types.md) \***

Matriz de números de punto flotante.

</dd> <dt>

*Recuento* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de valores de punto flotante de la matriz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
