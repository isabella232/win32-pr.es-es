---
title: Configuración de la cuenta de usuario de un servicio
description: El instalador del servicio puede sugerir una cuenta de inicio de sesión predeterminada para una instancia de servicio y permitir al administrador seleccionar la cuenta predeterminada o especificar otra.
ms.assetid: 37285c23-8922-4da5-9f0b-922ea5e5794e
ms.tgt_platform: multiple
keywords:
- Configuración de la cuenta de usuario de un servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705fa16d8d2cce137755f4a5086716aaaef8046a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789454"
---
# <a name="setting-up-a-services-user-account"></a>Configuración de la cuenta de usuario de un servicio

El instalador del servicio puede sugerir una cuenta de inicio de sesión predeterminada para una instancia de servicio y permitir al administrador seleccionar la cuenta predeterminada o especificar otra. Si el administrador selecciona una cuenta de usuario, en lugar de la cuenta LocalSystem, la cuenta debe existir antes de llamar a la función [**CreateService**](/windows/desktop/api/winsvc/nf-winsvc-createservicea) para instalar una instancia del servicio en un servidor host. Para obtener más información y un ejemplo de código que se puede usar para crear un nuevo objeto de usuario de dominio en Active Directory Domain Services, consulte [crear un usuario](creating-a-user.md).

Idealmente, cada instancia de un servicio, ya sea un servicio basado en host o replicable, debe tener su propia cuenta de usuario de dominio. El uso de cuentas independientes para cada instancia de servicio es más seguro que tener varias instancias que comparten la misma cuenta. Además, el uso de cuentas independientes permite auditar las actividades de cada instancia de servicio.

Cuando el instalador sugiere una cuenta de inicio de sesión predeterminada, debe especificar el nombre de una cuenta nueva que se va a crear para la nueva instancia de servicio. El nombre de cuenta podría estar compuesto de los mismos elementos usados para crear un nombre de entidad de seguridad de servicio, como la clase de servicio, el equipo host y el nombre del servicio. Para obtener más información, consulte [Service Principal Names](service-principal-names.md) (Nombres de entidad de seguridad de servicio). Normalmente, se crea la cuenta en el contenedor usuarios del dominio del equipo host.

Debe generar una contraseña para cada cuenta. Para obtener más información acerca de cómo escribir una herramienta que automatice la tarea de actualizar las contraseñas de las cuentas de servicio, consulte [cambiar la contraseña en la cuenta de usuario de un servicio](changing-the-password-on-a-serviceampaposs-user-account.md).

 

 