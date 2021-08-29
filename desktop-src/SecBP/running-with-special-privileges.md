---
description: Algunas funciones requieren privilegios especiales para ejecutarse correctamente.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Ejecución con privilegios especiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9bcd9db0f54c14c5a66d452e394252e6dacad933a92157f59811af90f84a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127275"
---
# <a name="running-with-special-privileges"></a>Ejecución con privilegios especiales

Algunas funciones requieren [privilegios especiales para](/windows/desktop/SecAuthZ/privileges) ejecutarse correctamente. En algunos casos, la función solo la pueden ejecutar determinados usuarios o miembros de determinados grupos. El requisito más común es que el usuario sea un administrador local. Otras funciones requieren que la cuenta del usuario tenga habilitados privilegios específicos.

Para reducir la posibilidad de que el código no autorizado pueda obtener el control, el sistema debe ejecutarse con los privilegios mínimos necesarios. Las aplicaciones que necesitan llamar a funciones que requieren privilegios especiales pueden dejar el sistema abierto a ataques por parte de hackers. Estas aplicaciones deben diseñarse para ejecutarse durante breves períodos de tiempo y deben informar al usuario de las implicaciones de seguridad implicadas.

Para obtener información sobre cómo ejecutarse como usuarios diferentes y cómo habilitar privilegios en la aplicación, consulte los temas siguientes:<dl>

[Ejecución con privilegios de administrador](running-with-administrator-privileges.md)  
[Pedir credenciales al usuario](asking-the-user-for-credentials.md)  
[Cambiar privilegios en un token](changing-privileges-in-a-token.md)  
[Asignación de privilegios a una cuenta](assigning-privileges-to-an-account.md)  
</dl>

 

 
