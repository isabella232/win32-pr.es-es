---
description: Si esta Directiva del sistema por equipo está establecida en 1, un usuario o un administrador no puede quitar las revisiones del equipo.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908187"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Si esta [Directiva del sistema](system-policy.md) por equipo está establecida en 1, un usuario o un administrador no puede quitar las revisiones del equipo. El Windows Installer todavía puede quitar una revisión que ya no es aplicable a un producto. Si no se establece esta Directiva, un usuario puede quitar una revisión del equipo sólo si se le han concedido privilegios para quitar la revisión. Esto puede depender de si el usuario es un administrador, si la configuración de la Directiva de [DisableMsi](disablemsi.md) y [AlwaysInstallElevated](alwaysinstallelevated.md) está establecida, y si la revisión se instaló en un contexto administrado por usuario, no administrado por usuario o por equipo.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



