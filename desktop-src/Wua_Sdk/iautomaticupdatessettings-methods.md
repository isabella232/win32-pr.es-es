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
# <a name="iautomaticupdatessettings-methods"></a><span data-ttu-id="9feb0-103">Métodos IAutomaticUpdatesSettings</span><span class="sxs-lookup"><span data-stu-id="9feb0-103">IAutomaticUpdatesSettings Methods</span></span>

<span data-ttu-id="9feb0-104">La interfaz [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) define los siguientes métodos.</span><span class="sxs-lookup"><span data-stu-id="9feb0-104">The [**IAutomaticUpdatesSettings**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdatessettings) interface defines the following methods.</span></span>



| <span data-ttu-id="9feb0-105">Método</span><span class="sxs-lookup"><span data-stu-id="9feb0-105">Method</span></span>                                               | <span data-ttu-id="9feb0-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="9feb0-106">Description</span></span>                                      |
|------------------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="9feb0-107">**Actualizar**</span><span class="sxs-lookup"><span data-stu-id="9feb0-107">**Refresh**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-refresh) | <span data-ttu-id="9feb0-108">Recupera la configuración de la Actualizaciones automáticas más reciente.</span><span class="sxs-lookup"><span data-stu-id="9feb0-108">Retrieves the latest Automatic Updates settings.</span></span> |
| [<span data-ttu-id="9feb0-109">**Guardar**</span><span class="sxs-lookup"><span data-stu-id="9feb0-109">**Save**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save)       | <span data-ttu-id="9feb0-110">Aplica la configuración de Actualizaciones automáticas actual.</span><span class="sxs-lookup"><span data-stu-id="9feb0-110">Applies the current Automatic Updates settings.</span></span>  |



 

> [!Note]  
> <span data-ttu-id="9feb0-111">En Windows RT, ya no se puede usar el método [**IAutomaticUpdatesSettings:: Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) para configurar los valores de Windows Update mediante programación.</span><span class="sxs-lookup"><span data-stu-id="9feb0-111">On Windows RT, you can no longer use the [**IAutomaticUpdatesSettings::Save**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdatessettings-save) method to configure Windows Update settings programmatically.</span></span> <span data-ttu-id="9feb0-112">Se produce un error en la operación de configuración si usa **Guardar** para establecer un valor distinto de 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span><span class="sxs-lookup"><span data-stu-id="9feb0-112">The configuration operation fails if you use **Save** to set any value other than 4 ([**aunlScheduledInstallation**](/windows/win32/api/wuapi/ne-wuapi-automaticupdatesnotificationlevel)).</span></span>

 

 

 



