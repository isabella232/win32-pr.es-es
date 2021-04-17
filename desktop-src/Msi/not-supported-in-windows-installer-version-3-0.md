---
description: Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer&\# 160; 3.0 y versiones anteriores.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: No se admite en Windows Installer 3,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677655"
---
# <a name="not-supported-in-windows-installer-30"></a>No se admite en Windows Installer 3,0

Las funciones, tablas y propiedades de Windows Installer que se enumeran en esta página no se admiten en Windows Installer 3,0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admita la característica. Consulte la documentación principal para determinar qué versión de Windows Installer es necesaria para una característica determinada. Para obtener información sobre otras versiones de Windows Installer, vea [novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows Installer 3,0 está disponible para Windows Server 2003, Windows XP o Windows 2000. Para obtener una lista de todas las versiones de Windows Installer y redistribuibles, consulte [versiones publicadas de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 3,0 y versiones anteriores.

[Funciones del instalador](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Prototipo de función de devolución de llamada

-   [**\_registro del controlador de INSTALLUI \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tablas de base de datos](database-tables.md)

-   La columna valor de la [tabla MsiPatchMetadata](msipatchmetadata-table.md) acepta **OptimizedInstallMode** y **MinorUpdateTargetRTM**.

[Propiedades](properties.md)

-   [**Propiedad Msix64**](msix64.md)

[Windows Installer en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   La [**propiedad de Resumen**](template-summary.md) de la plantilla acepta el valor x64.

[Evaluadores de coherencia interna-CIEM](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
