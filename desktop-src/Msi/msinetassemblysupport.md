---
description: La propiedad MsiNetAssemblySupport indica si el equipo admite ensamblados de Common Language Runtime en tiempo de ejecución.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propiedad MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653505"
---
# <a name="msinetassemblysupport-property"></a>Propiedad MsiNetAssemblySupport

La propiedad **MsiNetAssemblySupport** indica si el equipo admite ensamblados de Common Language Runtime en tiempo de ejecución. En los sistemas que admiten los ensamblados en tiempo de ejecución de Common Language Runtime, el instalador establece el valor de **MsiNetAssemblySupport** en la versión de archivo de Fusion.dll. El instalador no establece esta propiedad si el sistema operativo no admite ensamblados en tiempo de ejecución de Common Language Runtime. Cuando se instalan varias versiones de Fusion.dll en paralelo en el equipo del usuario, esta propiedad se establece en la versión más reciente del archivo de Fusion.dll. Por ejemplo, si .NET Framework versión 1.0.3705 (Fusion.dll versión 1.0.3705.15) y .NET Framework versión 1.1.4322 (Fusion.dll versión 1.1.4322.314) se instalan en paralelo, la propiedad **MsiNetAssemblySupport** se establece en 1.1.4322.314. Para obtener más información, vea [ensamblados](assemblies.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP. Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




