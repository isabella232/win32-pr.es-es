---
title: RpcTryFinally (Rpc.h)
description: La instrucción RpcTryFinally proporciona control de terminación estructurado.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RpcTryFinally RPC
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67521329770abd1888356e7054b689c3f39a6293dff602a4920336760ccccb94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018095"
---
# <a name="rpctryfinally"></a>RpcTryFinally

La **instrucción RpcTryFinally proporciona** control de terminación estructurado. Se produce una excepción durante las instrucciones de ejecución del bloque de código asociado a la **instrucción RpcTryFinally** y se ejecutan las instrucciones del bloque de código asociado a la instrucción [**RpcFinally.**](/previous-versions/aa375699(v=vs.80)) Todas **las instrucciones RpcTryFinally** deben terminarse mediante [**una instrucción RpcEndFinally.**](/previous-versions/aa375634(v=vs.80))

Para obtener más información, [**vea RpcFinally**](/previous-versions/aa375699(v=vs.80)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>Rpc.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpcFinally**](/previous-versions/aa375699(v=vs.80))
</dt> <dt>

[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))
</dt> </dl>

 

