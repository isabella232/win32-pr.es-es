---
title: Constantes de opción de enlace (Rpcdce. h)
description: Las aplicaciones establecen las constantes de la opción de enlace para controlar el modo en que la biblioteca en tiempo de ejecución de RPC procesa las llamadas a procedimientos remotos. En la tabla siguiente se enumeran las propiedades de enlace y los valores constantes pertinentes para las propiedades de enlace.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996168"
---
# <a name="binding-option-constants"></a>Constantes de opción de enlace

Las aplicaciones establecen las constantes de la opción de enlace para controlar el modo en que la biblioteca en tiempo de ejecución de RPC procesa las llamadas a procedimientos remotos. En la tabla siguiente se enumeran las propiedades de enlace y los valores constantes pertinentes para las propiedades de enlace.

> [!Note]  
> Todas las opciones de cola de mensajes (MQ) de la tabla siguiente solo son válidas para Windows 2000. Windows XP y versiones posteriores no admiten Message Queue Server. No se recomienda a los desarrolladores utilizar Message Queue Server.

 



| Constante o valor                                                                                                                                                                                                                                                        | Descripción                                                                                                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_OPT_BINDING_NONCAUSAL"></span><span id="rpc_c_opt_binding_noncausal"></span><dl> <dt>**RPC \_ C \_ elegir \_ enlace no \_ causal**</dt> <dt>9</dt> </dl>     | Predeterminada. Si **es false**, orden de llamadas causal. Las llamadas RPC se ejecutan en un orden estricto de envío. Vea la sección Comentarios.<br/> Si **es true**, orden de llamadas no causal. Las llamadas RPC se ejecutan de forma independiente. Vea la sección Comentarios.<br/>                                                                        |
| <span id="RPC_C_OPT_MAX_OPTIONS"></span><span id="rpc_c_opt_max_options"></span><dl> <dt>**RPC \_ Opciones de C \_ OPC \_ máx \_**</dt> . <dt>17</dt> </dl>                      | No es necesario para los programas de aplicación. Microsoft lo usa internamente.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_DONT_FAIL"></span><span id="rpc_c_dont_fail"></span><dl> <dt>**RPC \_ C \_ \_ no**</dt> se puede producir el error <dt>4</dt> </dl>                                          | No es necesario para los programas de aplicación. Microsoft lo usa internamente.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_SESSION_ID"></span><span id="rpc_c_opt_session_id"></span><dl> <dt>**RPC \_ C \_ OPT \_ \_ ID. de sesión**</dt> <dt>6</dt> </dl>                          | Si es **true**, se genera un identificador de sesión para cada conexión.<br/>                                                                                                                                                                                                                                |
| <span id="RPC_C_OPT_COOKIE_AUTH"></span><span id="rpc_c_opt_cookie_auth"></span><dl> <dt>**RPC \_ \_ \_ \_ Autenticación de cookies**</dt> <dt>7</dt> de C </dl>                       | Si **es true**, la autenticación basada en cookies de cliente se utiliza para las conexiones. Un puntero a la estructura de [**\_ \_ \_ \_ \_ descriptor de autenticación de cookies de RPC C opt**](/windows/desktop/api/Rpcdcep/ns-rpcdcep-rpc_c_opt_cookie_auth_descriptor) se pasa como el parámetro *OptionValue* en [**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption).<br/> |
| <span id="RPC_C_OPT_RESOURCE_TYPE_UUID"></span><span id="rpc_c_opt_resource_type_uuid"></span><dl> <dt>**RPC \_ Tipo de recurso de C \_ OPC \_ \_ \_ UUID**</dt> <dt>8</dt> </dl> | No es necesario para los programas de aplicación. Microsoft lo usa internamente.<br/>                                                                                                                                                                                                                         |
| <span id="RPC_C_OPT_DONT_LINGER"></span><span id="rpc_c_opt_dont_linger"></span><dl> <dt>**RPC \_ C \_ OPT \_ no \_ persistente**</dt> <dt>13</dt> </dl>                      | Si **es true**, se libera el cierre forzado de la Asociación después del último identificador de enlace o identificador de contexto.<br/>                                                                                                                                                                                |
| <span id="RPC_C_OPT_UNIQUE_BINDING"></span><span id="rpc_c_opt_unique_binding"></span><dl> <dt>**RPC \_ C \_ OPT \_ \_ enlace único**</dt> <dt>11</dt> </dl>             | Cuando se establece en **true**, RPC no reutiliza las conexiones existentes. Se abre un identificador de enlace único para cada conexión y el estado se mantiene para cada identificador de enlace único.<br/>                                                                                                               |



## <a name="remarks"></a>Observaciones

De forma predeterminada, la biblioteca en tiempo de ejecución de RPC ejecuta las llamadas en un identificador de enlace determinado desde cada subproceso de una aplicación en orden estricto de envío. Esto no garantiza que se serialicen las llamadas de distintos subprocesos en el mismo identificador de enlace. Las aplicaciones multiproceso deben serializar sus llamadas RPC. Si este comportamiento es demasiado restrictivo, puede habilitar el orden no causal. Cuando lo hace, la biblioteca en tiempo de ejecución de RPC ejecuta llamadas de manera independiente. No impone ninguna ordenación en su envío.

Un ejemplo de una aplicación que podría encontrar una ordenación no causal útil es un programa multiproceso cuyos subprocesos realizan llamadas en el mismo identificador de enlace. Del mismo modo, un programa que use varias llamadas asincrónicas en un controlador de enlace encontrará una ordenación no causal de una opción adecuada. Otro ejemplo podría ser un programa proxy de Internet que utiliza un único subproceso para controlar las solicitudes de varios clientes. En cada uno de estos casos, sería extremadamente restrictivo intentar serializar las llamadas a procedimiento remoto.

La opción no **persistente de RPC \_ C \_ OPT \_ \_** no se puede establecer solo en los identificadores de enlace que utilizan las secuencias de protocolo **ncalrpc** o **ncacn \_ \** _. No se puede usar en secuencias de protocolo _*ncadg \_ \**_ . Se debe llamar a la función [_ *RpcBindingSetOption* *](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption) con esta opción en un controlador de enlace en el que se haya realizado al menos una llamada RPC. Si no se ha realizado ninguna llamada RPC en el controlador de enlace, la llamada a la función **RpcBindingSetOption** devuelve un **\_ \_ \_ tipo \_ de \_ enlace RPC erróneo** . La opción surte efecto en toda la asociación, independientemente del número de identificadores de enlace que se adjunten a la asociación. Puesto que se comprueba antes de que se destruya la asociación, se puede establecer en cualquier momento antes de que se cierre el identificador de enlace.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                                                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                                                                 |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h; </dt> <dt>Rpcdcep. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[Administración de conjuntos de conexiones de red (asociaciones)](managing-network-connection-sets-associations-.md)
</dt> </dl>

 

 





