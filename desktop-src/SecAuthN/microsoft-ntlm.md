---
description: Desafío/respuesta de Windows (NTLM) es el protocolo de autenticación usado en redes que incluyen sistemas que ejecutan el sistema operativo Windows y en sistemas independientes.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541174"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Desafío/respuesta de Windows (NTLM) es el protocolo de autenticación usado en redes que incluyen sistemas que ejecutan el sistema operativo Windows y en sistemas independientes.

El [*paquete de seguridad*](../secgloss/s-gly.md) de Microsoft [*Kerberos*](../secgloss/k-gly.md) agrega mayor seguridad que NTLM a los sistemas de una red. Aunque Microsoft *Kerberos* es el protocolo preferido, sigue siendo compatible con NTLM. NTLM debe usarse también para la autenticación de inicio de sesión en sistemas independientes. Para obtener más información acerca de Kerberos, consulte [Microsoft Kerberos](microsoft-kerberos.md).

Las credenciales de NTLM se basan en los datos obtenidos durante el proceso de inicio de sesión interactivo y constan de un nombre de dominio, un nombre de usuario y un [*hash*](../secgloss/h-gly.md) unidireccional de la contraseña del usuario. NTLM utiliza un protocolo de desafío/respuesta cifrado para autenticar a un usuario sin enviar la contraseña del usuario a través de la conexión. En su lugar, el sistema que solicita la autenticación debe realizar un cálculo que demuestre que tiene acceso a las credenciales NTLM protegidas.

La autenticación NTLM interactiva a través de una red normalmente implica dos sistemas: un sistema cliente, donde el usuario solicita la autenticación y un controlador de dominio, donde se mantiene la información relacionada con la contraseña del usuario. Autenticación no interactiva, que puede ser necesaria para permitir que un usuario que ya ha iniciado sesión tenga acceso a un recurso, como una aplicación de servidor, normalmente implica tres sistemas: un cliente, un servidor y un controlador de dominio que realiza los cálculos de autenticación en nombre del servidor.

Los pasos siguientes presentan un esquema de autenticación no interactiva NTLM. En el primer paso se proporcionan las credenciales NTLM del usuario y solo se produce como parte del proceso de autenticación interactiva (inicio de sesión).

1.  (Solo autenticación interactiva) Un usuario obtiene acceso a un equipo cliente y proporciona un nombre de dominio, un nombre de usuario y una contraseña. El cliente calcula un [*hash*](../secgloss/h-gly.md) criptográfico de la contraseña y descarta la contraseña real.
2.  El cliente envía el nombre de usuario al servidor (en [*texto sin formato*](../secgloss/p-gly.md)).
3.  El servidor genera un número aleatorio de 16 bytes, denominado *desafío* o valor de seguridad ( [*nonce*](../secgloss/n-gly.md)), y lo envía al cliente.
4.  El cliente cifra este desafío con el hash de la contraseña del usuario y devuelve el resultado al servidor. Esto se denomina *respuesta*.
5.  El servidor envía los tres elementos siguientes al controlador de dominio:

    -   Nombre de usuario
    -   Desafío enviado al cliente
    -   Respuesta recibida del cliente

6.  El controlador de dominio utiliza el nombre de usuario para recuperar el hash de la contraseña del usuario de la base de datos del administrador de cuentas de seguridad. Usa este hash de contraseña para cifrar el desafío.
7.  El controlador de dominio compara el desafío cifrado calculado (en el paso 6) con la respuesta calculada por el cliente (en el paso 4). Si son idénticos, la autenticación se realiza correctamente.

La aplicación no debe tener acceso al [*paquete de seguridad*](../secgloss/s-gly.md) de NTLM directamente; en su lugar, debe usar el paquete de seguridad [*Negotiate*](../secgloss/n-gly.md) . Negotiate permite que la aplicación aproveche los [*protocolos de seguridad*](../secgloss/s-gly.md) más avanzados si son compatibles con los sistemas implicados en la autenticación. Actualmente, el paquete de seguridad Negotiate selecciona entre [*Kerberos*](../secgloss/k-gly.md) y NTLM. Negotiate selecciona Kerberos a menos que uno de los sistemas implicados en la autenticación no pueda utilizarlo.

 

 
