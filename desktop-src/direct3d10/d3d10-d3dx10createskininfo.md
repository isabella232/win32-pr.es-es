---
description: 'Función D3DX10CreateSkinInfo: crea un objeto de malla de máscara vacía mediante un declarador.'
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Función D3DX10CreateSkinInfo (D3DX10Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateSkinInfo
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 17d6ec99d3f43c41d56deebef81a021c81ec1d69
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103603"
---
# <a name="d3dx10createskininfo-function"></a>Función D3DX10CreateSkinInfo

Crea un objeto de malla de máscara vacía mediante un declarador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSkinInfo* \[ out\]
</dt> <dd>

Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Dirección de un puntero a una [**interfaz ID3DX10SkinInfo**](id3dx10skininfo.md), que representa el objeto de malla de máscara creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Comentarios

Use [**id3DX10SkinInfo::SetIonalInfluence para**](id3dx10skininfo-setboneinfluence.md) rellenar el objeto de malla de máscara vacío devuelto por este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funciones D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




