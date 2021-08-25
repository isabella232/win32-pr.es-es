---
description: La interfaz IAutomaticUpdatesSettings define las siguientes propiedades.
ms.assetid: 663aaf7d-c701-4da8-ba92-7e0a6d0f35ba
title: Propiedades IAutomaticUpdatesSettings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6995264aebed44e8cb21e3880268a1488157ed5085645e5232feaa94a8786eed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897155"
---
# <a name="iautomaticupdatessettings-properties"></a>Propiedades IAutomaticUpdatesSettings

La [**interfaz IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define las siguientes propiedades.



| Propiedad                                                                                 | Descripción                                                                                      |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**NotificationLevel**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_notificationlevel)                 | Obtiene y establece cómo se notifica a los usuarios sobre los eventos de actualización automática.                              |
| [**Readonly**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_readonly)                                   | Obtiene un valor booleano que indica si la configuración de actualización automática es de solo lectura.         |
| [**Requerido**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_required)                                   | Obtiene un valor booleano que indica si directiva de grupo requiere el Actualizaciones automáticas servicio. |
| [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday)   | Obtiene y establece los días de la semana en los que Actualizaciones automáticas instala o desinstala las actualizaciones.    |
| [**ScheduledInstallationTime**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) | Obtiene y establece la hora a la que Actualizaciones automáticas instala o desinstala las actualizaciones.                |



 

> [!Note]  
> Windows 8, Windows 8.1, Windows Server 2012 y Windows Server 2012 R2 solo proporcionan compatibilidad limitada con [**ScheduledInstallationDay**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationday) y [**ScheduledInstallationTime.**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-get_scheduledinstallationtime) Si el equipo se ha configurado a través de directiva de grupo para usar un día y hora de instalación programados, las propiedades **ScheduledInstallationDay** y **ScheduledInstallationTime** devuelven este día y hora programados. Si el equipo no se ha configurado mediante directiva de grupo de esta manera, las propiedades **ScheduledInstallationDay** y **ScheduledInstallationTime** devuelven valores predeterminados y no confiables. Si intenta modificar el día y la hora de instalación programada en estos sistemas operativos, **ScheduledInstallationDay** y **ScheduledInstallationTime** parecen tener éxito, pero no tienen ningún efecto.

 

 

 



