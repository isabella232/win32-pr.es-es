---
description: Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.
ms.assetid: cee49eba-c113-49f5-a702-c366401f1f2d
title: 'ID3DX10Mesh:: GetAttributeTable (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetAttributeTable
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4ff00f3c5d036b3b463bc7c6622de75361b196e6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707988"
---
# <a name="id3dx10meshgetattributetable-method"></a>ID3DX10Mesh:: GetAttributeTable (método)

Recupera una tabla de atributos para una malla o el número de entradas almacenadas en una tabla de atributos para una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAttributeTable(
  [in] D3DX10_ATTRIBUTE_RANGE *pAttribTable,
  [in] UINT                   *pAttribTableSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAttribTable* \[ de\]
</dt> <dd>

Tipo: **[ **\_ \_ intervalo del atributo D3DX10**](d3dx10-attribute-range.md)\***

Puntero a una matriz de estructuras de intervalo de atributos de D3DX10 \_ \_ , que representa las entradas de la tabla de atributos de la malla. Especifique **null** para recuperar el valor de pAttribTableSize.

</dd> <dt>

*pAttribTableSize* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)\***

Puntero al número de entradas almacenadas en pAttribTable o un valor que se va a rellenar con el número de entradas almacenadas en la tabla de atributos de la malla.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores que aparecen en los [códigos de retorno de Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Observaciones

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con distintas texturas, Estados de representación, materiales, etc. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado al dibujar el marco.

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

 

 
