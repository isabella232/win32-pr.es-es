---
title: Constantes de tiempo de espera de enlace (Rpcdce. h)
description: La biblioteca RPC utiliza las constantes de tiempo de espera de enlace para especificar la cantidad relativa de tiempo que se debe gastar para establecer un enlace con el servidor antes de abandonarlo.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676687"
---
# <a name="binding-time-out-constants"></a>Constantes de tiempo de espera de enlace

La biblioteca RPC utiliza las constantes de tiempo de espera de enlace para especificar la cantidad relativa de tiempo que se debe gastar para establecer un enlace con el servidor antes de abandonarlo. El tiempo de espera se puede habilitar con una llamada a la función [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) . La lista siguiente contiene los valores de tiempo de espera válidos.



| Constante o valor                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ \_Tiempo de \_ \_ espera infinito de enlace C**</dt> <dt> 10</dt> </dl> | Sigue intentando establecer comunicaciones indefinidamente.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ \_Tiempo de \_ \_ espera mínimo de enlace C**</dt> <dt>0</dt> </dl>                   | Intenta la cantidad mínima de tiempo para el protocolo de red que se va a usar. Este valor favorece el tiempo de respuesta con respecto a la corrección a la hora de determinar si el servidor se está ejecutando.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ \_Tiempo de \_ \_ espera predeterminado de enlace de C**</dt> <dt>5</dt> </dl>       | Intenta un promedio de tiempo para el protocolo de red que se utiliza. Este valor proporciona exactitud a la hora de determinar si un servidor se está ejecutando y proporciona un tiempo de respuesta igual. Este es el valor predeterminado.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ \_Tiempo de \_ \_ espera máximo de enlace de C**</dt> <dt>9</dt> </dl>                   | Intenta la cantidad más larga de tiempo para el protocolo de red que se va a usar. Este valor favorece la corrección a la hora de determinar si un servidor se está ejecutando a lo largo del tiempo de respuesta.<br/>                                            |



## <a name="remarks"></a>Observaciones

Los valores de la tabla anterior no están en segundos. Estos valores representan una cantidad de tiempo relativa en una escala de cero a 10. Para obtener más información acerca de cómo evitar los retrasos de la comunicación, consulte evitar bloqueos del lado cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





