---
description: Si esta Directiva del sistema por equipo está establecida en 1 (uno), Windows Installer no interactúa con el administrador de reinicio, pero usará el cuadro de diálogo FilesInUse. Si esta Directiva del sistema por equipo está establecida en 2 (dos), Windows Installer utiliza el cuadro de diálogo FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666885"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

Si esta Directiva del sistema por equipo está establecida en 1 (uno), Windows Installer no interactúa con el [Administrador de reinicio](/windows/desktop/RstMgr/restart-manager-portal), pero utilizará el [cuadro de diálogo FilesInUse](filesinuse-dialog.md).

Si esta Directiva del sistema por equipo está establecida en 2 (dos), Windows Installer usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md). Esta configuración deshabilita los intentos del [Administrador de reinicio](/windows/desktop/RstMgr/restart-manager-portal) para mitigar los reinicios al instalar un paquete de Windows Installer que no se ha creado para usar el administrador de reinicio. El instalador sigue usando el administrador de reinicio para detectar los archivos que usan las aplicaciones.

La Directiva DisableAutomaticApplicationShutdown está disponible a partir de Windows Installer versión 4,0 en Windows Vista.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ \_** Directivas de software de equipo local \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**\_valor DWORD reg**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
