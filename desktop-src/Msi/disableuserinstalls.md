---
description: Se trata de una directiva del sistema por equipo que se puede usar cuando el administrador solo desea tener instaladas las aplicaciones por máquina.
ms.assetid: 3afa1d89-b76b-4184-b0d7-25cbf6749c7f
title: DisableUserInstalls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ee8275567c62fc383c0488d6ad3ef8dfc928f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153883"
---
# <a name="disableuserinstalls"></a>DisableUserInstalls

Se trata de una [Directiva del sistema](system-policy.md) por equipo que se puede usar cuando el administrador solo desea tener instaladas las aplicaciones por máquina.

Si no se establece esta Directiva, el instalador busca en el registro las aplicaciones en el siguiente orden: las aplicaciones administradas registradas como aplicaciones por usuario y no administradas registradas como por usuario y, por último, las aplicaciones registradas como por equipo.

Si esta Directiva se establece en 1, el instalador omite todas las aplicaciones registradas como por usuario y solo busca las aplicaciones registradas como por equipo. Las llamadas a la interfaz de programación de aplicaciones de Windows Installer o el sistema omiten las aplicaciones por usuario. Un intento de realizar una instalación en el [contexto de instalación](installation-context.md) por usuario hace que el instalador muestre un mensaje de error y detenga la instalación. En este caso, el Windows Installer también evita las instalaciones por usuario de un servidor de Terminal Server.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

 

 



