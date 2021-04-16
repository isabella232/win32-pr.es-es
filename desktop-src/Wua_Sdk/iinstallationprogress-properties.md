---
description: La interfaz IInstallationProgress define las siguientes propiedades.
ms.assetid: f16c682f-3e9f-4767-8f26-d7af0a14d720
title: Propiedades de IInstallationProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcbcdb162c544c81b96326ec7b2b7657d81538a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696576"
---
# <a name="iinstallationprogress-properties"></a><span data-ttu-id="41152-103">Propiedades de IInstallationProgress</span><span class="sxs-lookup"><span data-stu-id="41152-103">IInstallationProgress Properties</span></span>

<span data-ttu-id="41152-104">La interfaz [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="41152-104">The [**IInstallationProgress**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="41152-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="41152-105">Property</span></span>                                                                                   | <span data-ttu-id="41152-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="41152-106">Description</span></span>                                                                                                                                        |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="41152-107">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="41152-107">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdateindex)                     | <span data-ttu-id="41152-108">Obtiene un valor de índice de base cero que especifica la actualización que se está instalando o desinstalando cuando se han seleccionado varias actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="41152-108">Gets a zero-based index value that specifies the update that is currently being installed or uninstalled when multiple updates have been selected.</span></span> |
| [<span data-ttu-id="41152-109">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="41152-109">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="41152-110">Obtiene el progreso del proceso de instalación o desinstalación de la actualización actual, en forma de porcentaje.</span><span class="sxs-lookup"><span data-stu-id="41152-110">Gets how far the installation or uninstallation process for the current update has progressed, as a percentage.</span></span>                                    |
| [<span data-ttu-id="41152-111">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="41152-111">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationprogress-get_percentcomplete)                           | <span data-ttu-id="41152-112">Obtiene hasta qué punto ha progresado el proceso de instalación o desinstalación global, como un porcentaje.</span><span class="sxs-lookup"><span data-stu-id="41152-112">Gets how far the overall installation or uninstallation process has progressed, as a percentage.</span></span>                                                   |



 

 

 



