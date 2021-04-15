---
description: Establece una matriz no transpuesta.
ms.assetid: 90329460-756e-4b3e-9ff3-be9dc556eb9f
title: 'ID3DXBaseEffect:: SetMatrix (método) (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.SetMatrix
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 39a5aed1d6321cf0599d212222fd967ee512e20e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547822"
---
# <a name="id3dxbaseeffectsetmatrix-method"></a>ID3DXBaseEffect:: SetMatrix (método)

Establece una matriz no transpuesta.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetMatrix(
  [in]       D3DXHANDLE hParameter,
  [in] const D3DXMATRIX *pMatrix
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador único. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pMatrix* \[ de\]
</dt> <dd>

Tipo: **const [**D3DXMATRIX**](d3dxmatrix.md) \***

Puntero a una matriz nontransposed. Vea [**D3DXMATRIX**](d3dxmatrix.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

Una matriz no transpuesta contiene datos principales de fila. En otras palabras, cada vector está incluido en una fila.

Si la matriz de destino es menor que la matriz de origen, se omitirán los componentes adicionales de la matriz de origen.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> <dt>

[**GetMatrix**](id3dxbaseeffect--getmatrix.md)
</dt> </dl>

 

 




