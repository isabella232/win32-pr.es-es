---
title: Elegir opciones de QOS de seguridad
description: Las opciones de QOS de seguridad se pasan como parte del parámetro SecurityQOS dado a la función RpcBindingSetAuthInfoEx. Utilice las siguientes prácticas recomendadas.
ms.assetid: 43befe3d-079a-4389-a1ff-6bda90935769
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c286b516438eae78117ef8d73939c3b4bed396d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676485"
---
# <a name="choosing-security-qos-options"></a>Elegir opciones de QOS de seguridad

Las opciones de QOS de seguridad se pasan como parte del parámetro *SecurityQOS* dado a la función [**RpcBindingSetAuthInfoEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa) . Utilice las siguientes prácticas recomendadas.

## <a name="use-mutual-authentication"></a>Usar autenticación mutua

La autenticación mutua verdadera solo está disponible para determinados proveedores de seguridad: Negotiate (cuando negocia Kerberos), Kerberos y Schannel. NTLM no admite la autenticación mutua. El uso de la autenticación mutua requiere que se proporcione un nombre de entidad de seguridad de servidor correcto. Muchos desarrolladores usan la siguiente práctica de seguridad defectuosa: se llama al servidor para solicitar su nombre principal ([**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)) y, a continuación, se les solicita la autenticación mutua mediante ese nombre de entidad de seguridad. Este enfoque interrumpe toda la idea de la autenticación mutua; la idea de la autenticación mutua es que solo se llama a determinados servidores porque son de confianza para analizar y controlar los datos. Mediante el uso de la práctica de seguridad defectuosa que se acaba de describir, los desarrolladores proporcionan sus datos a cualquier persona lo suficientemente inteligente como para devolver su nombre.

Por ejemplo, si el software cliente debe llamar solo a un servidor que ejecute en las cuentas Joe, Ana o Alice, se debe llamar a la función [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname) y debe comprobarse el nombre que se devuelve. Si es Joe, Pedro o Alice, se debe solicitar la autenticación mutua con el nombre de la entidad de seguridad del servidor. Esto garantiza que las dos mitades de la conversación vayan a la misma entidad de seguridad.

Si el software cliente debe llamar solo a un servicio que se ejecuta en la cuenta de Joe, cree directamente el nombre de entidad de seguridad de servidor de Joe y realice la llamada. Si el servidor no es Joe, simplemente se producirá un error en la llamada.

Muchas veces, los servicios se ejecutan como servicios del sistema de Windows, lo que significa que se ejecutan en la cuenta de la máquina. Todavía se recomienda la autenticación mutua y la creación de un nombre de entidad de seguridad de servidor.

## <a name="use-the-lowest-impersonationtype-that-allows-the-call-to-go-through"></a>Use el ImpersonationType más bajo que permite a la llamada pasar por

Este procedimiento recomendado es bastante descriptivo. Incluso si se usa la autenticación mutua, no proporcione al servidor más derechos de lo necesario. es posible que se haya puesto en peligro un servidor legítimo y, aunque los datos que envía se encuentren en las manos equivocadas, como mínimo, el servidor no podrá tener acceso a otros datos de la red en su nombre. Algunos servidores rechazarán una llamada que no tiene información suficiente para determinar y, posiblemente, suplantar al llamador. Además, tenga en cuenta que algunas secuencias de protocolos admiten la seguridad de nivel de transporte ([**ncacn \_ NP**](/windows/desktop/Midl/ncacn-np) y [**ncalrpc**](/windows/desktop/Midl/ncalrpc)). En tales casos, el servidor siempre puede suplantar al usuario si se especifica un nivel de suplantación lo suficientemente alto mediante el parámetro *NetworkOptions* al crear el identificador de enlace.

Por último, algunos proveedores de seguridad o transportes pueden golpear de forma transparente ImpersonationType a un nivel superior al especificado. Al desarrollar un programa, asegúrese de intentar realizar llamadas con el ImpersonationType previsto y compruebe si está obteniendo más ImpersonationType en el servidor.

 

 