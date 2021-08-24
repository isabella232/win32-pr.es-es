---
description: Cliente o servidor Exchange
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Cliente o servidor Exchange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2401d3cf2bb59586e608bc7566c13009869d2874a1532b659f70c6c4e09e4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141178"
---
# <a name="clientserver-exchange"></a>Cliente o servidor Exchange

Una vez que un usuario tiene un vale para un servidor, el cliente de estación de trabajo puede establecer una sesión de comunicaciones seguras con ese servidor.

**Para establecer una sesión de comunicaciones seguras con un servidor**

1.  El cliente envía al servidor un mensaje de tipo KRB \_ AP \_ REQ (solicitud de aplicación Kerberos). Este mensaje contiene un mensaje autenticador cifrado con la clave enviada por el [*Centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) para la sesión con el servidor, el vale para las sesiones con el servidor y una marca que indica si el cliente solicita autenticación mutua. Establecer la marca que solicita la autenticación mutua es una de las opciones de configuración de [*Kerberos.*](/windows/desktop/SecGloss/k-gly) Nunca se pregunta al usuario si se debe usar la autenticación mutua.
2.  El servidor recibe KRB \_ AP \_ REQ, descifra el vale y extrae los datos de autorización del usuario y la [*clave de sesión*](/windows/desktop/SecGloss/s-gly).
3.  El servidor usa la clave de sesión del vale para descifrar el mensaje de autenticación del usuario y evalúa la marca de tiempo dentro.
4.  Si el mensaje de autenticación es válido, el servidor comprueba la marca de autenticación mutua en la solicitud del cliente.
5.  Si se establece la marca de autenticación mutua, el servidor usa la clave de sesión para cifrar la hora del mensaje autenticador del usuario y devuelve el resultado en un mensaje de tipo KRB AP REP (respuesta de aplicación \_ \_ Kerberos).
6.  Cuando el cliente recibe KRB \_ AP REP, descifra el mensaje autenticador del servidor con la clave de sesión que comparte con el servidor y compara la hora enviada por el servicio con la hora del mensaje de autenticación \_ original. Si coinciden, el cliente está seguro de que el servicio es original y la conexión continúa.

 

 
