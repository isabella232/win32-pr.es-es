---
description: Al establecer la directiva TransformsSecure en 1, se informa al instalador de que las transformaciones se almacenarán en caché localmente en el equipo del usuario en una ubicación donde el usuario no tenga acceso de escritura.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: TransformsSecure Policy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6300a25db8e80003ff2a03afd56b168b9697f92764f16a26e99860c0a27796bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500305"
---
# <a name="transformssecure-policy"></a>TransformsSecure Policy

Al establecer la directiva TransformsSecure en 1, se informa al instalador de que las transformaciones se almacenarán en caché localmente en el equipo del usuario en una ubicación donde el usuario no tenga acceso de escritura. Establecer esta directiva es lo mismo que establecer la [propiedad TRANSFORMSSECURE,](transformssecure.md) salvo que el ámbito es diferente. El establecimiento de la directiva TransformsSecure se aplica a todos los paquetes instalados en un equipo determinado. El establecimiento de la propiedad TRANSFORMSSECURE se aplica al paquete independientemente del equipo.

El propósito de esta directiva es proporcionar almacenamiento de transformación seguro con usuarios que viajan Windows 2000. A partir Windows Server 2003, el valor predeterminado de esta directiva es 1.

Cuando se establece esta directiva, una [instalación de mantenimiento](maintenance-installation.md) solo puede usar la transformación de la caché protegida. En caso de que el instalador encuentre que falta la transformación en el equipo local, el instalador intenta restaurar la transformación. Para que el instalador restaure la transformación, la transformación segura debe residir en un origen autorizado en la lista de origen del paquete de instalación. Para obtener más información, vea [Resistencia de origen.](source-resiliency.md) Se produce un error en la instalación de mantenimiento si la transformación no está disponible o no se puede cargar.

En Windows Server 2003, si no se establece esta directiva, el comportamiento predeterminado es almacenar las transformaciones en una ubicación segura. En todas las versiones anteriores a Windows Server 2003, si no se establece la directiva, el comportamiento predeterminado es almacenar las transformaciones en el perfil de usuarios.

Consulte también [Transformaciones protegidas](secured-transforms.md) para obtener más información.

Windows El instalador interpreta que [la directiva TransformsAtSource](transformsatsource-policy.md) es la misma que la directiva TransformsSecure.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



