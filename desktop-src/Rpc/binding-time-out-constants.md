---
title: Constantes de tiempo de espera de enlace (Rpcdce.h)
description: La biblioteca RPC usa las constantes de tiempo de espera de enlace para especificar la cantidad relativa de tiempo que se debe pasar para establecer un enlace al servidor antes de dar por hecho.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476613"
---
# <a name="binding-time-out-constants"></a>Constantes de tiempo de espera de enlace

La biblioteca RPC usa las constantes de tiempo de espera de enlace para especificar la cantidad relativa de tiempo que se debe pasar para establecer un enlace al servidor antes de dar por hecho. El tiempo de espera se puede habilitar con una llamada a la [**función RpcMgmtSetComTimeout.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) La lista siguiente contiene los valores de tiempo de espera válidos.



| Constante o valor                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <dt>**RPC \_ TIEMPO \_ DE ESPERA INFINITO DE ENLACE \_ \_ DE C**</dt> <dt> 10</dt> </dl> | Sigue intentando establecer comunicaciones para siempre.<br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <dt>**RPC \_ C \_ BINDING \_ MIN \_ TIMEOUT**</dt> <dt>0</dt> </dl>                   | Prueba la cantidad mínima de tiempo para el protocolo de red que se está utilizando. Este valor favorece el tiempo de respuesta sobre la corrección a la hora de determinar si el servidor se está ejecutando.<br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <dt>**RPC \_ TIEMPO \_ DE ESPERA PREDETERMINADO DE ENLACE \_ \_ DE C**</dt> <dt>5</dt> </dl>       | Intenta una cantidad media de tiempo para el protocolo de red que se está utilizando. Este valor proporciona la corrección para determinar si un servidor se está ejecutando y proporciona el mismo peso al tiempo de respuesta. Este es el valor predeterminado.<br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <dt>**RPC \_ TIEMPO \_ DE ESPERA MÁXIMO DE ENLACE \_ \_ DE C**</dt> <dt>9</dt> </dl>                   | Intenta la mayor cantidad de tiempo para el protocolo de red que se usa. Este valor favorece la corrección a la hora de determinar si un servidor se ejecuta durante el tiempo de respuesta.<br/>                                            |



## <a name="remarks"></a>Observaciones

Los valores de la tabla anterior no están en segundos. Estos valores representan una cantidad relativa de tiempo en una escala de cero a 10. Para obtener más información sobre cómo evitar retrasos de comunicación, consulte Prevención de los errores de espera del lado cliente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





