---
title: Elección de las opciones de QOS de seguridad
description: Las opciones de QOS de seguridad se pasan como parte del parámetro SecurityQOS dado a la función RpcBindingSetAuthInfoEx. Use los siguientes procedimientos recomendados.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244736"
---
# <a name="choosing-security-qos-options"></a>Elección de las opciones de QOS de seguridad

Las opciones de QOS de seguridad se pasan como parte del parámetro *SecurityQOS* dado a la [**función RpcBindingSetAuthInfoEx.**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) Use los siguientes procedimientos recomendados.

## <a name="use-mutual-authentication"></a>Uso de la autenticación mutua

La autenticación mutua verdadera solo está disponible para determinados proveedores de seguridad: Negotiate (cuando negocia Kerberos), Kerberos y Schannel. NTLM no admite la autenticación mutua. El uso de la autenticación mutua requiere que se proporciona un nombre principal de servidor correcto. Muchos desarrolladores usan la siguiente práctica de seguridad defectuosa: se llama al servidor para pedir su nombre principal [**(RpcMgmtInqServerPrincName)**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)y, a continuación, solicitan de forma inequilada la autenticación mutua con ese nombre principal. Este enfoque interrumpe toda la idea de autenticación mutua; La idea de la autenticación mutua es que solo se llama a determinados servidores porque son de confianza para analizar y controlar los datos. Con la práctica de seguridad defectuosa que se acaba de describir, los desarrolladores dan sus datos a cualquier persona lo suficientemente inteligente como para devolver su nombre.

Por ejemplo, si el software cliente debe llamar solo a un servidor que se ejecuta en las cuentas de Joe, Quer o Alice, se debe llamar a la función [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) y se debe comprobar el nombre que se devuelve. Si es Joe, Kerberos o Alice, se debe solicitar la autenticación mutua con su nombre principal de servidor. Esto garantiza que ambas mitades de la conversación vayan a la misma entidad de seguridad.

Si el software cliente debe llamar a un servicio que se ejecuta solo con la cuenta de Joe, cree directamente el nombre principal del servidor de Joe y realice la llamada. Si el servidor no es Joe, la llamada simplemente producirá un error.

Muchas veces, los servicios se ejecutan Windows servicios del sistema, lo que significa que se ejecutan en la cuenta de equipo. Todavía se recomienda la autenticación mutua y la creación de un nombre principal de servidor.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Usar el tipo de suplantación más bajo que permite que la llamada pase por

Este procedimiento recomendado es bastante explicativo. Aunque se utilice la autenticación mutua, no dé al servidor más derechos de los necesarios; es posible que un servidor legítimo se haya puesto en peligro y, aunque los datos que envíe se encontrarán en manos equivocadas en estos casos, al menos el servidor no podrá acceder a otros datos de la red en su nombre. Algunos servidores rechazarán una llamada que no tenga suficiente información para determinar y posiblemente suplantar al autor de la llamada. Además, tenga en cuenta que algunas secuencias de protocolo admiten la seguridad de nivel de transporte [**(ncacn \_ np**](/windows/desktop/Midl/ncacn-np) y [**ncalrpc).**](/windows/desktop/Midl/ncalrpc) En tales casos, el servidor siempre puede suplantar si especifica un nivel de suplantación lo suficientemente alto a través del parámetro *NetworkOptions* al crear el identificador de enlace.

Por último, algunos proveedores de seguridad o transportes pueden subir impersonationType de forma transparente a un nivel superior al especificado. Al desarrollar un programa, asegúrese de intentar realizar llamadas con el impersonationType previsto y compruebe si está obteniendo un valor superior de ImpersonationType en el servidor.

 

 