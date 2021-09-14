---
description: Puede asignar privilegios a las cuentas mediante el complemento directiva de seguridad local Microsoft Management Console (MMC) (Secpol.msc) o llamando a la función LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Asignación de privilegios a una cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0865a59b8bad75e687fd12f6bfc42c2cd39f664d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071193"
---
# <a name="assigning-privileges-to-an-account"></a>Asignación de privilegios a una cuenta

Puede asignar privilegios a las cuentas mediante el complemento directiva de seguridad local Microsoft Management Console (MMC) (Secpol.msc) o llamando a la función [**LsaAddAccountRights.**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights)

La asignación de un privilegio a una cuenta no afecta a los tokens de usuario existentes. Un usuario debe cerrar sesión y volver a iniciar sesión para obtener un token de acceso con el privilegio recién asignado.

Para asignar privilegios mediante el complemento MMC directiva de seguridad local, edite la lista de usuarios para cada privilegio que aparece en Security **Configuración/Local Policies/User Rights Assignment**.

 

 
