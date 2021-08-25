---
title: Método IMemoryAllocator Free
description: El método Free libera la memoria asignada por el método Allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Método gratuito Structured Storage
- Método gratuito Structured Storage , interfaz IMemoryAllocator
- Interfaz IMemoryAllocator Structured Storage , método Free
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f78690a37b5500f5e540cf4c2ef516b7c3ea89c219ba475dc5e5ac030f775d81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119906175"
---
# <a name="imemoryallocatorfree-method"></a>IMemoryAllocator::Free (Método)

El **método Free** libera la memoria asignada por el método [**Allocate.**](imemoryallocator-allocate.md)

## <a name="syntax"></a>Sintaxis


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Pv* 
</dt> <dd>

Puntero a la memoria que se va a liberar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32.lib</dt> </dl> |



 

 





