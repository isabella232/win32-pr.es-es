---
title: Servicios de Escritorio remoto WMI
description: El Servicios de Escritorio remoto WMI proporciona acceso mediante programación a la información y la configuración expuestas por el complemento Servicios de Escritorio remoto Configuration/Connections Microsoft Management Console (MMC).
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , proveedor WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4ed84dee9b2521c392b8b39ee1297121a85e1c4f8ad41f7d96d0d73042a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869605"
---
# <a name="remote-desktop-services-wmi-provider"></a>Servicios de Escritorio remoto WMI

El Servicios de Escritorio remoto WMI proporciona acceso mediante programación a la información y la configuración expuestas por el complemento Servicios de Escritorio remoto Configuration/Connections Microsoft Management Console (MMC).

El proceso de administración de Windows (Winmgmt.exe) carga el archivo DLL del proveedor cuando un cliente realiza una solicitud al servidor. La administración es posible mediante los métodos del proveedor. El proveedor se registra como una instancia y un proveedor de métodos.

El proveedor WMI Servicios de Escritorio remoto se ha implementado como un proveedor dinámico derivado de la clase base del servicio [**Win32, \_**](/windows/desktop/CIMWin32Prov/win32-service) heredando todas sus propiedades y métodos, y una biblioteca de vínculos dinámicos en proceso.

Para obtener más información, vea el Servicios de Escritorio remoto [referencia del proveedor WMI](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Servicios de Escritorio remoto referencia del proveedor WMI](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 