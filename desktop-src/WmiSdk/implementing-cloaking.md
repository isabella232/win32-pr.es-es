---
description: La ocultación es una extensión a la suplantación que permite un mejor control sobre cómo COM suplanta a un cliente a través de un proxy. Al igual que muchas formas de seguridad de WMI, se establece la ocultación a través de las interfaces CoSetProxyBlanket y CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementar Cloaking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac73d7aacf32a2168dc3651b82ae1ce3a977cf5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277931"
---
# <a name="implementing-cloaking"></a>Implementar Cloaking

La ocultación es una extensión a la suplantación que permite un mejor control sobre cómo COM suplanta a un cliente a través de un proxy. Al igual que muchas formas de seguridad de WMI, se establece la ocultación a través de las interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) y [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) .

COM proporciona las siguientes formas de Cloaking:

-   estática

    COM establece la identidad del token por el subproceso o el token de proceso en la primera llamada al proxy. Si utiliza el Cloaking estático con [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket), establezca la identidad del proxy para la vida del proxy.

-   Dinámica

    COM restablece la identidad del token del subproceso o token del proceso en cada llamada al proxy. Dado que COM comprueba la identidad en cada llamada, el Cloaking dinámico permite un mayor control sobre la identidad del cliente. Sin embargo, el Cloaking dinámico es menos eficaz que el Cloaking estático.

Cuando se establece la ocultación junto con el nivel de delegación de la suplantación, un servidor puede propagar la identidad de un cliente entre servidores, incluso si los servidores son remotos. Si no habilita la ocultación, COM realiza cualquier llamada desde un servidor local a un servidor remoto en el contexto del proceso de servidor real.

La ocultación permite a WMI suplantar a un cliente para obtener acceso a recursos de red locales y remotos en varios límites de equipos. WMI puede pasar la identidad del cliente a servidores locales y remotos, como otras instancias remotas de WMI. Estos servidores remotos pueden realizar operaciones en el contexto de cliente inicial.

En el procedimiento siguiente se describe cómo usar juntos la ocultación y la delegación.

**Para usar la ocultación y la delegación juntas**

1.  Establezca el servicio de autenticación en Kerberos.

    Kerberos es el único servicio de autenticación que admite el Cloaking y la delegación remotos. Esto significa que la ocultación y la delegación solo se pueden usar en servidores remotos.

2.  Marque la cuenta de inicio de sesión del servidor como "de confianza para delegación" en el Active Directory Services.
3.  Marque la cuenta de inicio de sesión de cliente como "la cuenta es importante y no se puede delegar" en Active Directory Services.

Por ejemplo, una llamada al proveedor de vistas, que puede devolver objetos de varias instancias de WMI en varios equipos, puede beneficiarse de la delegación y la ocultación.

 

 
