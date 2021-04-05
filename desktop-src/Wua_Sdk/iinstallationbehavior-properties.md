---
description: La interfaz IInstallationBehavior define las siguientes propiedades.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Propiedades de IInstallationBehavior
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001199"
---
# <a name="iinstallationbehavior-properties"></a>Propiedades de IInstallationBehavior

La interfaz [**IInstallationBehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) define las siguientes propiedades.



| Propiedad                                                                                 | Descripción                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Obtiene un valor booleano thast indica si la instalación o desinstalación de una actualización puede solicitar la intervención del usuario.                                                        |
| [**Impacto**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Obtiene una enumeración [**InstallationImpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) que indica cómo afecta la instalación o desinstalación de la actualización al equipo.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Obtiene una enumeración [**InstallationRebootBehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) que especifica el comportamiento de reinicio que se produce al instalar o desinstalar la actualización. |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Obtiene un valor booleano que indica si la instalación o desinstalación de una actualización requiere conectividad de red.                                                     |



 

 

 



