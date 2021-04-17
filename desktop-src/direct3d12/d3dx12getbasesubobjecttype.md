---
title: Función D3DX12GetBaseSubobjectType (D3dx12. h)
description: Devuelve el tipo de subobjeto que corresponde a la clase base del tipo de subobjeto pasado.
ms.assetid: 3744B042-094C-4EA4-8185-A018B728D843
keywords:
- D3DX12GetBaseSubobjectType función)
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
ms.openlocfilehash: 0b39f1c61be682d55512772bef1258aecdb009a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105707755"
---
# <a name="d3dx12getbasesubobjecttype-function"></a>D3DX12GetBaseSubobjectType función)

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

Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de canalización D3D12**

Un valor de enumeración que especifica el tipo de subobjeto que le interesa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **\_ \_ \_ \_ tipo de subobjeto de estado de canalización D3D12**

Si *SubobjectType* corresponde a un tipo de datos de subobjeto que se deriva de otro tipo de datos de subobjeto, se devuelve el tipo de subobjeto del tipo de datos base de subobjeto; de lo contrario, se devuelve el tipo de subobjeto pasado. Por ejemplo, si se pasa el **\_ tipo de subobjeto de estado de canalización D3D12 \_ \_ \_ \_ Depth \_ STENCIL1** , se devuelve **D3D12 el \_ \_ \_ \_ tipo \_ \_ de subobjeto de estado de canalización** .

## <a name="remarks"></a>Observaciones

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| Archivo DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Funciones auxiliares de D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





