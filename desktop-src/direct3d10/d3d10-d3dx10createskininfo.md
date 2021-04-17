---
description: Crea un objeto de malla de máscara vacía mediante un declarador.
ms.assetid: 5356cfe5-de90-462d-9722-72f3618decfb
title: Función D3DX10CreateSkinInfo (D3DX10Mesh. h)
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
ms.openlocfilehash: a68da20c2e2e15e3b73d55ee1df70518bba46200
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689892"
---
# <a name="d3dx10createskininfo-function"></a>D3DX10CreateSkinInfo función)

Crea un objeto de malla de máscara vacía mediante un declarador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateSkinInfo(
  _Out_ LPD3DX10SKININFO *ppSkinInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSkinInfo* \[ enuncia\]
</dt> <dd>

Tipo: **[ **LPD3DX10SKININFO**](id3dx10skininfo.md)\***

Dirección de un puntero a una [**interfaz ID3DX10SkinInfo**](id3dx10skininfo.md)que representa el objeto de malla de máscara creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser: E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Use [**ID3DX10SkinInfo:: SetBoneInfluence**](id3dx10skininfo-setboneinfluence.md) para rellenar el objeto de malla de máscara vacía devuelto por este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones de malla](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> <dt>

[Funciones de D3DX](d3d10-graphics-reference-d3dx10-functions.md)
</dt> </dl>

 

 




