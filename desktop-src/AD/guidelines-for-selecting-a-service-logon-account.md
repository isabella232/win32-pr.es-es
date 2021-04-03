---
title: Directrices para seleccionar una cuenta de inicio de sesión de servicio
description: Un servicio basado en Win32 puede ejecutarse en el contexto de seguridad de una cuenta de usuario local, una cuenta de usuario de dominio o la cuenta LocalSystem.
ms.assetid: aa2b93c7-335f-4e03-9198-fe2b396e296e
ms.tgt_platform: multiple
keywords:
- Directrices para seleccionar una cuenta de inicio de sesión de servicio AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bb8f5b4fe6a57863c09c9563454fc3ec09e75c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075118"
---
# <a name="guidelines-for-selecting-a-service-logon-account"></a>Directrices para seleccionar una cuenta de inicio de sesión de servicio

Un servicio basado en Win32 puede ejecutarse en el contexto de seguridad de una cuenta de usuario local, una cuenta de usuario de dominio o la cuenta LocalSystem. Para decidir qué cuenta usar, un administrador debe instalar el servicio con el conjunto mínimo de permisos necesario para realizar las operaciones de servicio. En un servicio típico habilitado para directorios, esto significa que el instalador del servicio debe crear una cuenta de usuario de dominio para el servicio y conceder a esa cuenta los derechos de acceso y privilegios específicos que requiere el servicio en tiempo de ejecución. Un servicio solo debe ejecutarse con la cuenta LocalSystem si el servicio requiere privilegios administrativos o debe actuar como parte del sistema operativo en el equipo local.

Tenga en cuenta que, de forma predeterminada, el instalador del servicio debe configurar el servicio para que se ejecute en una cuenta de usuario de dominio. Para ejecutar el servicio con la cuenta LocalSystem, el instalador del servicio debe consultar al administrador para obtener permiso para hacerlo.

Para obtener más información acerca de las descripciones, las ventajas y las desventajas de cada tipo de cuenta, consulte:

-   [Cuentas de usuario locales](local-user-accounts.md).
-   [Cuentas de usuario de dominio](domain-user-accounts.md).
-   [La cuenta LocalSystem](the-localsystem-account.md).

 

 




