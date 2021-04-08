---
description: Si no se establece esta Directiva del sistema por equipo, solo los administradores pueden aplicar revisiones a los productos existentes que se instalaron con privilegios elevados.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001754"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Si no se establece esta [Directiva del sistema](system-policy.md) por equipo, solo los administradores pueden aplicar revisiones a los productos existentes que se instalaron con privilegios elevados. Si AllowLockdownPatch se establece en "1", los usuarios no administrativos pueden, en algunos casos, aplicar revisiones a los productos mientras se ejecuta una instalación con privilegios elevados. Con la directiva establecida, la revisión puede instalar [actualizaciones secundarias](minor-upgrades.md) mientras se ejecuta una instalación con privilegios elevados, la revisión no puede instalar las [actualizaciones principales](major-upgrades.md). La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas en privilegios LocalSystem durante una instalación con privilegios elevados.

Se recomienda la configuración predeterminada para garantizar un entorno seguro.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="remarks"></a>Observaciones

Cualquier usuario puede aplicar una revisión durante una instalación no elevada. La configuración de esta [Directiva del sistema](system-policy.md) por equipo en "1" proporciona a los usuarios no administrativos la flexibilidad adicional de aplicar revisiones a cualquier producto durante una instalación con privilegios elevados. Si no se establece esta Directiva, los usuarios no administrativos no podrán aplicar una revisión a las aplicaciones asignadas o publicadas.

La configuración de esta Directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios en privilegios LocalSystem si tienen un paquete de revisión Windows Installer que instala o inicia esos programas.

 

 



