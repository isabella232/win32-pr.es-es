---
title: RPC_NS_HANDLE (Rpcnsi.h)
description: El tipo de datos RPC \_ NS \_ HANDLE define un identificador de servicio de nombre.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7612671b03f507bc2e722520fa775e0e999d0f1456ebfcefa971bba27b65dbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926289"
---
# <a name="rpc_ns_handle"></a>IDENTIFICADOR \_ DE NS \_ RPC

El tipo de **datos RPC \_ NS \_ HANDLE** define un identificador de servicio de nombre.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Comentarios

Un identificador de servicio de nombre es una variable opaca que contiene información que la biblioteca en tiempo de ejecución rpc usa para devolver los siguientes datos RPC de la base de datos name-service:

-   Identificadores de enlace de servidor
-   UUID de los recursos ofrecidos por los miembros del perfil de servidor
-   Miembros del grupo

El ámbito de un identificador de servicio de nombre es de una rutina "Begin" a través de la rutina "Done" correspondiente.

Las aplicaciones son responsables del control de simultaneidad de los identificadores de servicio de nombre entre subprocesos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcnsi.h (incluir Rpc.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[**RpcNsBindingLookupDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





