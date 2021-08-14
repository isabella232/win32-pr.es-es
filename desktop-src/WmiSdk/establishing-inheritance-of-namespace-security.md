---
description: Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Establecer la herencia de la seguridad del espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951bd5a2a14aa0a62620090d07df9bc56e8a0832674f2c1eee84369f4e2b4dae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119411915"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Establecer la herencia de la seguridad del espacio de nombres

Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.

Los espacios de nombres WMI tienen descriptores de seguridad que controlan quién puede tener acceso al espacio de nombres y a los datos del espacio de nombres. Cada descriptor de seguridad tiene una lista de control de acceso discrecional (DACL) y una lista de control de acceso de seguridad (SACL). Estas listas contienen entradas de control de acceso (ACE).

En función de las constantes de marca [**ACE**](namespace-ace-flag-constants.md) de espacio de nombres que se establezcan, todos los espacios de nombres secundarios de ese espacio de nombres pueden heredar los permisos que se aplican a un espacio de nombres. Un espacio de nombres secundario hereda el descriptor de seguridad de su espacio de nombres primario cuando se crea el espacio de nombres secundario si la marca **ACE CONTAINER \_ INHERIT \_** está en el descriptor de seguridad del espacio de nombres primario. Si **CONTAINER INHERIT ACE NO \_ \_ \| \_ PROPOGATE \_ INHERIT \_ ACE** está establecido, solo el espacio de nombres secundario hereda el descriptor de seguridad, no los espacios de nombres secundarios. Los espacios de nombres secundarios pueden invalidar los permisos de seguridad de su elemento primario llamando a métodos de la [**\_ \_ clase SystemSecurity**](--systemsecurity.md) para escribir un nuevo descriptor de seguridad. No se puede cambiar la configuración de seguridad predeterminada. Para obtener más información, vea [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md). Para obtener más información sobre las DACL, vea listas de Access Control [(ACL)](/windows/desktop/SecAuthZ/access-control-lists) y Constantes de tipo [**ACE de espacio de nombres**](namespace-ace-type-constants.md).

Tenga en cuenta que no se pueden cambiar los permisos predeterminados. Además, no se usa SE la marca **\_ DACL \_ PROTECTED** al establecer el descriptor de seguridad (SD) para agregar un SD especializado a un espacio de nombres secundario. Para invalidar una SD heredada, basta con establecer una nueva. Para heredar esa SD a un espacio de nombres secundario, pase la **marca ACE CONTAINER \_ \_ INHERIT** en el descriptor de seguridad del espacio de nombres. Para heredar solo al elemento secundario y no a los descendientes, pase `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer descriptores de seguridad namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
