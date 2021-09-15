---
description: Crea un objeto de malla de máscara vacío mediante un código de formato de vértice flexible (FVF).
ms.assetid: 72e27850-0102-4121-a397-16f2e0220b93
title: Función D3DXCreateSkinInfoFVF (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSkinInfoFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 907ab874b8cd8b766e6f9413212ba8771df9b25c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575221"
---
# <a name="d3dxcreateskininfofvf-function"></a>Función D3DXCreateSkinInfoFVF

Crea un objeto de malla de máscara vacío mediante un código de formato de vértice flexible (FVF).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DXCreateSkinInfoFVF(
  _In_  DWORD          NumVertices,
  _In_  DWORD          FVF,
  _In_  DWORD          NumBones,
  _Out_ LPD3DXSKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NumVertices* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de vértices para la malla de máscara.

</dd> <dt>

*FVF* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Combinación de [D3DFVF](d3dfvf.md) que describe el formato de vértice para la malla de máscara devuelta.

</dd> <dt>

*Num Num* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Número de esqueletos para la malla de máscara.

</dd> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DXSKININFO**](id3dxskininfo.md)\***

Dirección de un puntero a una [**interfaz ID3DXSkinInfo,**](id3dxskininfo.md) que representa el objeto de información de máscara creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Use [**SetIonalInfluence para**](id3dxskininfo--setboneinfluence.md) rellenar el objeto de malla de máscara vacío devuelto por este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**SetIonalInfluence**](id3dxskininfo--setboneinfluence.md)
</dt> </dl>

 

 
