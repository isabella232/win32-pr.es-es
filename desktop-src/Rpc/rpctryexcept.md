---
title: RpcTryExcept (Rpc.h)
description: La instrucción RpcTryExcept proporciona un control estructurado de excepciones para las aplicaciones RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RpcTryExcept RPC
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c7a73ca80eb342b9a23fcaa4b922afe8d19f00e1f22ab82f8c6027ecc43d76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925972"
---
# <a name="rpctryexcept"></a>RpcTryExcept

La **instrucción RpcTryExcept proporciona** un control estructurado de excepciones para las aplicaciones RPC. Si alguna de las instrucciones de programa de **RpcTryExcept** produce una excepción, se ejecutan las instrucciones del bloque de código [**RpcExcept.**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) La **instrucción RpcEndExcept** debe terminar todas las instrucciones [**RpcTryExcept.**](/previous-versions/aa375629(v=vs.80))

Para obtener más información, [**vea RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).

**Windows Vista** y versiones posteriores de Windows:[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) se recomienda para el control de excepciones estructurado para las excepciones más comunes como alternativa a los filtros personalizados [**con RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).  

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Rpc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[**RpcTryFinally**](rpctryfinally.md)
</dt> </dl>

 

