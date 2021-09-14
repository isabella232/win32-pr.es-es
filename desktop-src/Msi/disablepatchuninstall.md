---
description: Si esta directiva de sistema por equipo está establecida en 1, un usuario o un administrador no pueden quitar las revisiones del equipo.
ms.assetid: e964cb2b-ceaa-4122-bf54-cf1eeab4bc25
title: DisablePatchUninstall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de1bc85a249b4377024f22a7cd0451421dcd060
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158539"
---
# <a name="disablepatchuninstall"></a>DisablePatchUninstall

Si esta directiva de sistema [por](system-policy.md) equipo está establecida en 1, un usuario o un administrador no pueden quitar las revisiones del equipo. El Windows de aplicaciones todavía puede quitar una revisión que ya no es aplicable a un producto. Si no se establece esta directiva, un usuario puede quitar una revisión del equipo solo si se le han concedido privilegios para quitar la revisión. Esto puede depender de si el usuario es administrador, de si se ha establecido la configuración de directiva [DisableMsi](disablemsi.md) y [AlwaysInstallElevated,](alwaysinstallelevated.md) y de si la revisión se instaló en un contexto administrado por usuario, no administrado por usuario o por equipo.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



