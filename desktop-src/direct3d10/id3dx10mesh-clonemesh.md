---
description: Crea una nueva malla y la rellena con los datos de una malla cargada previamente.
ms.assetid: 2ce39982-abc0-444b-bc6f-24508f76fe31
title: Método ID3DX10Mesh::CloneMesh (D3DX10.h)
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
ms.openlocfilehash: 292522e47dbaf6937d871209006134e866e92fdeb27f6edba4f4f71f6d1fad14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409135"
---
# <a name="id3dx10meshclonemesh-method"></a>Método ID3DX10Mesh::CloneMesh

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

*Marcas* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Marcas de creación que se aplicarán a la nueva malla. Vea [**D3DX10 \_ MESH**](d3dx10-mesh.md).

</dd> <dt>

*pPosSemantic* \[ En\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Nombre semántico de los datos de posición.

</dd> <dt>

*pDesc* \[ En\]
</dt> <dd>

Tipo: **const [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc) \***

Matriz de estructuras D3D10 \_ INPUT \_ ELEMENT \_ DESC, que describen el formato de vértice de la malla devuelta. Vea [**D3D10 \_ INPUT ELEMENT \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc).

</dd> <dt>

*DeclCount* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de elementos de la matriz pDesc.

</dd> <dt>

*ppCloneMesh* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DX10Mesh**](id3dx10mesh.md)\*\***

Nueva malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
