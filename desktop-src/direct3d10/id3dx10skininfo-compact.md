---
description: Limitar el número de esqueletos que pueden influir en un vértice o limitar la cantidad de influencia que puede tener un esqueleto en un vértice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: Método ID3DX10SkinInfo::Compact (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo.Compact
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 379343688a1fd2ffe5ebd968dc984fa09faada7d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126888780"
---
# <a name="id3dx10skininfocompact-method"></a>Método ID3DX10SkinInfo::Compact

Limitar el número de esqueletos que pueden influir en un vértice o limitar la cantidad de influencia que puede tener un esqueleto en un vértice.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Compact(
  [in] UINT  MaxPerVertexInfluences,
  [in] UINT  ScaleMode,
  [in] float MinWeight
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*MaxPerVertexInfluences* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número máximo de esqueletos que pueden influir en cualquier vértice determinado. Este valor se omite si es mayor que el valor devuelto por [**ID3DX10SkinInfo::GetMaxIonalInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Una marca que describe cómo escalar los pesos restantes en un vértice determinado después de que MinWeight haya reducido algunos. Si se especifica D3DX10 SKININFO NO SCALING, los pesos no se \_ \_ \_ escalarán en absoluto. Si se especifica D3DX10 SKININFO SCALE TO 1, los pesos mayores que MinWeight se escalarán verticalmente para que suman \_ \_ hasta \_ \_ 1,0. Si se especifica D3DX10 SKININFO SCALE TO TOTAL, los pesos mayores que MinWeight se escalarán verticalmente para que se suman al \_ \_ total \_ \_ original.

</dd> <dt>

*MinWeight* \[ En\]
</dt> <dd>

Tipo: **float**

El porcentaje mínimo de influencia, o peso, que cualquier pórmo puede tener en cualquier vértice. Este valor debe estar entre 0 y 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se realiza correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método , el valor devuelto puede ser: E \_ OUTOFMEMORY o E \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
