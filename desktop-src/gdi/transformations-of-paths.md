---
description: Las rutas de acceso se definen mediante unidades lógicas y transformaciones actuales.
ms.assetid: a5a426ec-25e8-4fe1-985c-d078227e8aba
title: Transformaciones de rutas de acceso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb2c033b5769a4edff29beba6cccbd80cfd26de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985807"
---
# <a name="transformations-of-paths"></a><span data-ttu-id="a4939-103">Transformaciones de rutas de acceso</span><span class="sxs-lookup"><span data-stu-id="a4939-103">Transformations of Paths</span></span>

<span data-ttu-id="a4939-104">Las rutas de acceso se definen mediante unidades lógicas y transformaciones actuales.</span><span class="sxs-lookup"><span data-stu-id="a4939-104">Paths are defined using logical units and current transformations.</span></span> <span data-ttu-id="a4939-105">(Si se ha llamado a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) , las unidades lógicas son unidades universales; de lo contrario, las unidades lógicas son unidades de página). Una aplicación puede usar transformaciones universales para escalar, girar, distorsionar, trasladar y reflejar las líneas y las curvas de Bézier que definen un trazado.</span><span class="sxs-lookup"><span data-stu-id="a4939-105">(If the [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) function has been called, the logical units are world units; otherwise, the logical units are page units.) An application can use world transformations to scale, rotate, shear, translate, and reflect the lines and Bézier curves that define a path.</span></span>

> [!Note]  
> <span data-ttu-id="a4939-106">Una transformación universal dentro de un corchete de ruta de acceso solo afecta a las líneas y curvas dibujadas después de que se haya establecido la transformación.</span><span class="sxs-lookup"><span data-stu-id="a4939-106">A world transformation within a path bracket only affects those lines and curves drawn after the transformation was set.</span></span> <span data-ttu-id="a4939-107">No tendrá ningún efecto en las líneas y curvas dibujadas antes de establecerse.</span><span class="sxs-lookup"><span data-stu-id="a4939-107">It will have no affect on those lines and curves that were drawn before it was set.</span></span> <span data-ttu-id="a4939-108">Para obtener una descripción de la transformación universal, vea [espacios de coordenadas y transformaciones](coordinate-spaces-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="a4939-108">For a description of the world transformation, see [Coordinate Spaces and Transformations](coordinate-spaces-and-transformations.md).</span></span>

 

<span data-ttu-id="a4939-109">Una aplicación también puede usar [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) para describir la forma del lápiz que se usa para esquematizar un trazado si el lápiz es una pluma geométrica.</span><span class="sxs-lookup"><span data-stu-id="a4939-109">An application can also use [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) to outline the shape of the pen used to outline a path if the pen is a geometric pen.</span></span> <span data-ttu-id="a4939-110">Para obtener una descripción de los lápices geométricos, consulte [lápices](pens.md).</span><span class="sxs-lookup"><span data-stu-id="a4939-110">For a description of geometric pens, see [Pens](pens.md).</span></span>

 

 



