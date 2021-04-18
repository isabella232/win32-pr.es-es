---
title: RpcTryFinally (RPC. h)
description: La instrucción RpcTryFinally proporciona un control de terminación estructurado.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RPC RpcTryFinally
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491398"
---
# <a name="rpctryfinally"></a>RpcTryFinally

La instrucción **RpcTryFinally** proporciona un control de terminación estructurado. Se produce una excepción durante las instrucciones de ejecución del bloque de código asociado a la instrucción **RpcTryFinally** , se ejecutan las instrucciones del bloque de código asociado a la instrucción [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) . Todas las instrucciones **RpcTryFinally** deben terminar con una instrucción [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .

Para obtener más información, vea [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                       |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                             |
| Encabezado<br/>                   | <dl> <dt>RPC. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpcFinally**](/previous-versions/aa375699(v=vs.80))
</dt> <dt>

[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))
</dt> </dl>

 

