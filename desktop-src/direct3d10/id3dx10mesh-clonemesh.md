---
description: Crea una nueva malla y la rellena con los datos de una malla cargada previamente.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: 'ID3DX10Mesh:: CloneMesh (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.CloneMesh
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0f007475ea9f6aeaa6dc0c01bbd721c4a5103adf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718371"
---
# <a name="id3dx10meshclonemesh-method"></a>ID3DX10Mesh:: CloneMesh (método)

Crea una nueva malla y la rellena con los datos de una malla cargada previamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CloneMesh(
  [in]        UINT                     Flags,
  [in]        LPCSTR                   pPosSemantic,
  [in]  const D3D10_INPUT_ELEMENT_DESC *pDesc,
  [in]        UINT                     DeclCount,
  [out]       ID3DX10Mesh              **ppCloneMesh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Marcas de creación que se van a aplicar a la nueva malla. Consulte [**D3DX10 \_ Mesh**](d3dx10-mesh.md).

</dd> <dt>

*pPosSemantic* \[ de\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre semántico para los datos de la posición.

</dd> <dt>

*pDesc* \[ de\]
</dt> <dd>

Tipo: **\* const [**D3D10 \_ \_ \_ DESC del elemento de entrada**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)**

Matriz de \_ estructuras de Desc del elemento de entrada D3D10 \_ \_ , que describe el formato de vértice de la malla devuelta. Vea [**\_ Descripción del \_ elemento \_ de entrada D3D10**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*DeclCount* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de elementos de la matriz pDesc.

</dd> <dt>

*ppCloneMesh* \[ enuncia\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

La nueva malla.

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

 

 
