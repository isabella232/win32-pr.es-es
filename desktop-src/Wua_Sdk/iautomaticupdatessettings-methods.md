---
description: La interfaz IAutomaticUpdatesSettings define los siguientes métodos.
ms.assetid: 2c6df896-bb59-4d77-acde-64e36ecb7d75
title: Métodos IAutomaticUpdatesSettings
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ecfc43539f70b9373a6db298acc6c688e83a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908539"
---
# <a name="iautomaticupdatessettings-methods"></a>Métodos IAutomaticUpdatesSettings

La interfaz [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define los siguientes métodos.



| Método                                               | Descripción                                      |
|------------------------------------------------------|--------------------------------------------------|
| [**Actualizar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | Recupera la configuración de la Actualizaciones automáticas más reciente. |
| [**Guardar**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | Aplica la configuración de Actualizaciones automáticas actual.  |



 

> [!Note]  
> En Windows RT, ya no se puede usar el método [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) para configurar los valores de Windows Update mediante programación. Se produce un error en la operación de configuración si usa **Guardar** para establecer un valor distinto de 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).

 

 

 



