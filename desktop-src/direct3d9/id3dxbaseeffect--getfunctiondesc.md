---
description: Obtiene una descripción de función.
ms.assetid: a1a0ccf4-2428-4e60-9af0-07dc2132a367
title: Método ID3DXBaseEffect::GetFunctionDesc (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 718960da7ff73f24f865fdacc09dfe55ff09a466
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126964824"
---
# <a name="id3dxbaseeffectgetfunctiondesc-method"></a>Método ID3DXBaseEffect::GetFunctionDesc

Obtiene una descripción de función.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetFunctionDesc(
  [in]  D3DXHANDLE        hFunction,
  [out] D3DXFUNCTION_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFunction* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de función. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md)\***

Devuelve una descripción de la función. Vea [**D3DXFUNCTION \_ DESC**](d3dxfunction-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




