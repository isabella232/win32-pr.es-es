---
title: IMemoryAllocator allocate (método)
description: El método allocate asigna memoria para la función StgConvertPropertyToVariant cuando la función convierte un tipo de datos SERIALIZEDPROPERTYVALUE en un tipo de datos PROPVARIANT.
ms.assetid: aa9c9308-fb55-405c-901a-9d5abfac5395
keywords:
- Asignar almacenamiento estructurado de método
- Asignar almacenamiento estructurado de método, interfaz IMemoryAllocator
- IMemoryAllocator interface Structured Storage, allocate (método)
topic_type:
- apiref
api_name:
- IMemoryAllocator.Allocate
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ee4b220e1c1e14ceed685e9b2adc694a44d2e4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105665913"
---
# <a name="imemoryallocatorallocate-method"></a>IMemoryAllocator:: Allocate (método)

El método **allocate asigna** memoria para la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) cuando la función convierte un tipo de datos **SERIALIZEDPROPERTYVALUE** en un tipo de datos **PROPVARIANT** .

## <a name="syntax"></a>Sintaxis


```C++
virtual void* Allocate(
  [in] ULONG cbSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*cbSize* \[ de\]
</dt> <dd>

Especifica el tamaño de la memoria que se va a asignar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

