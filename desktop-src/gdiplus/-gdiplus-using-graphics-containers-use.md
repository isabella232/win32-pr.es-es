---
description: Un objeto Graphics proporciona métodos como DrawLine, DrawImage y DrawString para mostrar imágenes vectoriales, imágenes de trama y texto.
ms.assetid: 721d0c1c-d105-4d9f-b5e9-6ca407b28c4e
title: Utilizar contenedores de gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80570f3a45c8d67b36f677fc404dcd63581e7938
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985114"
---
# <a name="using-graphics-containers"></a><span data-ttu-id="9b54d-103">Utilizar contenedores de gráficos</span><span class="sxs-lookup"><span data-stu-id="9b54d-103">Using Graphics Containers</span></span>

<span data-ttu-id="9b54d-104">Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) proporciona métodos como [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint))y [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) para mostrar imágenes vectoriales, imágenes de trama y texto.</span><span class="sxs-lookup"><span data-stu-id="9b54d-104">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object provides methods such as [DrawLine](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawline(inconstpen_inint_inint_inint_inint)), [DrawImage](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawimage(inimage_inconstpointf_inint)), and [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) for displaying vector images, raster images, and text.</span></span> <span data-ttu-id="9b54d-105">Un objeto **Graphics** también tiene varias propiedades que influyen en la calidad y la orientación de los elementos que se dibujan.</span><span class="sxs-lookup"><span data-stu-id="9b54d-105">A **Graphics** object also has several properties that influence the quality and orientation of the items that are drawn.</span></span> <span data-ttu-id="9b54d-106">Por ejemplo, la propiedad modo de suavizado determina si se aplica el suavizado de contorno a las líneas y las curvas, y la propiedad de transformación universal influye en la posición y la rotación de los elementos que se dibujan.</span><span class="sxs-lookup"><span data-stu-id="9b54d-106">For example, the smoothing mode property determines whether antialiasing is applied to lines and curves, and the world transformation property influences the position and rotation of the items that are drawn.</span></span>

<span data-ttu-id="9b54d-107">Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) suele estar asociado a un dispositivo de presentación determinado.</span><span class="sxs-lookup"><span data-stu-id="9b54d-107">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object is often associated with a particular display device.</span></span> <span data-ttu-id="9b54d-108">Cuando se usa un objeto **Graphics** para dibujar en una ventana, el objeto **Graphics** también está asociado a esa ventana concreta.</span><span class="sxs-lookup"><span data-stu-id="9b54d-108">When you use a **Graphics** object to draw in a window, the **Graphics** object is also associated with that particular window.</span></span>

<span data-ttu-id="9b54d-109">Un objeto [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) puede considerarse como un contenedor porque contiene un conjunto de propiedades que influyen en el dibujo y se vincula a información específica del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9b54d-109">A [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object can be thought of as a container because it holds a set of properties that influence drawing, and it is linked to device-specific information.</span></span> <span data-ttu-id="9b54d-110">Puede crear un contenedor secundario dentro de un objeto **Graphics** existente llamando al método [BeginContainer](/previous-versions//ms535731(v=vs.85)) de ese objeto **Graphics** .</span><span class="sxs-lookup"><span data-stu-id="9b54d-110">You can create a secondary container within an existing **Graphics** object by calling the [BeginContainer](/previous-versions//ms535731(v=vs.85)) method of that **Graphics** object.</span></span>

<span data-ttu-id="9b54d-111">En los temas siguientes se tratan los objetos [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) y los contenedores anidados con más detalle:</span><span class="sxs-lookup"><span data-stu-id="9b54d-111">The following topics cover [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) objects and nested containers in more detail:</span></span>

-   [<span data-ttu-id="9b54d-112">Estado de un objeto de gráficos</span><span class="sxs-lookup"><span data-stu-id="9b54d-112">The State of a Graphics Object</span></span>](-gdiplus-the-state-of-a-graphics-object-use.md)
-   [<span data-ttu-id="9b54d-113">Contenedores de gráficos anidados</span><span class="sxs-lookup"><span data-stu-id="9b54d-113">Nested Graphics Containers</span></span>](-gdiplus-nested-graphics-containers-use.md)

 

 
