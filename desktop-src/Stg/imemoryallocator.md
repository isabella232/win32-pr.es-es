---
title: IMemoryAllocator (clase)
description: Implementado por el asignador de memoria para la función StgConvertPropertyToVariant.
ms.assetid: a0735b62-5ed3-42df-a320-b58c742645a8
keywords:
- Clase IMemoryAllocator Structured Storage
- Clase IMemoryAllocator structured Storage , descrita
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
ms.openlocfilehash: d3a92cb2fa31b937a86acd80d2e7be9c83fb1d01476a2f50a856494d8f2a0d35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961760"
---
# <a name="imemoryallocator-class"></a>IMemoryAllocator (clase)

El asignador de memoria implementa la clase **IMemoryAllocator** para la [**función StgConvertPropertyToVariant.**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)

## <a name="methods"></a>Métodos



| Nombre                                                     | Descripción                                                                                                                                                                                                        |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Asignar**](imemoryallocator-allocate.md)<br/> | Asigna memoria para la [**función StgConvertPropertyToVariant**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant) cuando la función convierte un tipo de datos **SERIALIZEDPROPERTYVALUE** en un tipo de **datos PROPVARIANT.**<br/> |
| [**Gratis**](/windows/desktop/api/vswriter/nf-vswriter-cvsswriter-initialize)<br/>        | Libera la memoria asignada por el [**método Allocate.**](imemoryallocator-allocate.md)<br/>                                                                                                                 |



 

## <a name="remarks"></a>Comentarios

Esta clase solo la usa la [**función StgConvertPropertyToVariant.**](/windows/desktop/api/propidl/nf-propidl-stgconvertpropertytovariant)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

