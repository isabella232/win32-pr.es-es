---
description: Para ayudar a evitar ataques malintencionados, determine si la aplicación requiere privilegios de administrador. En el caso de las funciones que requieren permisos de administrador, cree una aplicación independiente y use el comando de línea de comandos runas de Windows.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Ejecutar con privilegios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc28843195e9b5cabadc13aa2317b0bdd8058ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669741"
---
# <a name="running-with-administrator-privileges"></a>Ejecutar con privilegios de administrador

El primer paso para establecer el tipo de cuenta con la que se debe ejecutar la aplicación es examinar qué recursos usará la aplicación y qué API con privilegios llamará. Es posible que la aplicación, o partes grandes, no requieran privilegios de administrador. La *escritura de código seguro*, de Michael Howard y David LeBlanc, ofrece una excelente descripción de cómo llevar a cabo esta evaluación y es muy recomendable. (Es posible que este recurso no esté disponible en algunos idiomas y países).

Puede proporcionar los privilegios que la aplicación necesita con menos exposición a ataques malintencionados mediante uno de los métodos siguientes:

-   Ejecutarse en una cuenta con menos privilegios. Una manera de hacerlo es usar [**PrivilegeCheck**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) para determinar qué privilegios están habilitados en un token. Si los privilegios disponibles no son adecuados para la operación actual, puede deshabilitar ese código y pedir al usuario que inicie sesión en una cuenta con privilegios de administrador.
-   Divida en una función de aplicación independiente que requiera permisos de administrador. Puede proporcionar al usuario un acceso directo que ejecute el comando runas. Para obtener instrucciones detalladas sobre cómo configurar el acceso directo, busque "runas" en la ayuda de. Mediante programación, puede configurar el comando [runas](/windows/desktop/com/runas) en la clave del registro de [clave AppID](/windows/desktop/com/appid-key) de la aplicación.
-   Autentique al usuario mediante una llamada a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) o [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (línea de comandos) para obtener el nombre de usuario y la contraseña. Para obtener un ejemplo, consulte [solicitar credenciales al usuario](asking-the-user-for-credentials.md).
-   Suplantar al usuario. Un proceso que se inicia en una cuenta con privilegios elevados, como sistema, puede suplantar una cuenta de usuario mediante una llamada a [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) o funciones de suplantación similares, lo que reduce el nivel de privilegios. Sin embargo, si se inserta una llamada a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) en el subproceso, el proceso vuelve a los privilegios del sistema originales.

Si ha determinado que la aplicación debe ejecutarse en una cuenta con privilegios de administrador y que se debe almacenar una contraseña de administrador en el sistema de software, consulte [Administración de contraseñas](handling-passwords.md) para los métodos de hacerlo de forma segura.

 

 
