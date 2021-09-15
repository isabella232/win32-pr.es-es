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
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473565"
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

 

