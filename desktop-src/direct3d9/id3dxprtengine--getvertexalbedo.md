---
description: Recupera los valores albedo de los vértices de malla.
ms.assetid: 12b8d6d1-c806-4dcd-80ac-f3963215dcf4
title: Método ID3DXPRTEngine::GetVertexAlbedo (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.GetVertexAlbedo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7bdaf264e887c12b6dd711be978c5fc233bacc14d41d0899ddda43473001fe6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985565"
---
# <a name="id3dxprtenginegetvertexalbedo-method"></a>Método ID3DXPRTEngine::GetVertexAlbedo

Recupera los valores albedo de los vértices de malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVertexAlbedo(
  [in, out] D3DXCOLOR *pVertColors,
  [in]      UINT      NumVerts
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVertColors* \[ in, out\]
</dt> <dd>

Tipo: **[ **D3DXCOLOR**](d3dxcolor.md)\***

Puntero a una matriz de destino de valores albedo de los vértices de malla. Vea [**D3DXCOLOR.**](d3dxcolor.md)

</dd> <dt>

*NumVerts* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de vértices en la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> </dl>

 

 
