---
description: Si no se establece esta directiva de sistema por equipo, solo los administradores pueden aplicar revisiones a los productos existentes que se instalaron con privilegios elevados.
ms.assetid: cd07dcb0-b9b5-4186-a916-604c40f88b5f
title: AllowLockdownPatch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85507d4f24209220ffb64411b452bbe46f3c76a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159148"
---
# <a name="allowlockdownpatch"></a>AllowLockdownPatch

Si no se establece esta directiva [de sistema](system-policy.md) por equipo, solo los administradores pueden aplicar revisiones a los productos existentes que se instalaron con privilegios elevados. Si AllowLockdownPatch está establecido en "1", los usuarios no administrativos pueden, en algunos casos, aplicar revisiones a los productos mientras se ejecuta una instalación con privilegios elevados. Con la directiva establecida, la revisión puede instalar actualizaciones [secundarias](minor-upgrades.md) mientras se ejecuta una instalación con privilegios elevados, la revisión no puede instalar [actualizaciones principales](major-upgrades.md). Establecer esta directiva también permite a los usuarios no administrativos ejecutar programas con privilegios LocalSystem durante una instalación con privilegios elevados.

Se recomienda la configuración predeterminada para garantizar un entorno seguro.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="remarks"></a>Observaciones

Cualquier usuario puede aplicar una revisión durante una instalación sin cambios. Establecer esta directiva [](system-policy.md) de sistema por máquina en "1" proporciona a los usuarios no administradores la flexibilidad adicional de aplicar revisiones a cualquier producto durante una instalación con privilegios elevados. Si no se establece esta directiva, los usuarios no administradores no pueden aplicar una revisión a las aplicaciones asignadas o publicadas.

Establecer esta directiva también permite a los usuarios no administrativos ejecutar programas arbitrarios con privilegios LocalSystem si tienen un paquete de revisión del instalador de Windows que instala o inicia esos programas.

 

 



