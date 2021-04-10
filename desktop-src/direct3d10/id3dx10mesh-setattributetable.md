---
description: Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.
ms.assetid: 629fd31b-d88a-4650-82ed-ab7c40690986
title: 'ID3DX10Mesh:: SetAttributeTable (método) (D3DX10. h)'
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
ms.openlocfilehash: 808349b3f7456ebf3f8e1c3a7f9fdf2236db4beb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "104280415"
---
# <a name="id3dx10meshsetattributetable-method"></a>ID3DX10Mesh:: SetAttributeTable (método)

Establece la tabla de atributos de una malla y el número de entradas almacenadas en la tabla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAttributeTable(
  [in] const D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in]       UINT                   cAttribTableSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttribTable* \[ de\]
</dt> <dd>

Tipo: **\* [**intervalo de \_ atributo \_ const D3DX10**](d3dx10-attribute-range.md)**

Puntero a una matriz de estructuras de intervalos de atributos de D3DX10 \_ \_ , que representa las entradas de la tabla de atributos de malla.

</dd> <dt>

*cAttribTableSize* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de atributos en la tabla de atributos de malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Si una aplicación realiza un seguimiento de la información en una tabla de atributos y reorganiza la tabla como resultado de los cambios en los atributos o caras, este método permite que la aplicación actualice las tablas de atributos en lugar de volver a llamar a ID3DX10Mesh:: Optimize.

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

 

 
