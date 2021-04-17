---
description: Una aplicación puede truncar o extender un archivo mediante una llamada a SetEndOfFile.
ms.assetid: 23a0242d-50e9-4324-bb09-505afe383a80
title: Truncar o extender archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: daf8a2d4e7e346bfea41285be97d6d756e2a6b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688284"
---
# <a name="truncating-or-extending-files"></a><span data-ttu-id="8dc6b-103">Truncar o extender archivos</span><span class="sxs-lookup"><span data-stu-id="8dc6b-103">Truncating or Extending Files</span></span>

<span data-ttu-id="8dc6b-104">Una aplicación puede truncar o extender un archivo mediante una llamada a [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span><span class="sxs-lookup"><span data-stu-id="8dc6b-104">An application can truncate or extend a file by calling [**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile).</span></span> <span data-ttu-id="8dc6b-105">Esta función establece el marcador de fin de archivo en la posición actual del puntero de archivo.</span><span class="sxs-lookup"><span data-stu-id="8dc6b-105">This function sets the end-of-file marker to the current position of the file pointer.</span></span>

<span data-ttu-id="8dc6b-106">Tenga en cuenta que cuando se extiende un archivo, no se define el contenido entre las ubicaciones de fin de archivo antiguas y nuevas.</span><span class="sxs-lookup"><span data-stu-id="8dc6b-106">Note that when a file is extended, the contents between the old and new end-of-file locations are not defined.</span></span>

 

 



