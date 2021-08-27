---
description: La propiedad MsiNetAssemblySupport indica si el equipo admite ensamblados en tiempo de ejecución de lenguaje común.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: Propiedad MsiNetAssemblySupport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d135fcc9eb301d3624586318fdc0d5dbbc534c5771ee89d4ae625af78b0782
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944908"
---
# <a name="msinetassemblysupport-property"></a>Propiedad MsiNetAssemblySupport

La **propiedad MsiNetAssemblySupport** indica si el equipo admite ensamblados en tiempo de ejecución de lenguaje comunes. En los sistemas que admiten ensamblados en tiempo de ejecución de lenguaje comunes, el instalador establece el valor de **MsiNetAssemblySupport** en la versión de archivo de Fusion.dll. El instalador no establece esta propiedad si el sistema operativo no admite ensamblados en tiempo de ejecución de lenguaje comunes. Cuando se instalan varias versiones de Fusion.dll en paralelo en el equipo del usuario, esta propiedad se establece en la versión más reciente del archivo Fusion.dll usuario. Por ejemplo, si .NET Framework versión 1.0.3705 (Fusion.dll versión 1.0.3705.15) y .NET Framework versión 1.1.4322 (Fusion.dll versión 1.1.4322.314) se instalan en paralelo, La **propiedad MsiNetAssemblySupport** se establece en 1.1.4322.314. Para obtener más información, vea [Ensamblados](assemblies.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP. Consulte el [Windows installer Run-Time para](windows-installer-portal.md) obtener información sobre los requisitos mínimos de Windows Service Pack que requiere una versión Windows Installer.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades](properties.md)
</dt> </dl>

 

 




