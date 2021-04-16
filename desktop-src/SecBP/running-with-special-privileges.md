---
description: Algunas funciones requieren privilegios especiales para ejecutarse correctamente.
ms.assetid: b25db548-d5ab-4276-9b50-36d030909384
title: Ejecutar con privilegios especiales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be662d187ef27c7afc12b031f2d8de225d34c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669739"
---
# <a name="running-with-special-privileges"></a>Ejecutar con privilegios especiales

Algunas funciones requieren [privilegios](/windows/desktop/SecAuthZ/privileges) especiales para ejecutarse correctamente. En algunos casos, la función solo puede ser ejecutada por determinados usuarios o por miembros de determinados grupos. El requisito más común es que el usuario sea un administrador local. Otras funciones requieren que la cuenta del usuario tenga habilitados los privilegios específicos.

Para reducir la posibilidad de que el código no autorizado pueda obtener el control, el sistema debe ejecutarse con los privilegios mínimos necesarios. Las aplicaciones que necesitan llamar a funciones que requieren privilegios especiales pueden dejar el sistema abierto para atacar a los hackers. Dichas aplicaciones deben diseñarse para que se ejecuten durante breves períodos de tiempo y deben informar al usuario de las implicaciones de seguridad implicadas.

Para obtener información sobre cómo ejecutar como usuarios diferentes y cómo habilitar los privilegios en la aplicación, vea los temas siguientes:<dl>

[Ejecutar con privilegios de administrador](running-with-administrator-privileges.md)  
[Solicitar credenciales al usuario](asking-the-user-for-credentials.md)  
[Cambiar los privilegios de un token](changing-privileges-in-a-token.md)  
[Asignación de privilegios a una cuenta](assigning-privileges-to-an-account.md)  
</dl>

 

 
