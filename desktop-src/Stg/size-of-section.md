---
title: Tamaño de la sección
description: El tipo de datos de tamaño de la sección indica el tamaño, en bytes, de la sección.
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269344"
---
# <a name="size-of-section"></a><span data-ttu-id="2634b-103">Tamaño de la sección</span><span class="sxs-lookup"><span data-stu-id="2634b-103">Size of Section</span></span>

<span data-ttu-id="2634b-104">El tipo de datos de tamaño de la sección indica el tamaño, en bytes, de la sección.</span><span class="sxs-lookup"><span data-stu-id="2634b-104">The section size data type indicates the size, in bytes, of the section.</span></span> <span data-ttu-id="2634b-105">Dado que el tamaño de la sección es los cuatro primeros bytes, las secciones se pueden copiar como una matriz de bytes.</span><span class="sxs-lookup"><span data-stu-id="2634b-105">Because the section size is the first 4 bytes, sections can be copied as an array of bytes.</span></span> <span data-ttu-id="2634b-106">El tamaño de la sección siempre debe ser un múltiplo de cuatro.</span><span class="sxs-lookup"><span data-stu-id="2634b-106">The section size should always be a multiple of four.</span></span>

<span data-ttu-id="2634b-107">Por ejemplo, una sección vacía, es decir, una con cero propiedades en ella, tendría un recuento de bytes de ocho (el recuento de bytes **DWORD** y el número **DWORD** de propiedades).</span><span class="sxs-lookup"><span data-stu-id="2634b-107">For example, an empty section, that is, one with zero properties in it, would have a byte count of eight (the **DWORD** byte count and the **DWORD** count of properties).</span></span> <span data-ttu-id="2634b-108">La sección contiene los 8 bytes: **08 00 00 00 00 00 00 00**.</span><span class="sxs-lookup"><span data-stu-id="2634b-108">The section itself would contain the 8 bytes: **08 00 00 00 00 00 00 00**.</span></span>

 

 




