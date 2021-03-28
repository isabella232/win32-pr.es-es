---
description: Una aplicación puede utilizar el recorte y las rutas de acceso para crear efectos gráficos especiales. En la ilustración siguiente se muestra una cadena de texto dibujada con una fuente Arial grande.
ms.assetid: fda0d627-406c-44f9-9061-7aea3e2d7f66
title: Trazados de clips y efectos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8156a8670747175502b2385e6c24a340345a54f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544547"
---
# <a name="clip-paths-and-graphic-effects"></a><span data-ttu-id="61b0c-104">Trazados de clips y efectos gráficos</span><span class="sxs-lookup"><span data-stu-id="61b0c-104">Clip Paths and Graphic Effects</span></span>

<span data-ttu-id="61b0c-105">Una aplicación puede utilizar el recorte y las rutas de acceso para crear efectos gráficos especiales.</span><span class="sxs-lookup"><span data-stu-id="61b0c-105">An application can use clipping and paths to create special graphic effects.</span></span> <span data-ttu-id="61b0c-106">En la ilustración siguiente se muestra una cadena de texto dibujada con una fuente Arial grande.</span><span class="sxs-lookup"><span data-stu-id="61b0c-106">The following illustration shows a string of text drawn with a large Arial font.</span></span>

![Ilustración en la que se muestra el texto negro sobre un fondo blanco](images/cspth-02.png)

<span data-ttu-id="61b0c-108">En la ilustración siguiente se muestra el resultado de seleccionar el texto como una ruta de recorte y dibujar líneas radiales para un círculo cuyo centro se encuentra encima y a la izquierda de la cadena.</span><span class="sxs-lookup"><span data-stu-id="61b0c-108">The next illustration shows the result of selecting the text as a clip path and drawing radial lines for a circle whose center is located above and left of the string.</span></span>

![Ilustración que muestra el mismo texto, pero rellenado con líneas en lugar de negro sólido](images/cspth-03.png)

> [!Note]  
> <span data-ttu-id="61b0c-110">Antes de que la interfaz de dispositivo gráfico (GDI) agregue texto creado con una fuente de mapa de imágenes a un trazado, convierte la fuente en una fuente de esquema o de vector.</span><span class="sxs-lookup"><span data-stu-id="61b0c-110">Before graphics device interface (GDI) adds text created with a bitmapped font to a path, it converts the font to an outline or vector font.</span></span>

 

<span data-ttu-id="61b0c-111">Una aplicación crea una ruta de acceso de clip generando un corchete de ruta de acceso y llamando a la función [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) .</span><span class="sxs-lookup"><span data-stu-id="61b0c-111">An application creates a clip path by generating a path bracket and then calling the [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) function.</span></span> <span data-ttu-id="61b0c-112">Después de seleccionar una ruta de acceso de recorte en un controlador de dominio, la salida solo aparece dentro de los bordes de la ruta de acceso.</span><span class="sxs-lookup"><span data-stu-id="61b0c-112">After a clip path is selected into a DC, output only appears within the borders of the path.</span></span>

<span data-ttu-id="61b0c-113">Además de crear efectos de gráficos especiales, las rutas de acceso de clip también son útiles en aplicaciones que guardan imágenes como metaarchivos mejorados.</span><span class="sxs-lookup"><span data-stu-id="61b0c-113">In addition to creating special graphics effects, clip paths are also useful in applications that save images as enhanced metafiles.</span></span> <span data-ttu-id="61b0c-114">Mediante el uso de una ruta de acceso de clip, una aplicación puede garantizar la independencia del dispositivo porque las unidades utilizadas para especificar una ruta de acceso son unidades lógicas.</span><span class="sxs-lookup"><span data-stu-id="61b0c-114">By using a clip path, an application is able to ensure device independence because the units used to specify a path are logical units.</span></span>

 

 



