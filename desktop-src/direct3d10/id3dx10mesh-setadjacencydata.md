---
description: Establezca los datos de adyacencia de la malla.
ms.assetid: 67d51ce0-7fe2-484d-9874-f1fa59632d59
title: Método ID3DX10Mesh::SetAdjacencyData (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetAdjacencyData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 8e183fb6fad07b92d8bca15654456ca1d31a11839af033222803044f8207a14f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990385"
---
# <a name="id3dx10meshsetadjacencydata-method"></a>Método ID3DX10Mesh::SetAdjacencyData

Establezca los datos de adyacencia de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetAdjacencyData(
  [in] const UINT *pAdjacency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAdjacency* \[ En\]
</dt> <dd>

Tipo: **const [**UINT**](../winprog/windows-data-types.md) \***

Datos de adyacencia que se establecerán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

El valor devuelto es uno de los valores enumerados en Códigos de retorno de [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

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

 

 
