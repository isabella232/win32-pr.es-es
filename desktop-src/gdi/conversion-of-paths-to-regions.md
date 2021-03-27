---
description: Una aplicación puede convertir un trazado en una región llamando a la función PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversión de rutas de acceso a regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812007"
---
# <a name="conversion-of-paths-to-regions"></a><span data-ttu-id="d0094-103">Conversión de rutas de acceso a regiones</span><span class="sxs-lookup"><span data-stu-id="d0094-103">Conversion of Paths to Regions</span></span>

<span data-ttu-id="d0094-104">Una aplicación puede convertir un trazado en una región llamando a la función [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) .</span><span class="sxs-lookup"><span data-stu-id="d0094-104">An application can convert a path into a region by calling the [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) function.</span></span> <span data-ttu-id="d0094-105">Al igual que [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** es útil en la creación de efectos gráficos especiales.</span><span class="sxs-lookup"><span data-stu-id="d0094-105">Like [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** is useful in the creation of special graphics effects.</span></span> <span data-ttu-id="d0094-106">Por ejemplo, no hay ninguna función que permita a una aplicación desplazar una ruta de acceso; sin embargo, hay una función que permite a una aplicación desplazar una región ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span><span class="sxs-lookup"><span data-stu-id="d0094-106">For example, there are no functions that allow an application to offset a path; however, there is a function that enables an application to offset a region ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)).</span></span> <span data-ttu-id="d0094-107">Con **PathToRegion** , una aplicación puede crear el efecto de animar una forma compleja creando una ruta de acceso que defina la forma, convirtiendo la ruta de acceso en una región (llamando a **PathToRegion**) y, a continuación, dibujando, moviendo y borrando la región repetidamente (llamando a funciones en una secuencia, como [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** y **FillRgn**).</span><span class="sxs-lookup"><span data-stu-id="d0094-107">Using **PathToRegion** , an application can create the effect of animating a complex shape by creating a path that defines the shape, converting the path into a region (by calling **PathToRegion**), and then repeatedly painting, moving, and erasing the region (by calling functions in a sequence, such as [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** , and **FillRgn**).</span></span>

 

 



