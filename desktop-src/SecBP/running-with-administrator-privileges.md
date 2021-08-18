---
description: Para ayudar a evitar ataques malintencionados, determine si la aplicación requiere privilegios de administrador. Para las funciones que requieren permisos de administrador, cree una aplicación independiente y use el Windows línea de comandos RunAs.
ms.assetid: afa520fc-c206-49de-8d73-8f6566ec4fb6
title: Ejecución con privilegios de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87533e71fbce613ff01ec2cf4670f1632d46786eb2a5b77900f950357a9eaa8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622725"
---
# <a name="running-with-administrator-privileges"></a>Ejecución con privilegios de administrador

El primer paso para establecer en qué tipo de cuenta debe ejecutarse la aplicación es examinar qué recursos usará la aplicación y a qué API con privilegios llamará. Es posible que la aplicación, o partes grandes de ella, no requiera privilegios de administrador. *Escribir código seguro*, de Michael Howard y David LeBlanc ofrece una descripción excelente de cómo llevar a cabo esta evaluación y es muy recomendable. (Es posible que este recurso no esté disponible en algunos idiomas y países).

Puede proporcionar los privilegios que necesita la aplicación con menos exposición a ataques malintencionados mediante uno de los enfoques siguientes:

-   Ejecutar en una cuenta con menos privilegios. Una manera de hacerlo es usar [**PrivilegeCheck para**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-privilegecheck) determinar qué privilegios están habilitados en un token. Si los privilegios disponibles no son adecuados para la operación actual, puede deshabilitar ese código y pedir al usuario que inicie sesión en una cuenta con privilegios de administrador.
-   Interrumpir en una aplicación independiente funciones que requieren permisos de administrador. Puede proporcionar al usuario un acceso directo que ejecute el comando RunAs. Para obtener instrucciones detalladas sobre cómo configurar el acceso directo, busque "runas" en la Ayuda. Mediante programación, puede configurar el [comando RunAs](/windows/desktop/com/runas) en la clave del Registro [AppId Key](/windows/desktop/com/appid-key) de la aplicación.
-   Autentique al usuario mediante una llamada a [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa) (GUI) o [**CredUICmdLinePromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduicmdlinepromptforcredentialsa) (línea de comandos) para obtener el nombre de usuario y la contraseña. Para obtener un ejemplo, vea [Asking the User for Credentials](asking-the-user-for-credentials.md).
-   Suplantar al usuario. Un proceso que se inicia en una cuenta con privilegios elevados, como System, puede suplantar una cuenta de usuario mediante una llamada a [**ImpersonateLoggedOnUser**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-impersonateloggedonuser) o a funciones impersonate similares, lo que reduce el nivel de privilegios. Sin embargo, si se inserta una llamada a [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) en el subproceso, el proceso vuelve a los privilegios originales del sistema.

Si ha determinado que la aplicación debe ejecutarse en una cuenta con privilegios de [](handling-passwords.md) administrador y que una contraseña de administrador debe almacenarse en el sistema de software, consulte Control de contraseñas para los métodos de hacerlo de forma segura.

 

 
