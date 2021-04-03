---
description: La interfaz IInstallationJob define las siguientes propiedades.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Propiedades de IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81b0083acd90b174349c105525676741c762aa05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810220"
---
# <a name="iinstallationjob-properties"></a>Propiedades de IInstallationJob

La interfaz [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define las siguientes propiedades.



| Propiedad                                            | Descripción                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Obtiene el objeto de estado específico del llamador que se pasa al método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Obtiene un valor que indica si se procesa completamente una llamada al método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) . |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Obtiene una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican en la instalación o desinstalación.                                                                                                        |



 

 

 



