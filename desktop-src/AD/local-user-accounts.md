---
title: Usar una cuenta de usuario local como cuenta de inicio de sesión de servicio
description: Una cuenta de usuario local (formato de nombre \ 0034;. \\ UserName \ 0034;) solo existe en la base de datos SAM del equipo host; no tiene un objeto de usuario en Active Directory Domain Services.
ms.assetid: a36d4d1c-3cfc-4ae1-8f1d-3f2e766f0c4b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a6d536b83675cc3d4fa9c23db01d8f4137fff228bf72444bec7164a51068ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186860"
---
# <a name="using-a-local-user-account-as-a-service-logon-account"></a>Usar una cuenta de usuario local como cuenta de inicio de sesión de servicio

Una cuenta de usuario local (formato de nombre: ". \\ *UserName*") solo existe en la base de datos SAM del equipo host; no tiene un objeto de usuario en Active Directory Domain Services. Esto significa que el dominio no puede autenticar una cuenta local. Por lo tanto, un servicio que se ejecuta en el contexto de seguridad de una cuenta de usuario local no tiene acceso a los recursos de red (excepto como usuario anónimo) y no puede admitir la autenticación mutua kerberos en la que sus clientes autentican el servicio. Por estos motivos, las cuentas de usuario locales no suelen ser adecuadas para los servicios habilitados para el uso de directorios. En el lado más, los errores del servicio no pueden dañar el sistema. Si el servicio se puede ejecutar con esas limitaciones, debe hacerlo.

 

 




