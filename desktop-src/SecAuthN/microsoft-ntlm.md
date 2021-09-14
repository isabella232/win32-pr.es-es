---
description: Windows Desafío/respuesta (NTLM) es el protocolo de autenticación que se usa en redes que incluyen sistemas que ejecutan el sistema operativo Windows y en sistemas independientes.
ms.assetid: 35a38858-d36f-45c9-95f4-2541a182f5ac
title: Microsoft NTLM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9723f24d5913adefe70d4e238de0591790a34bfd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173462"
---
# <a name="microsoft-ntlm"></a>Microsoft NTLM

Windows Desafío/respuesta (NTLM) es el protocolo de autenticación que se usa en redes que incluyen sistemas que ejecutan el sistema operativo Windows y en sistemas independientes.

El paquete de [*seguridad de*](../secgloss/s-gly.md) Microsoft [*Kerberos*](../secgloss/k-gly.md) agrega mayor seguridad que NTLM a los sistemas de una red. Aunque Microsoft *Kerberos* es el protocolo elegido, NTLM todavía se admite. NTLM debe usarse también para la autenticación de inicio de sesión en sistemas independientes. Para obtener más información sobre Kerberos, vea [Microsoft Kerberos](microsoft-kerberos.md).

Las credenciales NTLM se basan en los datos obtenidos durante el proceso de inicio de sesión interactivo y constan de un nombre de dominio, un nombre de usuario y un [*hash*](../secgloss/h-gly.md) un way de la contraseña del usuario. NTLM usa un protocolo cifrado de desafío/respuesta para autenticar a un usuario sin enviar la contraseña del usuario a través de la conexión. En su lugar, el sistema que solicita la autenticación debe realizar un cálculo que demuestre que tiene acceso a las credenciales NTLM protegidas.

La autenticación NTLM interactiva a través de una red suele implicar dos sistemas: un sistema cliente, donde el usuario solicita autenticación y un controlador de dominio, donde se conserva la información relacionada con la contraseña del usuario. La autenticación no inactiva, que puede ser necesaria para permitir que un usuario que ya ha iniciado sesión acceda a un recurso como una aplicación de servidor, normalmente implica tres sistemas: un cliente, un servidor y un controlador de dominio que realiza los cálculos de autenticación en nombre del servidor.

En los pasos siguientes se presenta un esquema de la autenticación NTLM no inactiva. El primer paso proporciona las credenciales NTLM del usuario y solo se produce como parte del proceso de autenticación interactiva (inicio de sesión).

1.  (solo autenticación interactiva) Un usuario accede a un equipo cliente y proporciona un nombre de dominio, un nombre de usuario y una contraseña. El cliente calcula un [*hash*](../secgloss/h-gly.md) criptográfico de la contraseña y descarta la contraseña real.
2.  El cliente envía el nombre de usuario al servidor (en [*texto no cifrado).*](../secgloss/p-gly.md)
3.  El servidor genera un número aleatorio de 16 bytes, denominado desafío o [*nonce,*](../secgloss/n-gly.md)y lo envía al cliente. 
4.  El cliente cifra este desafío con el hash de la contraseña del usuario y devuelve el resultado al servidor. Esto se denomina *respuesta*.
5.  El servidor envía los tres elementos siguientes al controlador de dominio:

    -   Nombre de usuario
    -   Desafío enviado al cliente
    -   Respuesta recibida del cliente

6.  El controlador de dominio usa el nombre de usuario para recuperar el hash de la contraseña del usuario de la base de datos del Administrador de cuentas de seguridad. Usa este hash de contraseña para cifrar el desafío.
7.  El controlador de dominio compara el desafío cifrado que calculó (en el paso 6) con la respuesta calculada por el cliente (en el paso 4). Si son idénticas, la autenticación se realiza correctamente.

La aplicación no debe acceder directamente al paquete de [*seguridad*](../secgloss/s-gly.md) NTLM; en su lugar, debe usar el [*paquete de seguridad Negotiate.*](../secgloss/n-gly.md) Negotiate permite que la aplicación aproveche los protocolos de seguridad más avanzados si son compatibles con los sistemas [*implicados*](../secgloss/s-gly.md) en la autenticación. Actualmente, el paquete de seguridad Negotiate selecciona entre [*Kerberos*](../secgloss/k-gly.md) y NTLM. Negotiate selecciona Kerberos a menos que uno de los sistemas implicados en la autenticación no pueda usarlo.

 

 
