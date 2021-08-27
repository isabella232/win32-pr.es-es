---
title: Protocolo Kerberos v5
description: Protocolo Kerberos v5
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a1b739aac67a7a30918e78fa3bb364506ade7dfd720c390db1cc37909f2fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992465"
---
# <a name="kerberos-v5-protocol"></a>Protocolo Kerberos v5

El protocolo de autenticación Kerberos v5 tiene un identificador de servicio de autenticación de RPC \_ C \_ \_ AUTHN GSS \_ KERBEROS. El protocolo Kerberos define cómo interactúan los clientes con un servicio de autenticación de red y fue estandarizado por el Grupo de tareas de ingeniería de Internet (IETF) en septiembre de 1993, en el documento [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt). Los clientes obtienen vales del Centro de distribución de claves Kerberos (KDC) y presentan estos vales a los servidores cuando se establecen las conexiones. Los vales de Kerberos representan las credenciales de red del cliente.

Al igual que NTLM, el protocolo Kerberos usa el nombre de dominio, el nombre de usuario y la contraseña para representar la identidad del cliente. El vale kerberos inicial obtenido del KDC cuando el usuario inicia sesión se basa en un hash cifrado de la contraseña del usuario. Este vale inicial se almacena en caché. Cuando el usuario intenta conectarse a un servidor, el protocolo Kerberos comprueba la caché de vales para un vale válido para ese servidor. Si no hay uno disponible, el vale inicial del usuario se envía al KDC junto con una solicitud de un vale para el servidor especificado. Ese vale de sesión se agrega a la memoria caché y se puede usar para conectarse al mismo servidor hasta que expire el vale.

Cuando un servidor llama a [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) mediante el protocolo Kerberos, se devuelven el nombre de dominio y el nombre de usuario del cliente. Cuando un servidor llama [**a CoImpersonateClient,**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)se devuelve el token del cliente. Estos comportamientos son los mismos que cuando se usa NTLM.

El protocolo Kerberos funciona a través de los límites del equipo. Los equipos cliente y servidor deben estar en dominios y esos dominios deben tener una relación de confianza.

El protocolo Kerberos requiere autenticación mutua y lo admite de forma remota. El cliente debe especificar el nombre principal del servidor y la identidad del servidor debe coincidir exactamente con ese nombre principal. Si el cliente especifica **NULL para** el nombre principal del servidor o si el nombre principal no coincide con el servidor, se producirá un error en la llamada.

Con el protocolo Kerberos, se pueden usar los niveles de suplantación para identificar, suplantar y delegar. Cuando un servidor llama a [**CoImpersonateClient,**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)el token devuelto es válido fuera del equipo durante un período de tiempo entre 5 minutos y 8 horas. Después de este tiempo, solo se puede usar en el equipo servidor. Si un servidor se "ejecuta como activador" y la activación se realiza con el protocolo Kerberos, el token del servidor expirará entre 5 minutos y 8 horas después de la activación.

El protocolo de autenticación Kerberos v5 implementado por Windows admite [la creación de](cloaking.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 




