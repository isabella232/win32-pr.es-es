---
description: Obtiene una descripción de paso.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: Método ID3DXBaseEffect::GetPassDesc (D3DX9Effect.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetPassDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 74106bc38367e13cd70af94d0ad12016165aaae24693f19386e69ebe1d7a5cb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987755"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>Método ID3DXBaseEffect::GetPassDesc

Obtiene una descripción de paso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPass* \[ En\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Controlador de paso. Vea [Identificadores (Direct3D 9).](handles.md)

</dd> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***

Devuelve una descripción del paso especificado. Vea [**D3DXPASS \_ DESC**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Comentarios

> [!Note]  
> Si se crea un efecto con [D3DXFX \_ NOT \_ CLONEABLE](d3dxfx.md), este método devolverá punteros **NULL** (en [**D3DXPASS \_ DESC)**](d3dxpass-desc.md)a las funciones del sombreador.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




