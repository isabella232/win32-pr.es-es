---
description: 'Función D3DX10CreateSkinInfo: crea un objeto de malla de máscara vacío mediante un declarador.'
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
ms.openlocfilehash: 52a6d1116e46771c4c092fb08f3d59f43277d2437db1bd2c5b750f4a381043fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070195"
---
# <a name="d3dx10createskininfo-function"></a>Función D3DX10CreateSkinInfo

Crea un objeto de malla de máscara vacío mediante un declarador.

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

Use [**id3DX10SkinInfo::SetIonalInfluence**](id3dx10skininfo-setboneinfluence.md) para rellenar el objeto de malla de máscara vacío devuelto por este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funciones D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




