---
title: RPC_NS_HANDLE (Rpcnsi. h)
description: El tipo de datos \_ \_ identificador de RPC NS define un identificador de servicio de nombres.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535104"
---
# <a name="rpc_ns_handle"></a>identificador de RPC \_ NS \_

El tipo de **datos \_ \_ identificador de RPC NS** define un identificador de servicio de nombres.


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a>Observaciones

Un identificador de servicio de nombre es una variable opaca que contiene información que la biblioteca en tiempo de ejecución de RPC utiliza para devolver los siguientes datos de RPC desde la base de datos de nombre-servicio:

-   Identificadores de enlace de servidor
-   UUID de recursos ofrecidos por los miembros del perfil de servidor
-   Miembros del grupo

El ámbito de un identificador de servicio de nombre es de una rutina "begin" a través de la rutina "Done" correspondiente.

Las aplicaciones son responsables del control de simultaneidad de los identificadores de servicio de nombre entre subprocesos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                |
| Encabezado<br/>                   | <dl> <dt>Rpcnsi. h (incluir RPC. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

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

 

 





