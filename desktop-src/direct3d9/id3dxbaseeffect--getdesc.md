---
description: Obtiene la descripción del efecto.
ms.assetid: 96b53b8a-0c20-4bfd-af45-626f6e0305d2
title: 'ID3DXBaseEffect:: GetDesc (método) (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetDesc
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 35fcb62e9461d419e6643c99c1879efa28fa78c1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105698415"
---
# <a name="id3dxbaseeffectgetdesc-method"></a>ID3DXBaseEffect:: GetDesc (método)

Obtiene la descripción del efecto.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXEFFECT_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXEFFECT \_ DESC**](d3dxeffect-desc.md)\***

Devuelve una descripción del efecto. Vea [**D3DXEFFECT \_ DESC**](d3dxeffect-desc.md).

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

 

 




