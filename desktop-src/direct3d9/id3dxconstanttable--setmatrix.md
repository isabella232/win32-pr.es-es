---
description: Establece una matriz sin transacciones.
ms.assetid: 30369e34-6e9d-4480-a142-e38f46fd38b0
title: Método ID3DXConstantTable::SetMatrix (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetMatrix
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 76b33f5b3f2c4f2856acf2cdf842b837587a73761e837beeb7a86887ca25b741
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987565"
---
# <a name="id3dxconstanttablesetmatrix-method"></a>Método ID3DXConstantTable::SetMatrix

Establece una matriz sin transacciones.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrix(
  [in]       LPDIRECT3DDEVICE9 pDevice,
  [in]       D3DXHANDLE        hConstant,
  [in] const D3DXMATRIX        *pMatrix
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ En\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntero a una [**interfaz IDirect3DDevice9,**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) que representa el dispositivo asociado a la tabla constante.

</dd> <dt>

*hConstant* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único de la matriz de constantes. Vea [D3DXHANDLE](dx9-graphics-reference-effects-constants.md).

</dd> <dt>

*pMatrix* \[ En\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una matriz sin transacciones. Vea [**D3DXMATRIX.**](d3dxmatrix.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> </dl>

 

 
