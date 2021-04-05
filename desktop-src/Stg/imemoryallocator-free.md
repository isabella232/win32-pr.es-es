---
title: IMemoryAllocator Free (método)
description: El método Free libera la memoria asignada por el método allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Almacenamiento estructurado de método gratuito
- Método gratuito de almacenamiento estructurado, interfaz IMemoryAllocator
- IMemoryAllocator interface Structured Storage, Free (método)
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
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078970"
---
# <a name="imemoryallocatorfree-method"></a>IMemoryAllocator:: Free (método)

El método **Free** libera la memoria asignada por el método [**allocate**](imemoryallocator-allocate.md) .

## <a name="syntax"></a>Sintaxis


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FV* 
</dt> <dd>

Puntero a la memoria que se va a liberar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Biblioteca<br/>                  | <dl> <dt>Ole32. lib</dt> </dl> |



 

 





