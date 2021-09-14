---
description: En lugar de enviar las claves de sesión cifradas a ambas entidades de seguridad, el KDC envía las copias del cliente y del servidor de la clave de sesión al cliente.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Vales de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762223311dd71f8bded5e021372d3a281f711eda
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244119"
---
# <a name="session-tickets"></a>Vales de sesión

En lugar de enviar las claves de sesión cifradas a ambas entidades de seguridad, el [](../secgloss/s-gly.md) [KDC](key-distribution-center.md) envía las copias del cliente y del servidor de la clave de sesión al cliente. La copia del cliente de la clave de [](../secgloss/m-gly.md) sesión se cifra con la clave maestra del cliente y, por tanto, ninguna otra entidad puede descifrarla. La copia del servidor de la clave de sesión se inserta, junto con los datos de autorización sobre el cliente, en una estructura de datos denominada vale. El vale se cifra completamente con la clave maestra del servidor y, por tanto, el cliente o cualquier otra entidad que no tenga acceso a la clave maestra del servidor no pueden leer ni cambiar. Es responsabilidad del cliente almacenar el vale de forma segura hasta que se póngase en contacto con el servidor.

> [!Note]  
> El KDC solo proporciona un servicio de concesión de vales. El cliente y el servidor son responsables de proteger sus respectivas claves maestras.

 

Cuando el cliente recibe la respuesta del KDC, extrae el vale y su propia copia de la clave de sesión, dejando ambos a un lado en una caché segura. Para establecer una sesión segura con el servidor, envía al servidor un mensaje que consta del [](authenticator-messages.md) vale, aún cifrado con la clave maestra del servidor y un mensaje autenticador cifrado con la clave de sesión. Juntos, el vale y el mensaje del autenticador son las credenciales del [*cliente*](../secgloss/c-gly.md) para el servidor.

Cuando el servidor recibe credenciales de un cliente, descifra [](../secgloss/s-gly.md)el vale con su clave [*maestra,*](../secgloss/m-gly.md)extrae la clave de sesión y usa la clave de sesión para descifrar el mensaje autenticador del cliente. Si todo se comprueba, el servidor sabe que las credenciales del cliente las emitió el KDC, una autoridad de confianza. Para la autenticación mutua, el servidor responde mediante el cifrado de la marca de tiempo del mensaje autenticador del cliente mediante la clave de sesión. Este mensaje cifrado se envía al cliente. A continuación, el cliente descifra el mensaje. Si el mensaje devuelto es el mismo que la marca de tiempo del mensaje autenticador original, el servidor se autentica.

Como ventaja adicional, el servidor no necesita almacenar las claves de sesión que usa con sus clientes. Es responsabilidad de cada cliente administrar el vale para el servidor en su caché de vales y presentar ese vale cada vez que accede al servidor. Cada vez que el servidor recibe un vale de un cliente, usa su clave maestra para descifrar el vale y extraer la clave de sesión. Cuando el servidor ya no necesita la clave de sesión, se elimina la clave.

El cliente no necesita acceder al KDC cada vez que desea acceder a este servidor en particular. Los vales se pueden reutilizar. Como medida de precaución frente a la posibilidad de robo de vales, los vales tienen una hora de expiración, especificada por el KDC en la estructura de vales. El tiempo que un vale es válido depende de la directiva de Kerberos para el dominio kerberos. Normalmente, los vales son buenos durante no más de ocho horas, aproximadamente la duración de una sesión de [*inicio de sesión normal.*](../secgloss/l-gly.md) Cuando el usuario de una estación de trabajo cliente cierra la sesión, se vacía la caché de vales de cliente y se destruyen todos los vales y las claves de sesión de cliente.

 

 
