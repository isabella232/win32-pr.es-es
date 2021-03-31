---
title: Deshabilitar características de Servicios de Escritorio remoto
description: Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/01/2020
ms.locfileid: "103995811"
---
# <a name="disabling-remote-desktop-services-features"></a>Deshabilitar características de Servicios de Escritorio remoto

Para mejorar la seguridad, puede optar por deshabilitar Servicios de Escritorio remoto características como el redireccionamiento del portapapeles y la redirección de la impresora para los clientes que se conectan a los servidores host de sesión Escritorio remoto (host de sesión de escritorio remoto) mediante el control ActiveX Escritorio remoto.

**Para deshabilitar las características de Servicios de Escritorio remoto**

1.  Edite el registro del equipo cliente y agregue las claves siguientes:

    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableClipboardRedirection**
    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisableDriveRedirection**
    -   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server \\ DisablePrinterRedirection**

2.  Establezca el valor de ambas claves en **reg \_ DWORD** 1.

 

 




