---
description: Recupera la descripción de la superficie de representación.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: Método ID3DXRenderToEnvMap::GetDesc (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXRenderToEnvMap.GetDesc
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7cfe9f3e8e857806895ec8be249d51f63ffe4818f24bbbf12d842754a885e855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847315"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>Método ID3DXRenderToEnvMap::GetDesc

Recupera la descripción de la superficie de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ out\]
</dt> <dd>

Tipo: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***

Puntero a una [**estructura D3DXRTE \_ DESC**](d3dxrte-desc.md) que describe la superficie de representación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




