---
description: Intercambio de cliente/servidor
ms.assetid: 2449c4b3-720d-4b84-b3cf-fcc4abd05d33
title: Intercambio de cliente/servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6274705ef6719c846f0551f90fca8790ba89f2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155905"
---
# <a name="clientserver-exchange"></a>Intercambio de cliente/servidor

Una vez que un usuario tiene un vale para un servidor, el cliente de estación de trabajo puede establecer una sesión de comunicaciones segura con ese servidor.

**Para establecer una sesión de comunicaciones segura con un servidor**

1.  El cliente envía al servidor un mensaje de tipo KRB \_ AP \_ req (solicitud de aplicación de Kerberos). Este mensaje contiene un mensaje de autenticador cifrado con la clave enviada por el [*centro de distribución de claves*](/windows/desktop/SecGloss/k-gly) (KDC) para la sesión con el servidor, el vale para las sesiones con el servidor y una marca que indica si el cliente solicita la autenticación mutua. La configuración de la marca que solicita la autenticación mutua es una de las opciones de configuración de [*Kerberos*](/windows/desktop/SecGloss/k-gly). Nunca se pregunta al usuario si se debe usar la autenticación mutua.
2.  El servidor recibe KRB \_ AP \_ req, descifra el vale y extrae los datos de autorización del usuario y la [*clave de sesión*](/windows/desktop/SecGloss/s-gly).
3.  El servidor utiliza la clave de sesión del vale para descifrar el mensaje del autenticador del usuario y evalúa la marca de tiempo dentro de.
4.  Si el mensaje del autenticador es válido, el servidor comprueba la marca de autenticación mutua en la solicitud del cliente.
5.  Si se establece la marca de autenticación mutua, el servidor utiliza la clave de sesión para cifrar el tiempo desde el mensaje del autenticador del usuario y devuelve el resultado en un mensaje de tipo KRB \_ AP \_ REP (respuesta de la aplicación Kerberos).
6.  Cuando el cliente recibe KRB \_ AP \_ REP, descifra el mensaje del autenticador del servidor con la clave de sesión que comparte con el servidor y compara la hora que devuelve el servicio con la hora del mensaje del autenticador original. Si coinciden, el cliente está seguro de que el servicio es original y que la conexión continúa.

 

 
