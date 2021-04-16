---
description: La interfaz IDownloadJob define las siguientes propiedades.
ms.assetid: 50e672d7-0ad6-402d-878c-4ac79b70a036
title: Propiedades de IDownloadJob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18c9bd940b4b091f2eeefbaaa2a60d66306a3e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705741"
---
# <a name="idownloadjob-properties"></a><span data-ttu-id="cc2a3-103">Propiedades de IDownloadJob</span><span class="sxs-lookup"><span data-stu-id="cc2a3-103">IDownloadJob Properties</span></span>

<span data-ttu-id="cc2a3-104">La interfaz [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="cc2a3-104">The [**IDownloadJob**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadjob) interface defines the following properties.</span></span>



| <span data-ttu-id="cc2a3-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="cc2a3-105">Property</span></span>                                        | <span data-ttu-id="cc2a3-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc2a3-106">Description</span></span>                                                                                                                                              |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cc2a3-107">**AsyncState**</span><span class="sxs-lookup"><span data-stu-id="cc2a3-107">**AsyncState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_asyncstate)   | <span data-ttu-id="cc2a3-108">Obtiene el objeto de estado específico del llamador que se pasa al método [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) .</span><span class="sxs-lookup"><span data-stu-id="cc2a3-108">Gets the caller-specific state object that is passed to the [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) method.</span></span>           |
| [<span data-ttu-id="cc2a3-109">**IsCompleted**</span><span class="sxs-lookup"><span data-stu-id="cc2a3-109">**IsCompleted**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_iscompleted) | <span data-ttu-id="cc2a3-110">Obtiene el valor que indica si la llamada a [**IUpdateDownloader. BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) se procesó completamente.</span><span class="sxs-lookup"><span data-stu-id="cc2a3-110">Gets the setting that indicates whether the call to [**IUpdateDownloader.BeginDownload**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatedownloader-begindownload) was processed completely.</span></span> |
| [<span data-ttu-id="cc2a3-111">**Actualizaciones**</span><span class="sxs-lookup"><span data-stu-id="cc2a3-111">**Updates**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadjob-get_updates)         | <span data-ttu-id="cc2a3-112">Obtiene una interfaz que contiene una colección de solo lectura de las actualizaciones que se especifican en una descarga.</span><span class="sxs-lookup"><span data-stu-id="cc2a3-112">Gets an interface that contains a read-only collection of the updates that are specified in a download.</span></span>                                                  |



 

 

 



