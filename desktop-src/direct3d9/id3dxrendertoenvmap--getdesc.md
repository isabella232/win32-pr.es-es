---
description: Recupera la descripción de la superficie de representación.
ms.assetid: 3c2612fa-540d-4d7a-9821-bf37fa3b6da4
title: 'ID3DXRenderToEnvMap:: GetDesc (método) (D3dx9core. h)'
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
ms.openlocfilehash: d0b9faf5bdd4c57f7320749aef2010f457dd682e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821018"
---
# <a name="id3dxrendertoenvmapgetdesc-method"></a>ID3DXRenderToEnvMap:: GetDesc (método)

Recupera la descripción de la superficie de representación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetDesc(
  [out] D3DXRTE_DESC *pDesc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDesc* \[ enuncia\]
</dt> <dd>

Tipo: **[ **D3DXRTE \_ DESC**](d3dxrte-desc.md)\***

Puntero a una [**estructura \_ DESC de D3DXRTE**](d3dxrte-desc.md) que describe la superficie de representación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXRenderToEnvMap](id3dxrendertoenvmap.md)
</dt> </dl>

 

 




