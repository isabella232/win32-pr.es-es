---
description: Establecer los datos de índice de la malla.
ms.assetid: f3e7e166-94b5-45f6-9d43-8d7e32b7b523
title: 'ID3DX10Mesh:: SetIndexData (método) (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.SetIndexData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: f561a4109fbab2163b2ec51e95b45a618da5b6d5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105718363"
---
# <a name="id3dx10meshsetindexdata-method"></a>ID3DX10Mesh:: SetIndexData (método)

Establecer los datos de índice de la malla.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetIndexData(
  [in] const void *pData,
  [in]       UINT cIndices
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pdata* \[ de\]
</dt> <dd>

Tipo: **const void \***

Los datos del índice.

</dd> <dt>

*cIndices* \[ de\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Número de índices en pData.

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

 

 
