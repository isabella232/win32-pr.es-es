---
description: Al igual que una región de recorte, una ruta de acceso de clip es otro objeto de gráficos que una aplicación puede seleccionar en un contexto de dispositivo.
ms.assetid: 35c4052b-3f11-40bc-9cc9-6f999326a656
title: Trazados de clip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dc4a93b0047110a6adb2f68d413e89cb1e97fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985046"
---
# <a name="clip-paths"></a><span data-ttu-id="c5dd1-103">Trazados de clip</span><span class="sxs-lookup"><span data-stu-id="c5dd1-103">Clip Paths</span></span>

<span data-ttu-id="c5dd1-104">Al igual que una región de recorte, una ruta de acceso de clip es otro objeto de gráficos que una aplicación puede seleccionar en un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-104">Like a clipping region, a clip path is another graphics object that an application can select into a device context.</span></span> <span data-ttu-id="c5dd1-105">A diferencia de una región de recorte, una ruta de acceso de clip siempre la crea una aplicación y se usa para recortar a una o varias formas irregulares.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-105">Unlike a clipping region, a clip path is always created by an application and it is used for clipping to one or more irregular shapes.</span></span> <span data-ttu-id="c5dd1-106">Por ejemplo, una aplicación puede utilizar las líneas y curvas que forman los contornos de los caracteres de una cadena de texto para definir una ruta de acceso de recorte.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-106">For example, an application can use the lines and curves that form the outlines of characters in a string of text to define a clip path.</span></span>

<span data-ttu-id="c5dd1-107">Para crear una ruta de acceso de clip, primero es necesario crear una ruta de acceso que describa la forma irregular necesaria.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-107">To create a clip path, it's first necessary to create a path that describes the required irregular shape.</span></span> <span data-ttu-id="c5dd1-108">Las rutas de acceso se crean mediante una llamada a las funciones de dibujo de la interfaz de dispositivo gráfico (GDI) adecuadas después de llamar a la función [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) y antes de llamar a la función [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) .</span><span class="sxs-lookup"><span data-stu-id="c5dd1-108">Paths are created by calling the appropriate graphics device interface (GDI) drawing functions after calling the [**BeginPath**](/windows/desktop/api/Wingdi/nf-wingdi-beginpath) function and before calling the [**EndPath**](/windows/desktop/api/Wingdi/nf-wingdi-endpath) function.</span></span> <span data-ttu-id="c5dd1-109">Esta colección de funciones se denomina corchete de ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-109">This collection of functions is called a path bracket.</span></span> <span data-ttu-id="c5dd1-110">Para obtener más información sobre las rutas de acceso y los corchetes de ruta, vea [rutas](paths.md).</span><span class="sxs-lookup"><span data-stu-id="c5dd1-110">For more information about paths and path brackets, see [Paths](paths.md).</span></span>

<span data-ttu-id="c5dd1-111">Una vez creada la ruta de acceso, se puede convertir en una ruta de acceso de clip llamando a la función [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) , identificando un contexto de dispositivo y especificando un modo de uso.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-111">After the path is created, it can be converted to a clip path by calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function, identifying a device context, and specifying a usage mode.</span></span> <span data-ttu-id="c5dd1-112">El modo de uso determina la forma en que el sistema combina la nueva ruta de acceso del clip con la región de recorte original del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-112">The usage mode determines how the system combines the new clip path with the device context's original clipping region.</span></span> <span data-ttu-id="c5dd1-113">En la tabla siguiente se describen los modos de uso.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-113">The following table describes the usage modes.</span></span>



| <span data-ttu-id="c5dd1-114">Mode</span><span class="sxs-lookup"><span data-stu-id="c5dd1-114">Mode</span></span>      | <span data-ttu-id="c5dd1-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="c5dd1-115">Description</span></span>                                                                                                                  |
|-----------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5dd1-116">RGN \_ y</span><span class="sxs-lookup"><span data-stu-id="c5dd1-116">RGN\_AND</span></span>  | <span data-ttu-id="c5dd1-117">La ruta de acceso del clip incluye la intersección (áreas superpuestas) de la región de recorte del contexto del dispositivo y la ruta de acceso actual.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-117">The clip path includes the intersection (overlapping areas) of the device context's clipping region and the current path.</span></span>    |
| <span data-ttu-id="c5dd1-118">copia de RGN \_</span><span class="sxs-lookup"><span data-stu-id="c5dd1-118">RGN\_COPY</span></span> | <span data-ttu-id="c5dd1-119">La ruta de acceso del clip es la ruta de acceso actual.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-119">The clip path is the current path.</span></span>                                                                                           |
| <span data-ttu-id="c5dd1-120">RGN ( \_ diferencia)</span><span class="sxs-lookup"><span data-stu-id="c5dd1-120">RGN\_DIFF</span></span> | <span data-ttu-id="c5dd1-121">La ruta de acceso del clip incluye la región de recorte del contexto del dispositivo con las partes que interseccionan de la ruta de acceso actual excluida.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-121">The clip path includes the device context's clipping region with any intersecting parts of the current path excluded.</span></span>        |
| <span data-ttu-id="c5dd1-122">RGN \_ o</span><span class="sxs-lookup"><span data-stu-id="c5dd1-122">RGN\_OR</span></span>   | <span data-ttu-id="c5dd1-123">La ruta de acceso del clip incluye la Unión (áreas combinadas) de la región de recorte del contexto del dispositivo y la ruta de acceso actual.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-123">The clip path includes the union (combined areas) of the device context's clipping region and the current path.</span></span>              |
| <span data-ttu-id="c5dd1-124">RGN \_ XOR</span><span class="sxs-lookup"><span data-stu-id="c5dd1-124">RGN\_XOR</span></span>  | <span data-ttu-id="c5dd1-125">La ruta de acceso del clip incluye la Unión de la región de recorte del contexto del dispositivo y la ruta de acceso actual, pero excluye la intersección.</span><span class="sxs-lookup"><span data-stu-id="c5dd1-125">The clip path includes the union of the device context's clipping region and the current path but excludes the intersection.</span></span> |



 

 

 



