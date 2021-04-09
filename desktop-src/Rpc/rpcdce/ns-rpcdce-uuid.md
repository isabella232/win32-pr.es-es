---
title: UUID
description: Proporciona una designación única de un objeto como, por ejemplo, una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/09/2019
ms.openlocfilehash: 95d2d420502a5d92af64c902ffa82c709639d872
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148983"
---
# <a name="uuid-structure"></a>UUID (estructura)

La estructura de **UUID** define un identificador único universal (UUID). Un **UUID** proporciona una designación única de un objeto como una interfaz, un vector de punto de entrada de administrador o un objeto de cliente.

La estructura de **UUID** es un `typedef` sinónimo de la estructura [GUID](/windows/win32/api/guiddef/ns-guiddef-guid) .

## <a name="syntax"></a>Sintaxis

```cpp
typedef GUID UUID;
```

## <a name="remarks"></a>Observaciones

Las bibliotecas en tiempo de ejecución de RPC usan **UUID** para comprobar la compatibilidad entre los clientes y los servidores, y para seleccionar entre varias implementaciones de una interfaz.

## <a name="requirements"></a>Requisitos

| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | Definido en rpcdce. h; incluir RPC. h |

## <a name="see-also"></a>Vea también

[GUID](/windows/win32/api/guiddef/ns-guiddef-guid) 
 de [UUID \_ VECTOR](/windows/win32/api/rpcdce/ns-rpcdce-uuid_vector)