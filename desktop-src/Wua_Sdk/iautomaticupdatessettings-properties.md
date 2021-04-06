---
description: La interfaz IAutomaticUpdatesSettings define las siguientes propiedades.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propiedades de IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2463fdc69fc93960ee45c0003a65894eaaf7399
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001206"
---
# <a name="iautomaticupdatessettings-properties"></a>Propiedades de IAutomaticUpdatesSettings

La interfaz [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define las siguientes propiedades.



| Propiedad                                                                                 | Descripción                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Obtiene y establece cómo se notifica a los usuarios acerca de los eventos de actualización automática.                              |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Obtiene un valor booleano que indica si la configuración de actualización automática es de solo lectura.         |
| [**Obligatorio**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Obtiene un valor booleano que indica si directiva de grupo requiere el servicio Actualizaciones automáticas. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Obtiene y establece los días de la semana en los que Actualizaciones automáticas instala o desinstala las actualizaciones.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Obtiene y establece la hora a la que Actualizaciones automáticas instala o desinstala las actualizaciones.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2 proporcionan solo compatibilidad limitada para [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) y [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime). Si el equipo se ha configurado a través de directiva de grupo para utilizar un día y una hora de instalación programada, las propiedades **ScheduledInstallationDay** y **ScheduledInstallationTime** devuelven este día y hora programados. Si el equipo no se ha configurado a través de directiva de grupo de esta manera, las propiedades **ScheduledInstallationDay** y **ScheduledInstallationTime** devuelven valores predeterminados y no confiables. Si intenta modificar el día y la hora de instalación programada en estos sistemas operativos, **ScheduledInstallationDay** y **ScheduledInstallationTime** parecen correctos, pero no tienen ningún efecto.

 

 

 



