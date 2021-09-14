---
description: Las funciones, tablas y propiedades del instalador de Windows que se enumeran en esta página no son compatibles con Windows Installer&\# 160;3.0 y versiones anteriores.
ms.assetid: 35be6da4-2a20-4a7a-9f6e-0420cd5a227e
title: No se admite en Windows Installer 3.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003a43a3667ece516f921bd9ae49695ab3716c09
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161473"
---
# <a name="not-supported-in-windows-installer-30"></a>No se admite en Windows Installer 3.0

Las Windows, las tablas y las propiedades del instalador que se enumeran en esta página no son compatibles con Windows Installer 3.0 y versiones anteriores. La ausencia de una característica de esta lista no garantiza que se admite la característica. Consulte la documentación principal para determinar qué versión Windows instalador es necesaria para una característica determinada. Para obtener información sobre otras Windows installer, vea [Novedades de Windows Installer](what-s-new-in-windows-installer.md).

Windows El instalador 3.0 está disponible para Windows Server 2003, Windows XP o Windows 2000. Para obtener una lista de todas las versiones Windows installer y redistribuibles, vea Versiones publicadas [de Windows Installer](released-versions-of-windows-installer.md).

Las siguientes características no se admiten en Windows Installer 3.0 y versiones anteriores.

[Funciones del instalador](installer-functions.md)

-   [**MsiSetExternalUIRecord**](/windows/desktop/api/Msi/nf-msi-msisetexternaluirecord)
-   [**MsiNotifySidChange**](/windows/desktop/api/Msi/nf-msi-msinotifysidchangea)

Prototipo de función de devolución de llamada

-   [**REGISTRO DEL CONTROLADOR INSTALLUI \_ \_**](/windows/win32/api/msi/nc-msi-installui_handler_record)

[Tablas de base de datos](database-tables.md)

-   La columna Valor de [la tabla MsiPatchMetadata](msipatchmetadata-table.md) acepta **OptimizedInstallMode** y **MinorUpdateTargetRTM.**

[Propiedades](properties.md)

-   [**Propiedad Msix64**](msix64.md)

[Windows Instalador en sistemas operativos de 64 bits](windows-installer-on-64-bit-operating-systems.md)

-   La [**propiedad Resumen de plantilla**](template-summary.md) acepta el valor x64.

[Evaluadores de coherencia internos: TIC](internal-consistency-evaluators-ices.md)

-   [ICE99](ice99.md)

 

 
