---
title: RPC_STATUS (Rpcdce.h)
description: El tipo de datos RPC \_ STATUS representa un tipo de código de estado específico de la plataforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473576"
---
# <a name="rpc_status"></a>ESTADO \_ DE RPC

El tipo de datos **RPC \_ STATUS** representa un tipo de código de estado específico de la plataforma.


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a>Observaciones

La mayoría de las funciones RPC devuelven el tipo **RPC \_ STATUS** y forma parte de la definición del tipo de función [**RPC OBJECT \_ \_ INQ \_ FN.**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h (incluir Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RPC \_ OBJECT \_ INQ \_ FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





