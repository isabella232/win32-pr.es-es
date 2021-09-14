---
title: Marcas de registro de interfaz (Rpcdce.h)
description: Las siguientes constantes se usan en el parámetro Flags de las funciones RpcServerRegisterIf2 y RpcServerRegisterIfEx.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba4a94fe1100db3cb332d85593ea42617657119
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244592"
---
# <a name="interface-registration-flags"></a>Marcas de registro de interfaz

Las siguientes constantes se usan en el *parámetro Flags* de las [**funciones RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) y [**RpcServerRegisterIfEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex)




| Constante | Descripción | 
|----------|-------------|
| <span id="0"></span><dl><dt><strong>0</strong></dt></dl> | Semántica de interfaz estándar.<br /> | 
| <span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt></dl> | Cuando se registra esta marca de interfaz, el tiempo de ejecución de RPC invoca la devolución de llamada de seguridad registrada para todas las llamadas, independientemente de la identidad, la secuencia de protocolo o el nivel de autenticación del cliente.<br /><blockquote>[!Note]<br />Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1. Cuando no se establece esta marca, RPC filtra automáticamente todas las llamadas no autenticadas antes de que lleguen a la devolución de llamada de seguridad.</blockquote><br /> | 
| <span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt></dl> | Cuando se registra esta marca de interfaz, el tiempo de ejecución rpc rechaza las llamadas realizadas por clientes remotos. Todas las llamadas locales que usan ncadg_* y ncacn_* también se rechazan, a excepción de ncacn_np. RPC permite ncacn_NP llamadas solo si la llamada no procede de SRV. Las llamadas desde ncalrpc siempre se procesan.<br /><blockquote>[!Note]<br />Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.</blockquote><br /> | 
| <span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl><dt><strong>RPC_IF_AUTOLISTEN</strong></dt></dl> | Se trata de una <strong>interfaz de escucha</strong> automática. El tiempo de ejecución comienza a escuchar llamadas en cuanto se registra la primera interfaz autolisten y deja de escuchar cuando se anula el registro de la última interfaz de lista automática.<br /> | 
| <span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl><dt><strong>RPC_IF_OLE</strong></dt></dl> | Reservado para OLE. No use esta marca.<br /> | 
| <span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt></dl> | No implementado actualmente.<br /> | 
| <span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt></dl> | Limita las conexiones a los clientes que usan un nivel de autorización superior a RPC_C_AUTHN_LEVEL_NONE. La especificación de esta marca permite que los clientes pasen por la <strong>sesión NULL.</strong> En Windows XP y Windows Server 2003, estos clientes no se permiten. Los clientes que no se RPC_IF_ALLOW_SECURE_ONLY prueba reciben un RPC_S_ACCESS_DENIED error. El uso RPC_IF_ALLOW_SECURE_ONLY marca no implica ni garantiza un alto nivel de privilegios por parte del usuario que realiza la llamada. RPC solo comprueba que el usuario tiene credenciales válidas; El usuario que realiza la llamada puede usar la cuenta de invitado u otras cuentas con pocos privilegios. No asuma privilegios elevados cuando RPC_IF_ALLOW_SECURE_ONLY se usa.<br /><strong>Windows NT 4.0 y Windows Me/98/95:</strong><br /> | 
| <span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt></dl> | Deshabilita el almacenamiento en caché de devolución de llamada de seguridad, forzando una devolución de llamada de seguridad para cada llamada RPC en una interfaz determinada.<br /><blockquote>[!Note]<br />Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.</blockquote><br /> | 




## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce.h</dt> </dl> |



 

 





