---
description: 'Método ID3DXConstantTable::GetDesc: obtiene una descripción de la tabla constante.'
ms.assetid: 3a7396c6-3a3e-44c2-96b7-60339015b376
title: Método ID3DXConstantTable::GetDesc (D3DX9Shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81b64f1a01af8909aa820e772214a1f11c6099b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888473"
---
# <a name="id3dxconstanttablegetdesc-method"></a>Método ID3DXConstantTable::GetDesc

Obtiene una descripción de la tabla constante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [in] D3DXCONSTANTTABLE_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ En\]
</dt> <dd>

Tipo: **[ **D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md)\***

Descripción de la tabla constante. Vea [**D3DXCONSTANTTABLE \_ DESC**](d3dxconstanttable-desc.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Shader.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXConstantTable](id3dxconstanttable.md)
</dt> <dt>

[**ID3DXConstantTable::GetConstantDesc**](id3dxconstanttable--getconstantdesc.md)
</dt> </dl>

 

 




