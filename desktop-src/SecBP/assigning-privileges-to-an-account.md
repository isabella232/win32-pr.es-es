---
description: Puede asignar privilegios a las cuentas mediante el complemento directiva de seguridad local Microsoft Management Console (MMC) (Secpol.msc) o llamando a la función LsaAddAccountRights.
ms.assetid: F2DAB2E3-8B24-49A3-A2DD-E83B5181E9A2
title: Asignación de privilegios a una cuenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a4ba4fb5266a66aac67b17c70fc6bbcaa1a397a8593534144c688daaee5a0b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623015"
---
# <a name="assigning-privileges-to-an-account"></a>Asignación de privilegios a una cuenta

Puede asignar privilegios a las cuentas mediante el complemento de directiva de seguridad local Microsoft Management Console (MMC) (Secpol.msc) o llamando a la función [**LsaAddAccountRights.**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaaddaccountrights)

La asignación de un privilegio a una cuenta no afecta a los tokens de usuario existentes. Un usuario debe cerrar sesión y volver a iniciar sesión para obtener un token de acceso con el privilegio recién asignado.

Para asignar privilegios mediante el complemento MMC directiva de seguridad local, edite la lista de usuarios para cada privilegio que aparece en Security **Configuración/Local Policies/User Rights Assignment**.

 

 
