---
title: Directrices para seleccionar una cuenta de inicio de sesión de servicio
description: Un servicio basado en Win32 se puede ejecutar en el contexto de seguridad de una cuenta de usuario local, una cuenta de usuario de dominio o la cuenta LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Directrices para seleccionar una cuenta de inicio de sesión de servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a976927130a3585be2e6130dbb71b37fa0c69660b6ae953e28909fad3db570f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188679"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Directrices para seleccionar una cuenta de inicio de sesión de servicio

Un servicio basado en Win32 se puede ejecutar en el contexto de seguridad de una cuenta de usuario local, una cuenta de usuario de dominio o la cuenta LocalSystem. Para decidir qué cuenta usar, un administrador debe instalar el servicio con el conjunto mínimo de permisos necesarios para realizar las operaciones del servicio. En un servicio típico habilitado para directorios, esto significa que el instalador del servicio debe crear una cuenta de usuario de dominio para el servicio y conceder a esa cuenta los derechos de acceso y privilegios específicos que requiere el servicio en tiempo de ejecución. Un servicio solo debe ejecutarse en la cuenta LocalSystem si el servicio requiere privilegios administrativos o debe actuar como parte del sistema operativo en el equipo local.

Tenga en cuenta que, de forma predeterminada, el instalador del servicio debe configurar el servicio para que se ejecute en una cuenta de usuario de dominio. Para ejecutar el servicio en la cuenta LocalSystem, el instalador del servicio debe consultar al administrador para obtener permiso para hacerlo.

Para obtener más información sobre descripciones, ventajas y desventajas de cada tipo de cuenta, consulte:

-   [Cuentas de usuario locales](local-user-accounts.md).
-   [Cuentas de usuario de dominio](domain-user-accounts.md).
-   [La cuenta LocalSystem](the-localsystem-account.md).

 

 




