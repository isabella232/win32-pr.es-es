---
description: Optimiza la malla de revisión para una teselación eficaz.
ms.assetid: 0049e649-5fe5-45b4-9b09-14b7f99b4988
title: Método ID3DXPatchMesh::Optimize (D3DX9Mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.Optimize
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6fa66aadd0ef1f9f9f65747694fc311f80172449
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060536"
---
# <a name="id3dxpatchmeshoptimize-method"></a>Método ID3DXPatchMesh::Optimize

Optimiza la malla de revisión para una teselación eficaz.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Optimize(
  [in] DWORD Flags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

Actualmente no se usa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en el método, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, D3DXERR \_ CANNOTATTRSORT.

## <a name="remarks"></a>Observaciones

Una vez que una aplicación genera información de adyacencia para una malla, los datos de la malla se pueden optimizar (reordenar) para mejorar el rendimiento del dibujo. Este método determina qué revisiones son adyacentes (dentro de la tolerancia proporcionada).

La información de adyacencia también se usa para optimizar la teselación. Genere información de adyacencia una vez y entrelaze repetidamente mediante una llamada a [**ID3DXPatchMesh::Tessellate**](id3dxpatchmesh--tessellate.md). La optimización realizada es independiente del nivel de teselación real utilizado. Sin embargo, si se cambian los vértices de la malla, debe volver a generar la información de adyacencia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX9Mesh.h</dt> </dl> |
| Biblioteca<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DXPatchMesh](id3dxpatchmesh.md)
</dt> <dt>

[**ID3DXPatchMesh::GenerateAdjacency**](id3dxpatchmesh--generateadjacency.md)
</dt> </dl>

 

 
