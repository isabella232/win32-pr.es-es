---
title: Función D3DX12GetBaseSubobjectType (D3dx12.h)
description: Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- Función D3DX12GetBaseSubobjectType
topic_type:
- apiref
api_name:
- D3DX12GetBaseSubobjectType
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33bd49b47e9fe603c0ebbdca015f3997eb06558a7039ddc866fb4d4667b8802b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989805"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>Función D3DX12GetBaseSubobjectType

Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.

## <a name="syntax"></a>Sintaxis


```C++
D3D12_PIPELINE_STATE_SUBOBJECT_TYPE inline D3DX12GetBaseSubobjectType(
   D3D12_PIPELINE_STATE_SUBOBJECT_TYPE SubobjectType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SubobjectType* 
</dt> <dd>

Tipo: **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE**

Valor de enumeración que especifica el tipo de subobjeto que le interesa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT \_ TYPE**

Si *SubobjectType corresponde* a un tipo de datos de subobjeto derivado de otro tipo de datos de subobjeto, se devuelve el tipo de subobjeto del tipo de datos de subobjeto base; De lo contrario, se devuelve el tipo de subobjeto pasado. Por ejemplo, si se pasa **D3D12 \_ PIPELINE \_ STATE \_ SUBOBJECT TYPE DEPTH \_ \_ \_ STENCIL1,** se devuelve **D3D12 \_ PIPELINE STATE \_ \_ SUBOBJECT TYPE DEPTH \_ \_ \_ STENCIL.**

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





