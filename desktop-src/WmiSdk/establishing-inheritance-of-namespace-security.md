---
description: Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.
ms.assetid: d4fbd5af-69e2-4c60-907a-cb2a1506b7c9
ms.tgt_platform: multiple
title: Establecer la herencia de la seguridad del espacio de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e242299b78ede3ff49679305a97823bc022358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707093"
---
# <a name="establishing-inheritance-of-namespace-security"></a>Establecer la herencia de la seguridad del espacio de nombres

Puede controlar si un espacio de nombres secundario hereda el descriptor de seguridad del espacio de nombres primario.

Los espacios de nombres de WMI tienen descriptores de seguridad que controlan quién puede tener acceso al espacio de nombres y a los datos del espacio de nombres. Cada descriptor de seguridad tiene una lista de control de acceso discrecional (DACL) y una lista de control de acceso (SACL) de seguridad. Estas listas contienen entradas de control de acceso (ACE).

Dependiendo de las [**constantes de marca ACE del espacio de nombres**](namespace-ace-flag-constants.md) que se establezcan, los permisos que se aplican a un espacio de nombres pueden ser heredados por todos los espacios de nombres secundarios de ese espacio de nombres. Un espacio de nombres secundario hereda el descriptor de seguridad de su espacio de nombres primario cuando se crea el espacio de nombres secundario si el **contenedor hereda la marca \_ \_ ACE** en el descriptor de seguridad del espacio de nombres primario. Si **Container \_ Inherits \_ ACE no se establece \| \_ propagándose \_ inherit \_ ACE** , solo el espacio de nombres secundario hereda el descriptor de seguridad, no los espacios de nombres terciarios. Los espacios de nombres secundarios pueden invalidar los permisos de seguridad de su elemento primario llamando a los métodos de la clase [**\_ \_ SystemSecurity**](--systemsecurity.md) para escribir un nuevo descriptor de seguridad. No se puede cambiar la configuración de seguridad predeterminada. Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md). Para obtener más información acerca de las DACL, consulte [listas de Access Control (ACL)](/windows/desktop/SecAuthZ/access-control-lists) y [**constantes de tipo ACE de espacio de nombres**](namespace-ace-type-constants.md).

Tenga en cuenta que los permisos predeterminados no se pueden cambiar. Además, la configuración de la marca de **\_ DACL \_ protegida con DACL** al establecer el descriptor de seguridad (SD) no se usa para agregar un SD especializado a un espacio de nombres secundario. Para invalidar un SD heredado, basta con establecer uno nuevo. Para heredar la SD a un espacio de nombres secundario, pase la marca **\_ inherit inherit \_ ACE** en el descriptor de seguridad del espacio de nombres. Para heredar solo el elemento secundario, y no los descendientes, pase `CONTAINER_INHERIT_ACE|NO_PROPOGATE_INHERIT_ACE`

.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> </dl>

 

 
