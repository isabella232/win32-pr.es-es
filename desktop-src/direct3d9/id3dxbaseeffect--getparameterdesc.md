---
description: Obtiene un parámetro o una descripción de la anotación.
ms.assetid: fd54eb08-a7e4-4106-b0ed-49a4da7fcadc
title: 'ID3DXBaseEffect:: GetParameterDesc (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 8c3a52c06ebed764b3ab1718488c2dbc55ceda41
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698412"
---
# <a name="id3dxbaseeffectgetparameterdesc-method"></a>ID3DXBaseEffect:: GetParameterDesc (método)

Obtiene un parámetro o una descripción de la anotación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetParameterDesc(
  [in]  D3DXHANDLE         hParameter,
  [out] D3DXPARAMETER_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hParameter* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de parámetro o anotación. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md)\***

Devuelve una descripción del parámetro o anotación especificados. Vea [**D3DXPARAMETER \_ DESC**](d3dxparameter-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




