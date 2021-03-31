---
title: Compatibilidad con el host de seguridad RAS
description: Windows NT 4,0 proporciona una manera de que un archivo DLL de seguridad RAS de terceros mejore las características de seguridad integradas de RAS. Windows 95 no proporciona esta compatibilidad.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Compatibilidad con hosts, RAS
- Compatibilidad del host de seguridad, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777275"
---
# <a name="ras-security-host-support"></a>Compatibilidad con el host de seguridad RAS

Windows NT 4,0 proporciona una manera de que un archivo DLL de seguridad RAS de terceros mejore las características de seguridad integradas de RAS. Windows 95 no proporciona esta compatibilidad.

Un servidor RAS de Windows NT/Windows 2000 proporciona mecanismos de seguridad para validar el acceso a la red de los usuarios remotos. Cuando un servidor RAS recibe una llamada, valida las credenciales del usuario con la base de datos de la cuenta local o de dominio. RAS también admite la seguridad de devolución de llamada, en la que el servidor RAS se cuelga y, a continuación, vuelve a llamar al usuario remoto para establecer la conexión. En el caso de las redes en las que este nivel de seguridad no es suficiente, puede instalar un archivo DLL de seguridad RAS de terceros. A continuación, el archivo DLL de seguridad puede autenticar a un usuario remoto leyendo información de seguridad de una base de datos que no sea la base de datos de cuentas de usuario estándar.

Cuando el servidor RAS recibe una llamada, invoca el archivo DLL de seguridad para autenticar al usuario remoto. La compatibilidad con el host de seguridad RAS proporciona un mecanismo para que la DLL de seguridad se comunique con el usuario remoto a través de una ventana de terminal en el equipo remoto. En un escenario típico, el archivo DLL de seguridad solicita el nombre de inicio de sesión del usuario remoto. A continuación, el archivo DLL utiliza su base de datos de seguridad privada para formular un desafío para enviar al terminal remoto. Por ejemplo, el desafío podría ser un código que el usuario debe proporcionar como entrada para un lector Cardkey. A continuación, el lector Cardkey muestra una respuesta que el usuario remoto escribe en la ventana de terminal. A continuación, la DLL de seguridad valida la respuesta con la información del usuario en la base de datos de seguridad privada.

Si el archivo DLL de seguridad autentica al usuario remoto, el servidor RAS realiza su propia autenticación. Esto garantiza que la seguridad de RAS siempre autentique a un usuario remoto, incluso si hay instalado un archivo DLL de seguridad que conceda acceso a todos los usuarios.

> [!Note]  
> Windows NT/Windows 2000 actualmente proporciona compatibilidad de host de seguridad de RAS solo para conexiones de módem asincrónicas; no se admiten otros tipos de conexiones, como Ethernet (que no es una conexión de módem), VPN (que tampoco es una conexión de módem) o ISDN (que es sincrónico).

 

 

 




