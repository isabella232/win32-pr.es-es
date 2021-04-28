---
description: 'Método ID3DX10Mesh::D rawSubset: dibuja un subconjunto de una malla.'
ms.assetid: e785949e-fcda-4ef9-b50a-193cd954e97d
title: Método ID3DX10Mesh::D rawSubset (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubset
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8441bfe4c5d965733a40816ff2def1015f3eb79c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084043"
---
# <a name="id3dx10meshdrawsubset-method"></a>Método ID3DX10Mesh::D rawSubset

Dibuja un subconjunto de una malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DrawSubset(
  [in] UINT AttribId
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AttribId* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Especifica qué subconjunto de la malla se va a dibujar. Este valor se usa para diferenciar las caras de una malla como pertenecientes a uno o varios grupos de atributos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentarios

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla no dibujando un identificador de atributo determinado (AttribId) al dibujar el marco.

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

 

 
