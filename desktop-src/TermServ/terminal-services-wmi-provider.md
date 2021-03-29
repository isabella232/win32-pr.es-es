---
title: Servicios de Escritorio remoto proveedor WMI
description: El proveedor WMI de Servicios de Escritorio remoto proporciona acceso mediante programación a la información y la configuración que se exponen en el complemento configuración/conexiones de Microsoft Management Console (MMC) de Servicios de Escritorio remoto.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de Servicios de Escritorio remoto, proveedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104077915"
---
# <a name="remote-desktop-services-wmi-provider"></a>Servicios de Escritorio remoto proveedor WMI

El proveedor WMI de Servicios de Escritorio remoto proporciona acceso mediante programación a la información y la configuración que se exponen en el complemento configuración/conexiones de Microsoft Management Console (MMC) de Servicios de Escritorio remoto.

El proceso de administración de Windows (Winmgmt.exe) carga la DLL del proveedor cuando un cliente realiza una solicitud al servidor. La administración es posible mediante el uso de los métodos de proveedor. El proveedor se registra como una instancia de y un proveedor de métodos.

El proveedor de WMI Servicios de Escritorio remoto se ha implementado como un proveedor dinámico derivado de la clase base del [**\_ servicio Win32**](/windows/desktop/CIMWin32Prov/win32-service) , heredando todas sus propiedades y métodos, y una biblioteca de vínculos dinámicos en proceso.

Para obtener más información, vea la [Referencia del proveedor de WMI de servicios de escritorio remoto](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios de Escritorio remoto referencia del proveedor WMI](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 