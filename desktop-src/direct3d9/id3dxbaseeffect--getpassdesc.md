---
description: Obtiene una descripción del paso.
ms.assetid: 44c65a82-bcf4-49f5-9312-8320e133bb2f
title: 'ID3DXBaseEffect:: GetPassDesc (método) (D3DX9Effect. h)'
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
ms.openlocfilehash: 15a997470fddf5056b7191fcc3226ad210724041
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718512"
---
# <a name="id3dxbaseeffectgetpassdesc-method"></a>ID3DXBaseEffect:: GetPassDesc (método)

Obtiene una descripción del paso.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetPassDesc(
  [in]  D3DXHANDLE    hPass,
  [out] D3DXPASS_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hPass* \[ de\]
</dt> <dd>

Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**

Identificador de paso. Vea [identificadores (Direct3D 9)](handles.md).

</dd> <dt>

*pDesc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXPASS \_ DESC**](d3dxpass-desc.md)\***

Devuelve una descripción del paso especificado. Vea [**D3DXPASS \_ DESC**](d3dxpass-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Observaciones

> [!Note]  
> Si se crea un efecto con [D3DXFX que no se pueda \_ \_ clonar](d3dxfx.md), este método devolverá punteros **null** (en [**D3DXPASS \_ DESC**](d3dxpass-desc.md)) a las funciones de sombreador.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Effect. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXBaseEffect](id3dxbaseeffect.md)
</dt> </dl>

 

 




