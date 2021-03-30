---
description: La interfaz IUpdateDownloader define las siguientes propiedades.
ms.assetid: b6a30356-f97d-408f-becd-a467e9f8e79f
title: Propiedades de IUpdateDownloader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99c16aa762bcc14dc1919ef91d162752652c327e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810213"
---
# <a name="iupdatedownloader-properties"></a><span data-ttu-id="2cf4d-103">Propiedades de IUpdateDownloader</span><span class="sxs-lookup"><span data-stu-id="2cf4d-103">IUpdateDownloader Properties</span></span>

<span data-ttu-id="2cf4d-104">La interfaz [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="2cf4d-104">The [**IUpdateDownloader**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloader) interface defines the following properties.</span></span>



| <span data-ttu-id="2cf4d-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2cf4d-105">Property</span></span>                                                             | <span data-ttu-id="2cf4d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="2cf4d-106">Description</span></span>                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cf4d-107">**ClientApplicationID**</span><span class="sxs-lookup"><span data-stu-id="2cf4d-107">**ClientApplicationID**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_clientapplicationid) | <span data-ttu-id="2cf4d-108">Obtiene y establece la aplicación cliente actual.</span><span class="sxs-lookup"><span data-stu-id="2cf4d-108">Gets and sets the current client application.</span></span>                                                                                                                              |
| [<span data-ttu-id="2cf4d-109">**IsForced**</span><span class="sxs-lookup"><span data-stu-id="2cf4d-109">**IsForced**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_isforced)                       | <span data-ttu-id="2cf4d-110">Obtiene y establece un valor booleano que indica si el agente de Windows Update (WUA) fuerza la descarga de actualizaciones que ya están instaladas o que no se pueden instalar.</span><span class="sxs-lookup"><span data-stu-id="2cf4d-110">Gets and sets a Boolean value that indicates whether the Windows Update Agent (WUA) forces the download of updates that are already installed or that cannot be installed.</span></span> |
| [<span data-ttu-id="2cf4d-111">**Priority**</span><span class="sxs-lookup"><span data-stu-id="2cf4d-111">**Priority**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_priority)                       | <span data-ttu-id="2cf4d-112">Obtiene y establece el nivel de prioridad de la descarga.</span><span class="sxs-lookup"><span data-stu-id="2cf4d-112">Gets and sets the priority level of the download.</span></span>                                                                                                                          |
| [<span data-ttu-id="2cf4d-113">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="2cf4d-113">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-get_updates)                         | <span data-ttu-id="2cf4d-114">Obtiene y establece una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican para su descarga.</span><span class="sxs-lookup"><span data-stu-id="2cf4d-114">Gets and sets an interface that contains a read-only collection of the updates that are specified for download.</span></span>                                                            |



 

 

 



