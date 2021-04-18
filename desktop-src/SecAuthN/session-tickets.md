---
description: En lugar de enviar las claves de sesión cifrada a ambas entidades de seguridad, el KDC envía las copias del cliente y del servidor de la clave de sesión al cliente.
ms.assetid: 6b20ab30-2cd9-4f2e-a26b-316980c4bc78
title: Vales de sesión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 762223311dd71f8bded5e021372d3a281f711eda
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667110"
---
# <a name="session-tickets"></a>Vales de sesión

En lugar de enviar las claves de sesión cifrada a ambas entidades de seguridad, el [KDC](key-distribution-center.md) envía las copias del cliente y del servidor de la [*clave de sesión*](../secgloss/s-gly.md) al cliente. La copia del cliente de la clave de sesión se cifra con la [*clave maestra*](../secgloss/m-gly.md) del cliente y, por tanto, no se puede descifrar con ninguna otra entidad. La copia del servidor de la clave de sesión está incrustada, junto con los datos de autorización sobre el cliente, en una estructura de datos denominada vale. El vale se cifra por completo con la clave maestra del servidor y, por lo tanto, el cliente no puede leer ni cambiar, ni tampoco otra entidad que no tenga acceso a la clave maestra del servidor. Es responsabilidad del cliente almacenar el vale de forma segura hasta que se ponga en contacto con el servidor.

> [!Note]  
> El KDC solo proporciona un servicio de concesión de vales. El cliente y el servidor son responsables de mantener seguros sus claves maestras respectivas.

 

Cuando el cliente recibe la respuesta del KDC, extrae el vale y su propia copia de la clave de sesión y coloca ambos en una caché segura. Para establecer una sesión segura con el servidor, envía al servidor un mensaje que consta del vale, todavía cifrado con la clave maestra del servidor y un mensaje de [autenticador](authenticator-messages.md) cifrado con la clave de sesión. Juntos, el vale y el mensaje del autenticador son las [*credenciales*](../secgloss/c-gly.md) del cliente para el servidor.

Cuando el servidor recibe las credenciales de un cliente, descifra el vale con su [*clave maestra*](../secgloss/m-gly.md), extrae la [*clave de sesión*](../secgloss/s-gly.md)y usa la clave de sesión para descifrar el mensaje del autenticador del cliente. Si todo se desprotege, el servidor sabe que las credenciales del cliente fueron emitidas por el KDC, una entidad de confianza. Para la autenticación mutua, el servidor responde mediante el cifrado de la marca de tiempo del mensaje del autenticador del cliente mediante la clave de sesión. Este mensaje cifrado se envía al cliente. A continuación, el cliente descifra el mensaje. Si el mensaje devuelto es el mismo que el de la marca de tiempo en el mensaje del autenticador original, el servidor se autentica.

Como ventaja adicional, el servidor no necesita almacenar las claves de sesión que usa con sus clientes. Es responsabilidad de cada cliente administrar el vale para el servidor en su caché de vales y presentar ese vale cada vez que tenga acceso al servidor. Cada vez que el servidor recibe un vale de un cliente, usa su clave maestra para descifrar el vale y extraer la clave de sesión. Cuando el servidor ya no necesita la clave de sesión, se elimina la clave.

El cliente no necesita tener acceso al KDC cada vez que desea tener acceso a este servidor en particular. Los vales se pueden volver a usar. Como medida de precaución contra la posibilidad de robo de vales, los vales tienen una hora de expiración, especificada por el KDC en la estructura del vale. El período de validez de un vale depende de la Directiva de Kerberos para el dominio Kerberos. Normalmente, los vales son buenos para no tener más de ocho horas, acerca de la duración de una [*sesión de inicio*](../secgloss/l-gly.md)de sesión normal. Cuando el usuario de una estación de trabajo cliente cierra la sesión, se vacía la caché de vales de cliente y se destruyen todos los vales y las claves de sesión de cliente.

 

 
