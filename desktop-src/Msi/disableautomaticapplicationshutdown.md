---
description: Si esta directiva de sistema por máquina se establece en 1 (uno), el instalador de Windows no interactúa con el Administrador de reinicio, pero usará el cuadro de diálogo FilesInUse.Si esta directiva del sistema por máquina está establecida en 2 (dos), el instalador de Windows usa el cuadro de diálogo FilesInUse.
ms.assetid: a59de5bb-e0a1-459d-83e6-afaf81298123
title: DisableAutomaticApplicationShutdown
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 060c4027a1fb4026f4e1d578bd1d0c2ed8cd979c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158556"
---
# <a name="disableautomaticapplicationshutdown"></a>DisableAutomaticApplicationShutdown

Si esta directiva de sistema por equipo está establecida en 1 (uno), Windows Installer no interactúa con el Administrador de [reinicio,](/windows/desktop/RstMgr/restart-manager-portal)pero usará el cuadro de [diálogo FilesInUse](filesinuse-dialog.md).

Si esta directiva de sistema por equipo está establecida en 2 (dos), Windows Instalador usa el [cuadro de diálogo FilesInUse](filesinuse-dialog.md). Esta configuración deshabilita los [](/windows/desktop/RstMgr/restart-manager-portal) intentos del Administrador de reinicio para mitigar los reinicios al instalar un paquete de Windows Installer que no se ha creado para usar el Administrador de reinicio. El instalador sigue utilizando el Administrador de reinicio para detectar archivos en uso por parte de las aplicaciones.

La directiva DisableAutomaticApplicationShutdown está disponible a partir de Windows Installer versión 4.0 en Windows Vista.

## <a name="registry-key"></a>Clave del Registro

**HKEY \_ Local \_ MACHINE** \\ **Software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>Tipo de datos

**REG \_ DWORD**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**MSIRESTARTMANAGERCONTROL**](msirestartmanagercontrol.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
