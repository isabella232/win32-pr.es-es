---
description: La interfaz IUpdateServiceManager define los métodos siguientes.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: Métodos IUpdateServiceManager
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1486727db4ed4e9b561c19a1a2f3994bca0085e836ae774fda1c7db76df38144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994355"
---
# <a name="iupdateservicemanager-methods"></a>Métodos IUpdateServiceManager

La [**interfaz IUpdateServiceManager**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) define los métodos siguientes.



| Método                                                                           | Descripción                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | Registra un paquete de examen como servicio con Windows Update Agent (WUA) y, a continuación, devuelve una [**interfaz IUpdateService.**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Registra un servicio con WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Registra un servicio con Actualizaciones automáticas.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Quita un registro de servicio de WUA.                                                                                                         |
| [**Setoption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Establece opciones para el objeto que especifica el identificador de servicio y si se debe mostrar una advertencia al cambiar el registro de Actualizaciones automáticas. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Anula el registro de un servicio con Actualizaciones automáticas.                                                                                                    |



 

 

 



