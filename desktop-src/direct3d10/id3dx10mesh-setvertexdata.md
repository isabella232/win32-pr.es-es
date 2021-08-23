---
description: Establezca los datos de vértice en uno de los búferes de vértice de la malla.
ms.assetid: 930cbc49-4202-431f-ac72-386c31acd87e
title: Método ID3DX10Mesh::SetVertexData (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetVertexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 59dc5292d5d5dfc269f97f2a8d19ce9a19ea95ceefda47eaf89ac77f81838f92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990335"
---
# <a name="id3dx10meshsetvertexdata-method"></a>Método ID3DX10Mesh::SetVertexData

Establezca los datos de vértice en uno de los búferes de vértice de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetVertexData(
  [in]       UINT iBuffer,
  [in] const void *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*iBuffer* \[ En\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Búfer de vértices que se va a rellenar con pData.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Tipo: **const \* void**

Datos de vértice que se establecerán.

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

 

 
