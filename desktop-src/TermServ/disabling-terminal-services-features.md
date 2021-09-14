---
title: Deshabilitación de Servicios de Escritorio remoto características
description: Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891108"
---
# <a name="disabling-remote-desktop-services-features"></a>Deshabilitación de Servicios de Escritorio remoto características

Para mejorar la seguridad, puede optar por deshabilitar características de Servicios de Escritorio remoto como el redireccionamiento del Portapapeles y el redireccionamiento de impresoras para los clientes que se conectan a servidores de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto) mediante el control Escritorio remoto ActiveX.

**Para deshabilitar Servicios de Escritorio remoto características**

1.  Edite el registro del equipo cliente y agregue las siguientes claves:

    -   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Establezca el valor de ambas claves en **REG \_ DWORD** 1.

 

 




