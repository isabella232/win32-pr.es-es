---
title: Concesión de derechos de acceso a la cuenta de inicio de sesión de servicio
description: Una consideración principal de la instalación de una instancia de servicio es asegurarse de que el servicio instalado puede acceder a los recursos necesarios.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Concesión de derechos de acceso a ad de la cuenta de inicio de sesión de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d13d3e06432b3501961f65a3e27ca00a46f18197bef23d78e6f7ca0deec59b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118189084"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Concesión de derechos de acceso a la cuenta de inicio de sesión de servicio

Una consideración principal de la instalación de una instancia de servicio es asegurarse de que el servicio instalado puede acceder a los recursos necesarios. Para ello, establezca AEE en los descriptores de seguridad de los objetos a los que el servicio debe tener acceso. Una ACE puede conceder o denegar derechos de acceso a una entidad de seguridad especificada, como la cuenta de usuario de servicio, la cuenta de equipo para un servicio LocalSystem o un grupo al que pertenece la cuenta del servicio. Para obtener más información sobre las ACE, los descriptores de seguridad y el control de [acceso,](/windows/desktop/SecAuthZ/access-control)vea Controlar el acceso a objetos en [Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) y Access Control .

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE que permita al servicio modificar su punto de conexión de servicio, vea Habilitación de la cuenta de servicio para acceder a las [propiedades de SCP.](enabling-service-account-to-access-scp-properties.md)

En algunos casos, debe agregar su cuenta de usuario de servicio como miembro de uno o varios grupos de seguridad. Por ejemplo, si crea un grupo de administradores para el servicio, puede convertir el servicio en miembro del grupo. A continuación, puede conceder derechos de acceso al grupo en lugar de concederlos explícitamente a la cuenta de servicio. Para obtener más información sobre los grupos de seguridad, vea [Administrar grupos](managing-groups.md).

 

 