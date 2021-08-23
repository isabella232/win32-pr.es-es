---
title: Deshabilitación de Servicios de Escritorio remoto características
description: Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e994999293a23468da78724fdcec8b09f3be4a5f814b4e805923f1bff469267d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401355"
---
# <a name="disabling-remote-desktop-services-features"></a>Deshabilitación de Servicios de Escritorio remoto características

Para mejorar la seguridad, puede optar por deshabilitar características de Servicios de Escritorio remoto como el redireccionamiento del Portapapeles y la redirección de impresoras para los clientes que se conectan Escritorio remoto servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) mediante el control Escritorio remoto ActiveX.

**Para deshabilitar Servicios de Escritorio remoto características**

1.  Edite el registro del equipo cliente y agregue las claves siguientes:

    -   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Establezca el valor de ambas claves en **REG \_ DWORD** 1.

 

 




