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
ms.openlocfilehash: b8f74715b163b3d197f62274c6aa6bf52ae872254db9df8225e061dc54900964
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119893725"
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



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




