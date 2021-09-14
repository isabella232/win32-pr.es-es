---
title: Compatibilidad con host de seguridad ras
description: Windows NT 4.0 proporciona una manera de que un archivo DLL de seguridad RAS de terceros mejore las características de seguridad integradas de RAS. Windows 95 no proporciona esta compatibilidad.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Compatibilidad con host, RAS
- Compatibilidad con host de seguridad, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073865"
---
# <a name="ras-security-host-support"></a>Compatibilidad con host de seguridad ras

Windows NT 4.0 proporciona una manera de que un archivo DLL de seguridad RAS de terceros mejore las características de seguridad integradas de RAS. Windows 95 no proporciona esta compatibilidad.

Un Windows NT/Windows 2000 RAS proporciona mecanismos de seguridad para validar el acceso a la red de los usuarios remotos. Cuando un servidor RAS recibe una llamada, valida las credenciales del usuario en la base de datos de la cuenta local o de dominio. RAS también admite la seguridad de de vuelta de llamadas, en la que el servidor RAS se mantiene y, a continuación, vuelve a llamar al usuario remoto para establecer la conexión. Para las redes en las que este nivel de seguridad no es suficiente, puede instalar un archivo DLL de seguridad RAS de terceros. A continuación, el archivo DLL de seguridad puede autenticar a un usuario remoto mediante la lectura de información de seguridad de una base de datos que no sea la base de datos de la cuenta de usuario estándar.

Cuando el servidor RAS recibe una llamada, invoca el archivo DLL de seguridad para autenticar al usuario remoto. La compatibilidad con el host de seguridad ras proporciona un mecanismo para que el archivo DLL de seguridad se comunique con el usuario remoto a través de una ventana de terminal en el equipo remoto. En un escenario típico, el archivo DLL de seguridad solicita el nombre de inicio de sesión del usuario remoto. A continuación, el archivo DLL usa su base de datos de seguridad privada para formular un desafío para enviar al terminal remoto. Por ejemplo, el desafío podría ser un código que el usuario debe proporcionar como entrada a un lector cardkey. A continuación, el lector de clave de tarjeta muestra una respuesta que el usuario remoto tipos en la ventana del terminal. A continuación, el archivo DLL de seguridad valida la respuesta con la información del usuario en la base de datos de seguridad privada.

Si la DLL de seguridad autentica al usuario remoto, el servidor RAS realiza su propia autenticación. Esto garantiza que la seguridad de RAS siempre autentica a un usuario remoto, incluso si se instala un archivo DLL de seguridad que concede acceso a todos los usuarios.

> [!Note]  
> Windows NT/Windows 2000 actualmente proporciona compatibilidad con host de seguridad RAS solo para conexiones de módem asincrónicas; No se admiten otros tipos de conexiones, como Ethernet (que no es una conexión de módem), VPN (que tampoco es una conexión de módem) o ISDN (que es sincrónico).

 

 

 




