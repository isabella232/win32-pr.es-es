---
description: Un objeto GraphicsPath almacena una secuencia de líneas y B&\# 233; curvas spline de Bézier.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Alisar trazados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987675"
---
# <a name="flattening-paths"></a><span data-ttu-id="3cff0-103">Alisar trazados</span><span class="sxs-lookup"><span data-stu-id="3cff0-103">Flattening Paths</span></span>

<span data-ttu-id="3cff0-104">Un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) almacena una secuencia de líneas y curvas spline de Bézier.</span><span class="sxs-lookup"><span data-stu-id="3cff0-104">A [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object stores a sequence of lines and Bézier splines.</span></span> <span data-ttu-id="3cff0-105">Puede agregar varios tipos de curvas (elipses, arcos, curvas spline cardinales) a un trazado, pero cada curva se convierte en una curva spline de Bézier antes de almacenarla en la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="3cff0-105">You can add several types of curves (ellipses, arcs, cardinal splines) to a path, but each curve is converted to a Bézier spline before it is stored in the path.</span></span> <span data-ttu-id="3cff0-106">El acoplamiento de un trazado consiste en convertir cada curva spline de Bézier del trazado en una secuencia de líneas rectas.</span><span class="sxs-lookup"><span data-stu-id="3cff0-106">Flattening a path consists of converting each Bézier spline in the path to a sequence of straight lines.</span></span>

<span data-ttu-id="3cff0-107">Para aplanar una ruta de acceso, llame al método [**GraphicsPath:: Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) de un objeto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="3cff0-107">To flatten a path, call the [**GraphicsPath::Flatten**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) method of a [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="3cff0-108">El método **GraphicsPath:: Flatten** recibe un argumento de flatity que especifica la distancia máxima entre el trazado plano y el trazado original.</span><span class="sxs-lookup"><span data-stu-id="3cff0-108">The **GraphicsPath::Flatten** method receives a flatness argument that specifies the maximum distance between the flattened path and the original path.</span></span> <span data-ttu-id="3cff0-109">En la ilustración siguiente se muestra una ruta de acceso antes y después del acoplamiento.</span><span class="sxs-lookup"><span data-stu-id="3cff0-109">The following illustration shows a path before and after flattening.</span></span>

![Ilustración donde se muestra una secuencia de curvas spline de Bézier conectadas en azul y las líneas correspondientes en rojo](images/aboutgdip02-art32a.png)

 

 



