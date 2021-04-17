---
description: Más información acerca de cómo transferir datos
ms.assetid: 34871ff4-7eb0-451b-a62b-85b632af9a47
title: Transferir datos
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05d94e9e09aad121720ca491864a23f3d2d38b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696511"
---
# <a name="transferring-data"></a><span data-ttu-id="719c2-103">Transferir datos</span><span class="sxs-lookup"><span data-stu-id="719c2-103">Transferring Data</span></span>

> [!Note]  
> <span data-ttu-id="719c2-104">Este sistema de scripting se ha reemplazado por el nivel de automatización de adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="719c2-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="719c2-105">Consulte [nivel de automatización de adquisición de imágenes de Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span><span class="sxs-lookup"><span data-stu-id="719c2-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="719c2-106">Use el método [**Transfer**](-wia-iwiadispatchitem-transfer.md) de un objeto [**Item**](-wia-item.md) para transferir datos de imagen o de audio desde un dispositivo a un archivo o al portapapeles.</span><span class="sxs-lookup"><span data-stu-id="719c2-106">Use the [**Transfer**](-wia-iwiadispatchitem-transfer.md) method of an [**Item**](-wia-item.md) object to transfer image or audio data from a device to a file or the clipboard.</span></span>

<span data-ttu-id="719c2-107">Pase una ruta de acceso y un nombre de archivo como primer parámetro para guardar los datos en el disco, o bien pase la cadena "Clipboard" para transferir el elemento al portapapeles.</span><span class="sxs-lookup"><span data-stu-id="719c2-107">Pass a path and filename as the first parameter to save the data to disk, or pass the string "clipboard" to transfer the item to the clipboard.</span></span>

 

 
