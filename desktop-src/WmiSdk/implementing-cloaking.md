---
description: La suplantación es una extensión para la suplantación que permite un mejor control sobre cómo COM suplanta a un cliente a través de un proxy. Al igual que muchas formas de seguridad WMI, establece la protección a través de las interfaces CoSetProxyBlanket y CoInitializeSecurity.
ms.assetid: e094aecc-e940-43aa-87c2-ea8cc86d1051
ms.tgt_platform: multiple
title: Implementar el contrabando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d32333250bc37d8ccbfdb17421fed635f0da77e6394229220b2b36a1ce57f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318900"
---
# <a name="implementing-cloaking"></a>Implementar el contrabando

La suplantación es una extensión para la suplantación que permite un mejor control sobre cómo COM suplanta a un cliente a través de un proxy. Al igual que muchas formas de seguridad WMI, establece la protección a través de las interfaces [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) y [**CoInitializeSecurity.**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity)

COM proporciona las siguientes formas de protección:

-   estática

    COM establece la identidad del token por el subproceso o el token de proceso en la primera llamada al proxy. Si usa el arroba estático [**con CoSetProxyBlanket,**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)establece la identidad del proxy durante la vida útil del proxy.

-   Dinámica

    COM restablece la identidad del token del subproceso o del token de proceso en cada llamada al proxy. Dado que COM comprueba la identidad en cada llamada, la dinámica permite un control más preciso sobre la identidad del cliente. Sin embargo, la dinámica es menos eficaz que la estática.

Al establecer la protección junto con el nivel de delegación de suplantación, un servidor puede propagar la identidad de un cliente entre servidores, incluso si los servidores son remotos. Si no habilita la protección, COM realiza cualquier llamada desde un servidor local a un servidor remoto en el contexto del proceso de servidor real.

La suplantación permite a WMI suplantar a un cliente para acceder a los recursos de red locales y remotos a través de varios límites de equipo. WMI puede pasar la identidad del cliente a servidores locales y remotos, como otras instancias remotas de WMI. Después, esos servidores remotos pueden realizar operaciones en el contexto de cliente inicial.

En el procedimiento siguiente se describe cómo usar conjuntamente la delegación y la delegación.

**Para usar conjuntamente la delegación y la colaboración**

1.  Establezca el servicio de autenticación en Kerberos.

    Kerberos es el único servicio de autenticación que admite la delegación y la delegación remotas. Esto significa que la delegación y la delegación solo se pueden usar en servidores remotos.

2.  Marque la cuenta de inicio de sesión del servidor como "Trusted for Delegation" (Confianza para la delegación) en Active Directory servicios.
3.  Marque la cuenta de inicio de sesión de cliente como "La cuenta es confidencial y no se puede delegar" en Active Directory servicios.

Por ejemplo, una llamada al proveedor de vistas, que puede devolver objetos de varias instancias de WMI en varios equipos, puede beneficiarse de la delegación y el movimiento.

 

 
