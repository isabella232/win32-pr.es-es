---
description: Puede especificar que el controlador recorte los fotogramas.
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: Recorte de un fotograma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667121"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="77528-103">Recorte de un fotograma</span><span class="sxs-lookup"><span data-stu-id="77528-103">Clipping a Frame</span></span>

<span data-ttu-id="77528-104">Puede especificar que el controlador recorte los fotogramas.</span><span class="sxs-lookup"><span data-stu-id="77528-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="77528-105">(Si se omiten las demás secciones del filtro de captura, esta puede ser la única función del filtro de captura).</span><span class="sxs-lookup"><span data-stu-id="77528-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="77528-106">Si el campo **nFrameBytesToCopy** no es cero (0), su valor especifica el número de bytes de cada fotograma recibidos para conservar.</span><span class="sxs-lookup"><span data-stu-id="77528-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="77528-107">Si el campo es cero, se conserva todo el marco.</span><span class="sxs-lookup"><span data-stu-id="77528-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="77528-108">Puede recortar cualquier fotograma que pase las demás partes del filtro de captura estableciendo **nFrameBytesToCopy**.</span><span class="sxs-lookup"><span data-stu-id="77528-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



