---
title: Clase IMemoryAllocator
description: Implementado por el asignador de memoria para la función StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Almacenamiento estructurado de la clase IMemoryAllocator
- Clase IMemoryAllocator almacenamiento estructurado, descrito
topic_type:
- apiref
api_name:
- IMemoryAllocator
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 421162fd0ee6228f1dbae03eeb52e5643b0e0b15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422366"
---
# <a name="imemoryallocator-class"></a>Clase IMemoryAllocator

La clase **IMemoryAllocator** se implementa mediante el asignador de memoria para la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="methods"></a>Métodos



| Nombre                                                     | Descripción                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asignación**](imemoryallocator-allocate.md)<br/> | Asigna memoria para la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) cuando la función convierte un tipo de datos **SERIALIZEDPROPERTYVALUE** en un tipo de datos **PROPVARIANT** .<br/> |
| [**Gratuito**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Libera la memoria asignada por el método [**allocate**](imemoryallocator-allocate.md) .<br/>                                                                                                                 |



 

## <a name="remarks"></a>Observaciones

Esta clase solo la usa la función [**StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

