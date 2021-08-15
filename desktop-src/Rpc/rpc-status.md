---
title: RPC_STATUS (Rpcdce.h)
description: El tipo de datos RPC \_ STATUS representa un tipo de código de estado específico de la plataforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93cc6f682dbb46b65fc261b738b94e8000f3a77d96c4bd65d1fead4bf8c0e17a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925992"
---
# <a name="rpc_status"></a>ESTADO \_ DE RPC

El tipo de datos **RPC \_ STATUS** representa un tipo de código de estado específico de la plataforma.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Comentarios

La mayoría de las funciones RPC devuelven el tipo **RPC \_ STATUS** y forma parte de la definición del tipo de función [**RPC OBJECT \_ \_ INQ \_ FN.**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RPC \_ OBJECT \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





