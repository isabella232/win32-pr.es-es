---
description: Obtiene el número máximo de influencias de caras en una malla de triángulo con el búfer de índice especificado.
ms.assetid: 72dc2440-87df-461e-80d0-9ad9b1e4d8ee
title: 'ID3DXSkinInfo:: GetMaxFaceInfluences (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo.GetMaxFaceInfluences
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 11724c50d5224f0bcb2c9ced25523b869f3e347f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424315"
---
# <a name="id3dxskininfogetmaxfaceinfluences-method"></a>ID3DXSkinInfo:: GetMaxFaceInfluences (método)

Obtiene el número máximo de influencias de caras en una malla de triángulo con el búfer de índice especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetMaxFaceInfluences(
  [in] LPDIRECT3DINDEXBUFFER9 pIB,
  [in] DWORD                  NumFaces,
  [in] DWORD                  *maxFaceInfluences
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pIB* \[ de\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DINDEXBUFFER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9)**

Puntero al búfer de índice que contiene los datos del índice de malla.

</dd> <dt>

*NumFaces* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de caras en la malla.

</dd> <dt>

*maxFaceInfluences* \[ de\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)\***

Puntero a las influencias máximas de la superficie.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser D3DERR \_ INVALIDCALL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXSkinInfo](id3dxskininfo.md)
</dt> </dl>

 

 
