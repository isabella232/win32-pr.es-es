---
description: La interfaz IInstallationJob define las siguientes propiedades.
ms.assetid: 74087098-bef0-41f8-8d7b-bbca1d000df8
title: Propiedades de IInstallationJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb1604e69efc1d716b77be7303fc2148e93c0fe6d4fe2bc1ccd299f18ed9d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896985"
---
# <a name="iinstallationjob-properties"></a>Propiedades de IInstallationJob

La [**interfaz IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define las siguientes propiedades.



| Propiedad                                            | Descripción                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AsyncState**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | Obtiene el objeto de estado específico del autor de la llamada que se pasa al método [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) [**o IUpdateInstaller.BeginUninstall.**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall)               |
| [**IsCompleted**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | Obtiene un valor que indica si una llamada al método [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) está completamente procesada. |
| [**Actualizaciones**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | Obtiene una interfaz que contiene una colección de solo lectura de las actualizaciones especificadas en la instalación o desinstalación.                                                                                                        |



 

 

 



