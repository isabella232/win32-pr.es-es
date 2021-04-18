---
title: Protocolo Kerberos V5
description: Protocolo Kerberos V5
ms.assetid: a53a1edf-f374-4cbf-8050-7cde45284157
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d78c4bdc457007c04ad66163e2ebfd7f5397f9
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105714341"
---
# <a name="kerberos-v5-protocol"></a>Protocolo Kerberos V5

El protocolo de autenticación Kerberos V5 tiene un identificador de servicio de autenticación de RPC \_ C \_ authn \_ GSS \_ Kerberos. El protocolo Kerberos define el modo en que los clientes interactúan con un servicio de autenticación de red y fueron estandarizados por Internet Engineering Task Force (IETF) en septiembre de 1993, en el documento [RFC 1510](https://www.ietf.org/rfc/rfc1510.txt). Los clientes obtienen vales del Centro de distribución de claves Kerberos (KDC) y presentan estos vales a los servidores cuando se establecen las conexiones. Los vales de Kerberos representan las credenciales de red del cliente.

Al igual que NTLM, el protocolo Kerberos utiliza el nombre de dominio, el nombre de usuario y la contraseña para representar la identidad del cliente. El vale de Kerberos inicial obtenido del KDC cuando el usuario inicia sesión se basa en un hash cifrado de la contraseña del usuario. Este vale inicial se almacena en caché. Cuando el usuario intenta conectarse a un servidor, el protocolo Kerberos comprueba la caché de vales en busca de un vale válido para ese servidor. Si no hay ninguno disponible, el vale inicial del usuario se envía al KDC junto con una solicitud de vale para el servidor especificado. Ese vale de sesión se agrega a la memoria caché y se puede usar para conectarse al mismo servidor hasta que expire el vale.

Cuando un servidor llama a [**CoQueryClientBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryclientblanket) con el protocolo Kerberos, se devuelven el nombre de dominio y el nombre de usuario del cliente. Cuando un servidor llama a [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), se devuelve el token del cliente. Estos comportamientos son los mismos que cuando se usa NTLM.

El protocolo Kerberos funciona a través de los límites del equipo. Los equipos cliente y servidor deben estar en dominios y esos dominios deben tener una relación de confianza.

El protocolo Kerberos requiere autenticación mutua y la admite de forma remota. El cliente debe especificar el nombre principal del servidor y la identidad del servidor debe coincidir exactamente con el nombre de la entidad de seguridad. Si el cliente especifica **null** para el nombre principal del servidor o si el nombre de la entidad de seguridad no coincide con el servidor, se producirá un error en la llamada.

Con el protocolo Kerberos, se pueden usar los niveles de suplantación de identidad, suplantar y delegado. Cuando un servidor llama a [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient), el token devuelto es válido fuera del equipo durante un período de tiempo entre 5 minutos y 8 horas. Después de este tiempo, solo se puede usar en el equipo servidor. Si un servidor se "ejecuta como Activator" y la activación se realiza con el protocolo Kerberos, el token del servidor expirará entre 5 minutos y 8 horas después de la activación.

El protocolo de autenticación de Kerberos V5 implementado por Windows admite la [ocultación](cloaking.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[COM y paquetes de seguridad](com-and-security-packages.md)
</dt> </dl>

 

 




