---
title: Escribir en un archivo
description: Escribir en un archivo
ms.assetid: a01f93e9-e0fe-4e81-aa9f-62cdca7bce4a
keywords:
- AVIFileWriteData función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9a6b9a399d8581909c99da615e32ef4487cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105676205"
---
# <a name="writing-to-a-file"></a><span data-ttu-id="1321c-104">Escribir en un archivo</span><span class="sxs-lookup"><span data-stu-id="1321c-104">Writing to a File</span></span>

<span data-ttu-id="1321c-105">Puede escribir información complementaria en un archivo que se ha abierto con privilegios de escritura mediante la función [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) .</span><span class="sxs-lookup"><span data-stu-id="1321c-105">You can write supplementary information to a file that has been opened with write privileges by using the [**AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) function.</span></span> <span data-ttu-id="1321c-106">Esta función copia la información de un búfer proporcionado por la aplicación y la coloca en uno o varios fragmentos del archivo.</span><span class="sxs-lookup"><span data-stu-id="1321c-106">This function copies the information from an application-supplied buffer and places it in one or more chunks in the file.</span></span> <span data-ttu-id="1321c-107">El fragmento "INFO" es un tipo de fragmento RIFF común en el que la función almacena información complementaria.</span><span class="sxs-lookup"><span data-stu-id="1321c-107">The "INFO" chunk is a common RIFF chunk type in which the function stores supplementary information.</span></span> <span data-ttu-id="1321c-108">Para obtener una descripción de los archivos RIFF y sus fragmentos de datos, consulte [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span><span class="sxs-lookup"><span data-stu-id="1321c-108">For a description of RIFF files and their data chunks, see [Resource Interchange File Format Services](resource-interchange-file-format-services.md).</span></span>

 

 




