---
description: Acceda a la descripción del vértice pasada en D3DX10CreateMesh. La descripción del vértice describe el diseño de los búferes de vértices de la malla.
ms.assetid: e4a4a98a-e131-414c-ad98-21288ff0c61b
title: 'ID3DX10Mesh:: GetVertexDescription (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetVertexDescription
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 01888ea83f43e37951b48e03916f18af1ec6ddb6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104003827"
---
# <a name="id3dx10meshgetvertexdescription-method"></a>ID3DX10Mesh:: GetVertexDescription (método)

Acceda a la descripción del vértice pasada en [**D3DX10CreateMesh**](d3d10-d3dx10createmesh.md). La descripción del vértice describe el diseño de los búferes de vértices de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetVertexDescription(
  [out] const D3D10_INPUT_ELEMENT_DESC **ppDesc,
  [in]        UINT                     *pDeclCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppDesc* \[ enuncia\]
</dt> <dd>

Tipo: **const [**D3D10 \_ \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \* \* del elemento de entrada**

Matriz de elementos de entrada que describen el diseño de los búferes de vértices de la malla. Vea [**\_ Descripción del \_ elemento \_ de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*pDeclCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

El número de elementos de entrada en ppDesc.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces de D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
