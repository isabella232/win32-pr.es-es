---
description: La interfaz IUpdateServiceManager define los siguientes métodos.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Métodos IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464b0b6e48d074dbc43f370f267fe7a526e8269b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540139"
---
# <a name="iupdateservicemanager-methods"></a>Métodos IUpdateServiceManager

La interfaz [**IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) define los siguientes métodos.



| Método                                                                           | Descripción                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | Registra un paquete de examen como un servicio con Windows Update Agent (WUA) y, a continuación, devuelve una interfaz [**IUpdateService**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) .    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Registra un servicio con WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Registra un servicio con Actualizaciones automáticas.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Quita un registro de servicio de WUA.                                                                                                         |
| [**SetOption (**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Establece las opciones del objeto que especifica el identificador de servicio y si se muestra una advertencia al cambiar el registro de Actualizaciones automáticas. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Anula el registro de un servicio con Actualizaciones automáticas.                                                                                                    |



 

 

 



