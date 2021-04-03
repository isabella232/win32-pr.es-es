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
# <a name="iinstallationjob-properties"></a><span data-ttu-id="fd510-103">Propiedades de IInstallationJob</span><span class="sxs-lookup"><span data-stu-id="fd510-103">IInstallationJob Properties</span></span>

<span data-ttu-id="fd510-104">La interfaz [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="fd510-104">The [**IInstallationJob**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationjob) interface defines the following properties.</span></span>



| <span data-ttu-id="fd510-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="fd510-105">Property</span></span>                                            | <span data-ttu-id="fd510-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="fd510-106">Description</span></span>                                                                                                                                                                                                                            |
|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fd510-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="fd510-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_asyncstate)   | <span data-ttu-id="fd510-108">Obtiene el objeto de estado específico del llamador que se pasa al método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="fd510-108">Gets the caller-specific state object that is passed to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method.</span></span>               |
| [<span data-ttu-id="fd510-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="fd510-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_iscompleted) | <span data-ttu-id="fd510-110">Obtiene un valor que indica si se procesa completamente una llamada al método [**IUpdateInstaller. BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) o [**IUpdateInstaller. BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) .</span><span class="sxs-lookup"><span data-stu-id="fd510-110">Gets a value that indicates whether a call to the [**IUpdateInstaller.BeginInstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-begininstall) or [**IUpdateInstaller.BeginUninstall**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstaller-beginuninstall) method is completely processed.</span></span> |
| [<span data-ttu-id="fd510-111">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="fd510-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationjob-get_updates)         | <span data-ttu-id="fd510-112">Obtiene una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican en la instalación o desinstalación.</span><span class="sxs-lookup"><span data-stu-id="fd510-112">Gets an interface that contains a read-only collection of the updates that are specified in the installation or uninstallation.</span></span>                                                                                                        |



 

 

 



