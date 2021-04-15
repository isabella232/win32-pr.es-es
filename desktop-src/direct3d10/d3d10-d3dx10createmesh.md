---
description: Crea un objeto Mesh mediante un declarador.
ms.assetid: 50e09378-2935-4b18-8fc9-5e58eaadae44
title: Función D3DX10CreateMesh (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateMesh
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2b00addb152fe18db448364fcc784c2044b10d23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105689893"
---
# <a name="d3dx10createmesh-function"></a>D3DX10CreateMesh función)

Crea un objeto Mesh mediante un declarador.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT D3DX10CreateMesh(
  _In_        ID3D10Device             *pDevice,
  _In_  const D3D10_INPUT_ELEMENT_DESC *pDeclaration,
  _In_        UINT                     DeclCount,
  _In_        LPCSTR                   pPositionSemantic,
  _In_        UINT                     VertexCount,
  _In_        UINT                     FaceCount,
  _In_        UINT                     Options,
  _Out_       ID3DX10Mesh              **ppMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pDevice* \[ de\]
</dt> <dd>

Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Puntero a una [**interfaz ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device), el objeto de dispositivo que se va a asociar a la malla.

</dd> <dt>

*pDeclaration* \[ de\]
</dt> <dd>

Tipo: **\* const [**D3D10 \_ \_ \_ DESC del elemento de entrada**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)**

Matriz de [**elementos \_ \_ \_ DESC del elemento de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) , que describe el formato de vértice de la malla devuelta. Este parámetro debe asignarse directamente a un formato de vértice flexible (FVF).

</dd> <dt>

*DeclCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos de pDeclaration.

</dd> <dt>

*pPositionSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Semántica que identifica qué parte de la declaración de vértice contiene información de posición.

</dd> <dt>

*VertexCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de vértices de la malla. Este parámetro debe ser mayor que 0.

</dd> <dt>

*FaceCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de caras de la malla. El intervalo válido para este número es mayor que 0 y uno menos que el valor DWORD máximo (normalmente 65534), ya que el último índice está reservado.

</dd> <dt>

*Opciones* \[ de de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Combinación de una o varias marcas de la [**\_ malla D3DX10**](d3dx10-mesh.md), especificando las opciones de la malla.

</dd> <dt>

*ppMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Dirección de un puntero a una [**interfaz ID3DX10Mesh**](id3dx10mesh.md)que representa el objeto de malla creado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la función se ejecuta correctamente, el valor devuelto es D3D \_ OK. Si se produce un error en la función, el valor devuelto puede ser uno de los siguientes: D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

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

 

 
