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
ms.openlocfilehash: 75723819ab7a4f82f25a68dfc2f0017e8b871130a8e0fbe70c939a95de221426
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753105"
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

Una tabla de atributos se usa para identificar las áreas de la malla que deben dibujarse con diferentes texturas, estados de representación, materiales, entre otras. Además, la aplicación puede usar la tabla de atributos para ocultar partes de una malla sin dibujar un identificador de atributo determinado (AttribId) al dibujar el marco.

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

 

 
