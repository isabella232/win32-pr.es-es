---
title: Conceder derechos de acceso a la cuenta de inicio de sesión del servicio
description: Una consideración principal de la instalación de una instancia de servicio es asegurarse de que el servicio instalado pueda acceder a los recursos necesarios.
ms.assetid: 5b756318-f621-4fce-af2b-71ccccbb4e3c
ms.tgt_platform: multiple
keywords:
- Conceder derechos de acceso a la cuenta de inicio de sesión del servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f4ea5b85e6158109338b881eeb3f59d74a3910
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "105656338"
---
# <a name="granting-access-rights-to-the-service-logon-account"></a>Conceder derechos de acceso a la cuenta de inicio de sesión del servicio

Una consideración principal de la instalación de una instancia de servicio es asegurarse de que el servicio instalado pueda acceder a los recursos necesarios. Para ello, establezca las ACE en los descriptores de seguridad de los objetos a los que el servicio debe tener acceso. Una ACE puede conceder o denegar derechos de acceso a una entidad de seguridad especificada, como la cuenta de usuario de servicio, o la cuenta de equipo para un servicio LocalSystem, o un grupo al que pertenece la cuenta del servicio. Para obtener más información sobre las ACE, los descriptores de seguridad y el control de acceso, vea [controlar el acceso a objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md) y [Access Control](/windows/desktop/SecAuthZ/access-control).

Para obtener más información y un ejemplo de código que se puede usar para establecer una ACE que permita al servicio modificar su punto de conexión de servicio, consulte [habilitación de la cuenta de servicio para acceder a las propiedades de SCP](enabling-service-account-to-access-scp-properties.md).

En algunos casos, debe agregar la cuenta de usuario de servicio como miembro de uno o varios grupos de seguridad. Por ejemplo, si crea un grupo de administradores para su servicio, es posible que el servicio sea miembro del grupo. Después, puede conceder derechos de acceso al grupo en lugar de concederlos explícitamente a la cuenta de servicio. Para obtener más información acerca de los grupos de seguridad, consulte [Administración de grupos](managing-groups.md).

 

 