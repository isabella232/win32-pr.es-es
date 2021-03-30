---
description: Al establecer la Directiva TransformsSecure en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Directiva TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907617"
---
# <a name="transformssecure-policy"></a>Directiva TransformsSecure

Al establecer la Directiva TransformsSecure en 1 se informa al instalador de que las transformaciones se almacenan en caché localmente en el equipo del usuario en una ubicación en la que el usuario no tiene acceso de escritura. Establecer esta directiva es igual que establecer la [propiedad TRANSFORMSSECURE](transformssecure.md) , excepto que el ámbito es diferente. La configuración de la Directiva TransformsSecure se aplica a todos los paquetes instalados en un equipo determinado. El establecimiento de la propiedad TRANSFORMSSECURE se aplica al paquete independientemente del equipo.

La finalidad de esta directiva es proporcionar almacenamiento de transformación seguro con usuarios móviles de Windows 2000. A partir de Windows Server 2003, el valor predeterminado de esta directiva es 1.

Cuando se establece esta Directiva, una [instalación de mantenimiento](maintenance-installation.md) solo puede utilizar la transformación de la caché protegida. En caso de que el instalador encuentre que falta la transformación en el equipo local, el instalador intenta restaurar la transformación. Para que el instalador restaure la transformación, la transformación segura debe residir en un origen autorizado en la lista de origen del paquete de instalación. Para obtener más información, consulte [resistencia del origen](source-resiliency.md). Se produce un error en la instalación de mantenimiento si la transformación no está disponible o no se puede cargar.

En Windows Server 2003, si no se establece esta Directiva, el comportamiento predeterminado es almacenar las transformaciones en una ubicación segura. En todas las versiones anteriores a Windows Server 2003, si no se establece la Directiva, el comportamiento predeterminado es almacenar las transformaciones en el perfil de los usuarios.

Vea también [transformaciones protegidas](secured-transforms.md) para obtener más información.

Windows Installer interpreta que la [Directiva TransformsAtSource](transformsatsource-policy.md) es la misma que la Directiva TransformsSecure.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



