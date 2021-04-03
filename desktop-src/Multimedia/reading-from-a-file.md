---
title: Leer de un archivo
description: Leer de un archivo
ms.assetid: 7c728304-7d05-4e28-a9bd-83b5b1af39be
keywords:
- AVIFileInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba1ffe866e454a898c5c3b91c7721c24f6a861ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076139"
---
# <a name="reading-from-a-file"></a><span data-ttu-id="e5a92-104">Leer de un archivo</span><span class="sxs-lookup"><span data-stu-id="e5a92-104">Reading from a File</span></span>

<span data-ttu-id="e5a92-105">Puede recuperar información sobre un archivo abierto mediante la función [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) .</span><span class="sxs-lookup"><span data-stu-id="e5a92-105">You can retrieve information about an open file by using the [**AVIFileInfo**](/windows/desktop/api/Vfw/nf-vfw-avifileinfo) function.</span></span> <span data-ttu-id="e5a92-106">Esta función rellena la estructura [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) con información como la velocidad de datos máxima, el número de flujos del archivo, si el archivo usa un índice y si el archivo está protegido por derechos de autor.</span><span class="sxs-lookup"><span data-stu-id="e5a92-106">This function fills the [**AVIFILEINFO**](/windows/desktop/api/Vfw/ns-vfw-avifileinfoa) structure with such information as the maximum data rate, the number of streams in the file, whether the file uses an index, and whether the file is copyrighted.</span></span>

<span data-ttu-id="e5a92-107">Para recuperar información complementaria en un archivo AVI, utilice la función [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) .</span><span class="sxs-lookup"><span data-stu-id="e5a92-107">To retrieve supplementary information in an AVI file, use the [**AVIFileReadData**](/windows/desktop/api/Vfw/nf-vfw-avifilereaddata) function.</span></span> <span data-ttu-id="e5a92-108">La información complementaria es aplicable a todo el archivo y no se incluye en los encabezados de archivo normales.</span><span class="sxs-lookup"><span data-stu-id="e5a92-108">Supplementary information is applicable to the entire file and is not included in the normal file headers.</span></span> <span data-ttu-id="e5a92-109">Por ejemplo, el nombre de la empresa o la persona que contiene los derechos de autor de un archivo puede ser información complementaria.</span><span class="sxs-lookup"><span data-stu-id="e5a92-109">For example, the name of the company or person who holds the copyrights of a file could be supplementary information.</span></span> <span data-ttu-id="e5a92-110">La información complementaria no se adhiere a un formato específico; puede ser específico del archivo.</span><span class="sxs-lookup"><span data-stu-id="e5a92-110">Supplementary information does not adhere to a specific format; it can be file specific.</span></span> <span data-ttu-id="e5a92-111">**AVIFileReadData** devuelve la información complementaria en un búfer proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e5a92-111">**AVIFileReadData** returns the supplementary information in an application-supplied buffer.</span></span>

 

 




