---
description: Los registros de polilínea son una serie de puntos; las líneas dibujadas entre los puntos describen el contorno del carácter.
ms.assetid: 6f0de0bb-ad23-471f-9771-8f28614ee28d
title: Registros de polilínea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20e9a9e87a730d06d15eae219f6f626f1d6d3848
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275984"
---
# <a name="polyline-records"></a><span data-ttu-id="c0bb0-103">Registros de polilínea</span><span class="sxs-lookup"><span data-stu-id="c0bb0-103">Polyline Records</span></span>

<span data-ttu-id="c0bb0-104">Los registros de [polilínea](/windows/desktop/api/Wingdi/nf-wingdi-polyline) son una serie de puntos; las líneas dibujadas entre los puntos describen el contorno del carácter.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-104">[Polyline](/windows/desktop/api/Wingdi/nf-wingdi-polyline) records are a series of points; lines drawn between the points describe the outline of the character.</span></span> <span data-ttu-id="c0bb0-105">Un registro de polilínea comienza con el último punto del registro anterior (o, para el primer registro del contorno, el punto inicial).</span><span class="sxs-lookup"><span data-stu-id="c0bb0-105">A polyline record begins with the last point in the previous record (or, for the first record in the contour, the starting point).</span></span> <span data-ttu-id="c0bb0-106">Cada punto del registro se encuentra en el contorno del glifo y se puede conectar simplemente mediante líneas rectas.</span><span class="sxs-lookup"><span data-stu-id="c0bb0-106">Each point in the record is on the glyph outline and can be connected simply by using straight lines.</span></span>

 

 



