---
title: UUID
description: Proporciona una designación única de un objeto como una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580185"
---
# <a name="uuid-structure"></a>UUID (estructura)

La **estructura UUID** define un identificador único universal (UUID). Un **UUID** proporciona una designación única de un objeto como una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.

La **estructura UUID** es un `typedef` sinónimo 'd de la estructura [GUID.](/windows/win32/api/guiddef/ns-guiddef-guid)

## <a name="syntax"></a>Sintaxis

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Observaciones

Las bibliotecas en tiempo de ejecución de RPC usan **UUID** para comprobar la compatibilidad entre clientes y servidores, y para seleccionar entre varias implementaciones de una interfaz.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | Se define en rpcdce.h; include rpc.h |

## <a name="see-also"></a>Vea también

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)