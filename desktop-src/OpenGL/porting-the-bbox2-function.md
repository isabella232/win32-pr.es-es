---
title: Trasladar la función bbox2
description: No hay ningún equivalente de OpenGL para la función bbox2 de la contabilidad de IRIS.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Migración de la contabilidad de IRIS, función bbox2
- portabilidad de IRIS GL, función bbox2
- portabilidad a OpenGL desde IRIS GL, función bbox2
- Exportación de OpenGL desde IRIS GL, función bbox2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778036"
---
# <a name="porting-the-bbox2-function"></a><span data-ttu-id="d89f7-107">Trasladar la función bbox2</span><span class="sxs-lookup"><span data-stu-id="d89f7-107">Porting the bbox2 Function</span></span>

<span data-ttu-id="d89f7-108">No hay ningún equivalente de OpenGL para la función **bbox2** de la contabilidad de iris.</span><span class="sxs-lookup"><span data-stu-id="d89f7-108">There is no OpenGL equivalent for the IRIS GL **bbox2** function.</span></span>

<span data-ttu-id="d89f7-109">**Para portar código que contiene funciones bbox2**</span><span class="sxs-lookup"><span data-stu-id="d89f7-109">**To port code that contains bbox2 functions**</span></span>

1.  <span data-ttu-id="d89f7-110">Cree una nueva lista de visualización (OpenGL) que contenga todo lo que se encuentra en la lista de visualización de la contabilidad de IRIS equivalente, excepto la llamada a **bbox2**.</span><span class="sxs-lookup"><span data-stu-id="d89f7-110">Create a new (OpenGL) display list that contains everything in the equivalent IRIS GL display list except the call to **bbox2**.</span></span>
2.  <span data-ttu-id="d89f7-111">Use el código de Windows adecuado para dibujar un rectángulo del mismo tamaño que el **BBox** de GL de iris.</span><span class="sxs-lookup"><span data-stu-id="d89f7-111">Use appropriate Windows code to draw a rectangle the same size as the IRIS GL **bbox**.</span></span>

 

 




