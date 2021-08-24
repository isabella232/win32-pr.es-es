---
description: La interfaz IAutomaticUpdatesSettings define los métodos siguientes.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Métodos IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5ae30a987dcf9d6573c179e7ef453c10c35a84b915b76a16439ba83a7174fd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049473"
---
# <a name="iautomaticupdatessettings-methods"></a>Métodos IAutomaticUpdatesSettings

La [**interfaz IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define los métodos siguientes.



| Método                                               | Descripción                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Actualizar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Recupera la configuración de Actualizaciones automáticas más reciente. |
| [**Guardar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Aplica la configuración de Actualizaciones automáticas actual.  |



 

> [!Note]  
> En Windows RT, ya no puede usar el método [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) para configurar Windows update mediante programación. Se produce un error en la operación de configuración si usa **Guardar** para establecer cualquier valor distinto de 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



