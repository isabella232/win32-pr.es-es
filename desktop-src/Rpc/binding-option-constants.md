---
title: Constantes de opción de enlace (Rpcdce.h)
description: Las aplicaciones establecen las constantes de opción de enlace para controlar cómo la biblioteca en tiempo de ejecución rpc procesa las llamadas a procedimiento remoto. En la tabla siguiente se enumeran cada propiedad de enlace y los valores constantes pertinentes para las propiedades de enlace.
ms.assetid: ff88e05d-b9f3-42ef-a44f-fee9261832c8
topic_type:
- apiref
api_name:
- RPC_C_OPT_BINDING_NONCAUSAL
- RPC_C_OPT_MAX_OPTIONS
- RPC_C_DONT_FAIL
- RPC_C_OPT_SESSION_ID
- RPC_C_OPT_COOKIE_AUTH
- RPC_C_OPT_RESOURCE_TYPE_UUID
- RPC_C_OPT_DONT_LINGER
- RPC_C_OPT_UNIQUE_BINDING
api_location:
- Rpcdce.h
- Rpcdcep.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52152b5ddcc17abe5c698697e30f1f1a512ee4f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069163"
---
# <a name="binding-option-constants"></a>Constantes de opción de enlace

Las aplicaciones establecen las constantes de opción de enlace para controlar cómo la biblioteca en tiempo de ejecución rpc procesa las llamadas a procedimiento remoto. En la tabla siguiente se enumeran cada propiedad de enlace y los valores constantes pertinentes para las propiedades de enlace.

> [!Note]  
> Todas las opciones de cola de mensajes (MQ) de la tabla siguiente son válidas solo Windows 2000. Windows XP y versiones posteriores no admiten la cola de mensajes. No se recomienda a los desarrolladores usar la cola de mensajes.

 



| Constante o valor                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ OPT \_ BINDING \_ NONCAUSAL**</dt> <dt>9</dt> </dl>     | Predeterminada. Si **es FALSE,** la ordenación de llamadas causales. Las llamadas RPC se ejecutan en orden estricto de envío. Vea la sección Comentarios.<br/> Si **es TRUE,** el orden de las llamadas no válidos. Las llamadas RPC se ejecutan de forma independiente. Vea la sección Comentarios.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ OPCIONES \_ \_ MÁXIMAS DE C \_ OPT**</dt> <dt>17</dt> </dl>                      | No es necesario para los programas de aplicación. Usado internamente por Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ ERROR DE C \_ DONT \_**</dt> <dt>4</dt> </dl>                                          | No es necesario para los programas de aplicación. Usado internamente por Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ IDENTIFICADOR \_ DE SESIÓN \_ \_ DE C OPT**</dt> <dt>6</dt> </dl>                          | Si **es TRUE,** se genera un identificador de sesión para cada conexión.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ C \_ OPT \_ COOKIE \_ AUTH**</dt> <dt>7</dt> </dl>                       | Si **es TRUE,** se usa la autenticación basada en cookies del lado cliente para las conexiones. Un puntero a la estructura [**RPC C OPT COOKIE \_ \_ \_ \_ AUTH \_ DESCRIPTOR**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) se pasa como el *parámetro OptionValue* [**en RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ C \_ OPT RESOURCE TYPE \_ \_ \_ UUID**</dt> <dt>8</dt> </dl> | No es necesario para los programas de aplicación. Usado internamente por Microsoft.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ OPT \_ DONT \_ LINGER**</dt> <dt>13</dt> </dl>                      | Si **es TRUE,** fuerce el cierre de la asociación después de liberar el último identificador de enlace o identificador de contexto en ella.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ OPT \_ UNIQUE \_ BINDING**</dt> <dt>11</dt> </dl>             | Cuando se establece en **true,** RPC no reutiliza las conexiones existentes. Se abre un identificador de enlace único para cada conexión y se mantiene el estado para cada identificador de enlace único.<br/>                                                                                                               |



## <a name="remarks"></a>Observaciones

De forma predeterminada, la biblioteca en tiempo de ejecución rpc ejecuta las llamadas en un identificador de enlace determinado desde cada subproceso de una aplicación en orden estricto de envío. Esto no garantiza que se serializan las llamadas de subprocesos diferentes en el mismo identificador de enlace. Las aplicaciones multiproceso deben serializar sus llamadas RPC. Si este comportamiento es demasiado restrictivo, puede habilitar la ordenación no restrictiva. Al hacerlo, la biblioteca en tiempo de ejecución de RPC ejecuta llamadas de forma independiente. No impone ninguna ordenación en su envío.

Un ejemplo de una aplicación que podría resultar útil para la ordenación no importante es un programa multiproceso cuyos subprocesos hacen llamadas en el mismo identificador de enlace. De forma similar, un programa que usa varias llamadas asincrónicas en un identificador de enlace encontrará una opción práctica de ordenación no segura. Otro ejemplo podría ser un programa de proxy de Internet que usa un único subproceso para controlar las solicitudes de varios clientes. En cada uno de estos casos, sería muy restrictivo intentar serializar las llamadas a procedimiento remoto.

La **opción RPC C OPT \_ \_ \_ DONT \_ LINGER** solo se puede establecer en identificadores de enlace que usan las secuencias de protocolo **ncalrpc** o **\_ \* ncacn_.* No se puede usar en secuencias de protocolo _*ncadg. \_ \**_ Se debe llamar a la función [_ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con esta opción en un identificador de enlace en el que se haya realizado al menos una llamada RPC. Si no se ha realizado ninguna llamada RPC en el identificador de enlace, **RPC S WRONG KIND OF \_ \_ \_ \_ \_ BINDING** se devuelve desde la llamada de función **RpcBindingSetOption.** La opción entra en vigor para toda la asociación, independientemente del número de identificadores de enlace asociados a la asociación. Puesto que se comprueba antes de que se destruya la asociación, se puede establecer en cualquier momento antes de que se cierre el identificador de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                 |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h; </dt> <dt>Rpcdcep.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Administración de conjuntos de conexiones de red (asociaciones)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





