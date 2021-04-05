---
description: La interfaz IDownloadProgress define las siguientes propiedades.
ms.assetid: 8f64c702-b2b5-4a5f-9365-bc962e35f499
title: Propiedades de IDownloadProgress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 469246acb59b4aa58efcbf4bb5aa7f04b7e44b6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001202"
---
# <a name="idownloadprogress-properties"></a><span data-ttu-id="eb472-103">Propiedades de IDownloadProgress</span><span class="sxs-lookup"><span data-stu-id="eb472-103">IDownloadProgress Properties</span></span>

<span data-ttu-id="eb472-104">La interfaz [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) define las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="eb472-104">The [**IDownloadProgress**](/windows/desktop/api/Wuapi/nn-wuapi-idownloadprogress) interface defines the following properties.</span></span>



| <span data-ttu-id="eb472-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="eb472-105">Property</span></span>                                                                               | <span data-ttu-id="eb472-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="eb472-106">Description</span></span>                                                                                                                                      |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eb472-107">**CurrentUpdateBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="eb472-107">**CurrentUpdateBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytesdownloaded) | <span data-ttu-id="eb472-108">Obtiene una cadena que especifica la cantidad de datos transferidos para el archivo de contenido o los archivos de la actualización que se está descargando, en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb472-108">Gets a string that specifies how much data has been transferred for the content file or files of the update that is being downloaded, in bytes.</span></span>  |
| [<span data-ttu-id="eb472-109">**CurrentUpdateBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="eb472-109">**CurrentUpdateBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatebytestodownload) | <span data-ttu-id="eb472-110">Obtiene una cadena que calcula la cantidad de datos que se deben transferir para el archivo de contenido o los archivos de la actualización que se está descargando, en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb472-110">Gets a string that estimates how much data should be transferred for the content file or files of the update that is being downloaded, in bytes.</span></span> |
| [<span data-ttu-id="eb472-111">**CurrentUpdateDownloadPhase**</span><span class="sxs-lookup"><span data-stu-id="eb472-111">**CurrentUpdateDownloadPhase**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatedownloadphase)     | <span data-ttu-id="eb472-112">Obtiene un valor de enumeración [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) que especifica la fase de la descarga que está actualmente en curso.</span><span class="sxs-lookup"><span data-stu-id="eb472-112">Gets a [**DownloadPhase**](/windows/win32/api/wuapi/ne-wuapi-downloadphase) enumeration value that specifies the phase of the download that is currently in progress.</span></span>          |
| [<span data-ttu-id="eb472-113">**CurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="eb472-113">**CurrentUpdateIndex**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdateindex)                     | <span data-ttu-id="eb472-114">Obtiene un valor de índice de base cero que especifica la actualización que se está descargando actualmente cuando se han seleccionado varias actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="eb472-114">Gets a zero-based index value that specifies the update that is currently being downloaded when multiple updates have been selected.</span></span>             |
| [<span data-ttu-id="eb472-115">**CurrentUpdatePercentComplete**</span><span class="sxs-lookup"><span data-stu-id="eb472-115">**CurrentUpdatePercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_currentupdatepercentcomplete) | <span data-ttu-id="eb472-116">Obtiene una estimación del porcentaje de la actualización actual que se ha descargado.</span><span class="sxs-lookup"><span data-stu-id="eb472-116">Gets an estimate of the percentage of the current update that has been downloaded.</span></span>                                                               |
| [<span data-ttu-id="eb472-117">**PercentComplete**</span><span class="sxs-lookup"><span data-stu-id="eb472-117">**PercentComplete**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_percentcomplete)                           | <span data-ttu-id="eb472-118">Obtiene una estimación del porcentaje de todas las actualizaciones que se han descargado.</span><span class="sxs-lookup"><span data-stu-id="eb472-118">Gets an estimate of the percentage of all the updates that have been downloaded.</span></span>                                                                 |
| [<span data-ttu-id="eb472-119">**TotalBytesDownloaded**</span><span class="sxs-lookup"><span data-stu-id="eb472-119">**TotalBytesDownloaded**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytesdownloaded)                 | <span data-ttu-id="eb472-120">Obtiene una cadena que especifica la cantidad total de datos que se han descargado, en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb472-120">Gets a string that specifies the total amount of data that has been downloaded, in bytes.</span></span>                                                        |
| [<span data-ttu-id="eb472-121">**TotalBytesToDownload**</span><span class="sxs-lookup"><span data-stu-id="eb472-121">**TotalBytesToDownload**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-idownloadprogress-get_totalbytestodownload)                 | <span data-ttu-id="eb472-122">Obtiene una cadena que representa la estimación de la cantidad total de datos que se van a descargar, en bytes.</span><span class="sxs-lookup"><span data-stu-id="eb472-122">Gets a string that represents the estimate of the total amount of data that will be downloaded, in bytes.</span></span>                                        |



 

 

 



