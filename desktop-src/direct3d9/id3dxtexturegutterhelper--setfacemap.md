---
description: Establece el índice de la superficie de la malla a la que pertenece cada textura.
ms.assetid: 45d931bc-fb8b-48da-b30d-99d5dc183494
title: 'ID3DXTextureGutterHelper:: SetFaceMap (método) (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXTextureGutterHelper.SetFaceMap
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8ba0472052d5e2e06d759c83a404a197ecda148f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280463"
---
# <a name="id3dxtexturegutterhelpersetfacemap-method"></a>ID3DXTextureGutterHelper:: SetFaceMap (método)

Establece el índice de la superficie de la malla a la que pertenece cada textura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetFaceMap(
  [in] UINT *pFaceData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pFaceData* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero al índice de la superficie de la malla a la que pertenece cada textura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, se devolverá el valor siguiente. D3DERR \_ INVALIDCALL

## <a name="remarks"></a>Observaciones

La entrada de datos de la superficie de la malla para este método solo es válida para textura válido (que no es de clase 0). [**ID3DXTextureGutterHelper:: GetGutterMap**](id3dxtexturegutterhelper--getguttermap.md) devolverá valores distintos de cero para textura válidos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DXTextureGutterHelper](id3dxtexturegutterhelper.md)
</dt> </dl>

 

 
