---
description: Limite el número de huesos que pueden influir en un vértice o limite la cantidad de influencia que puede tener un hueso en un vértice.
ms.assetid: 75c4d2eb-0a43-494d-9642-4c08aa814794
title: 'Método ID3DX10SkinInfo:: Compact (D3DX10. h)'
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
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104424359"
---
# <a name="id3dx10skininfocompact-method"></a>ID3DX10SkinInfo:: Compact (método)

Limite el número de huesos que pueden influir en un vértice o limite la cantidad de influencia que puede tener un hueso en un vértice.

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

*MaxPerVertexInfluences* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número máximo de huesos que pueden influir en cualquier vértice determinado. Este valor se omite si es mayor que el valor devuelto por [**ID3DX10SkinInfo:: GetMaxBoneInfluences**](id3dx10skininfo-getmaxboneinfluences.md).

</dd> <dt>

*ScaleMode* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Marca que describe cómo escalar los pesos restantes en un vértice determinado después de que se hayan cortado algunos en MinWeight. Si D3DX10 \_ SKININFO \_ no \_ se especifica ningún ajuste de escala, no se reducirá el tamaño de los pesos. Si \_ \_ se especifica D3DX10 SKININFO escalar \_ a \_ 1, los pesos mayores que MinWeight se escalarán verticalmente para que se agreguen hasta 1,0. Si \_ \_ se especifica D3DX10 SKININFO Scale \_ to total, se reducirán \_ los pesos mayores que MinWeight para que se agreguen al total original.

</dd> <dt>

*MinWeight* \[ de\]
</dt> <dd>

Tipo: **float**

Porcentaje mínimo de influencia, o peso, que cualquier hueso puede tener en cualquier vértice. Este valor debe estar comprendido entre 0 y 1.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si el método se ejecuta correctamente, el valor devuelto es S \_ OK. Si se produce un error en el método, el valor devuelto puede ser: E \_ OUTOFMEMORY o e \_ INVALIDARG.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10SkinInfo](id3dx10skininfo.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
