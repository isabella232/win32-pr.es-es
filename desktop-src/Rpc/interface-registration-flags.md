---
title: Marcas de registro de interfaz (Rpcdce. h)
description: Las constantes siguientes se usan en el parámetro flags de las funciones RpcServerRegisterIf2 y RpcServerRegisterIfEx.
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
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150959"
---
# <a name="interface-registration-flags"></a>Marcas de registro de interfaz

Las constantes siguientes se usan en el parámetro *Flags* de las funciones [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) y [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <dt><strong>0,1</strong></dt> </dl></td>
<td style="text-align: left;">Semántica de la interfaz estándar.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </dl></td>
<td style="text-align: left;">Cuando se registra esta marca de interfaz, el tiempo de ejecución de RPC invoca la devolución de llamada de seguridad registrada para todas las llamadas, independientemente de la identidad, la secuencia de protocolo o el nivel de autenticación del cliente.<br/>
<blockquote>
[!Note]<br />
Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1. Cuando no se establece esta marca, RPC filtra automáticamente todas las llamadas no autenticadas antes de que lleguen a la devolución de llamada de seguridad.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Cuando se registra esta marca de interfaz, el tiempo de ejecución de RPC rechaza las llamadas realizadas por los clientes remotos. También se rechazan todas las llamadas locales que usan secuencias de protocolo ncadg_ * y ncacn_ *, con la excepción de ncacn_np. RPC solo permite llamadas ncacn_NP si la llamada no procede de SRV. Siempre se procesan las llamadas desde ncalrpc.<br/>
<blockquote>
[!Note]<br />
Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </dl></td>
<td style="text-align: left;">Se trata de una interfaz <strong>de escucha automática</strong> . El tiempo de ejecución comienza a escuchar las llamadas en cuanto se registra la primera interfaz autoliston y se detiene la escucha cuando se anula el registro de la última interfaz autoliston.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <dt><strong>RPC_IF_OLE</strong></dt> </dl></td>
<td style="text-align: left;">Reservado para OLE. No use esta marca.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </dl></td>
<td style="text-align: left;">No implementado actualmente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </dl></td>
<td style="text-align: left;">Limita las conexiones a los clientes que usan un nivel de autorización superior a RPC_C_AUTHN_LEVEL_NONE. Si se especifica esta marca, los clientes pueden pasar a través de la sesión <strong>nula</strong> . En Windows XP y Windows Server 2003, estos clientes no están permitidos. Los clientes que no superan la prueba de RPC_IF_ALLOW_SECURE_ONLY reciben un error de RPC_S_ACCESS_DENIED. El uso de la marca RPC_IF_ALLOW_SECURE_ONLY no implica ni garantiza un alto nivel de privilegios en la parte del usuario que realiza la llamada. RPC solo comprueba si el usuario tiene credenciales válidas; el usuario que realiza la llamada puede estar usando la cuenta invitado u otras cuentas con pocos privilegios. No asuma privilegios elevados cuando se use RPC_IF_ALLOW_SECURE_ONLY.<br/> <strong>Windows NT 4,0 y Windows Me/98/95:  </strong><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </dl></td>
<td style="text-align: left;">Deshabilita el almacenamiento en caché de devolución de llamada de seguridad, lo que fuerza una devolución de llamada de seguridad para cada llamada RPC en una interfaz determinada.<br/>
<blockquote>
[!Note]<br />
Esta marca está disponible a partir de Windows XP con SP2 y Windows Server 2003 con SP1.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Rpcdce. h</dt> </dl> |



 

 





