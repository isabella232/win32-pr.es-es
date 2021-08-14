---
title: UUID
description: Proporciona una designación única de un objeto como una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 31ff8eb22a234020e0da5b5ebb5799d5ddb0c8d1dca7bc094394f79a5ceb0c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925952"
---
# <a name="uuid-structure"></a>UUID (estructura)

La **estructura UUID** define un identificador único universal (UUID). Un **UUID** proporciona una designación única de un objeto como una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.

La **estructura UUID** es un `typedef` sinónimo 'd de la estructura [GUID.](/windows/win32/api/guiddef/ns-guiddef-guid)

## <a name="syntax"></a>Sintaxis

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Comentarios

Las bibliotecas rpc en tiempo de ejecución usan **UUID** para comprobar la compatibilidad entre clientes y servidores, y para seleccionar entre varias implementaciones de una interfaz.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | Se define en rpcdce.h; include rpc.h |

## <a name="see-also"></a>Consulte también

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 [UUID \_ VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)