---
description: 'Método ID3DX10Mesh::SetAttributeTable: establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.'
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: Método ID3DX10Mesh::SetAttributeTable (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6cdaedef52693810519ebb92e6f523afbfe078df68a2a13b7fae7ce0fad98fb1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634545"
---
# <a name="id3dx10meshsetattributetable-method"></a>Método ID3DX10Mesh::SetAttributeTable

Establece la tabla de atributos para una malla y el número de entradas almacenadas en la tabla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttribTable* \[ En\]
</dt> <dd>

Tipo: **const [**D3DX10 \_ ATTRIBUTE \_ RANGE**](d3dx10-attribute-range.md) \***

Puntero a una matriz de estructuras D3DX10 ATTRIBUTE RANGE, que \_ representan las entradas de la tabla de atributos de \_ malla.

</dd> <dt>

*cAttribTableSize* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Número de atributos de la tabla de atributos de malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Si una aplicación realiza un seguimiento de la información de una tabla de atributos y reorganiza la tabla como resultado de cambios en atributos o caras, este método permite a la aplicación actualizar las tablas de atributos en lugar de llamar de nuevo a ID3DX10Mesh::Optimize.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[D3DX Interfaces](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
