---
title: Funciones de formato de píxeles
description: Las siguientes funciones de Windows administran formatos de píxeles.
ms.assetid: 78a6be75-72f6-4aef-a6bc-5f052c6fe2e9
keywords:
- Funciones de WGL, formato de píxel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e219fc6a2aafecdcda43708cdb4c77553c88f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903844"
---
# <a name="pixel-format-functions"></a><span data-ttu-id="6516a-104">Funciones de formato de píxeles</span><span class="sxs-lookup"><span data-stu-id="6516a-104">Pixel Format Functions</span></span>

<span data-ttu-id="6516a-105">Las siguientes funciones de Windows administran formatos de píxeles.</span><span class="sxs-lookup"><span data-stu-id="6516a-105">The following Windows functions manage pixel formats.</span></span>



| <span data-ttu-id="6516a-106">Función de Windows</span><span class="sxs-lookup"><span data-stu-id="6516a-106">Windows Function</span></span>                                               | <span data-ttu-id="6516a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6516a-107">Description</span></span>                                                                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6516a-108">**ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="6516a-108">**ChoosePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat)                 | <span data-ttu-id="6516a-109">Obtiene el formato de píxel del contexto del dispositivo, que es la coincidencia más cercana a un formato de píxel especificado.</span><span class="sxs-lookup"><span data-stu-id="6516a-109">Obtains the device context's pixel format that is the closest match to a specified pixel format.</span></span>                                                                      |
| [<span data-ttu-id="6516a-110">**SetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="6516a-110">**SetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat)                       | <span data-ttu-id="6516a-111">Establece el formato de píxel actual del contexto del dispositivo en el formato de píxel especificado por un índice de formato de píxel.</span><span class="sxs-lookup"><span data-stu-id="6516a-111">Sets a device context's current pixel format to the pixel format specified by a pixel format index.</span></span>                                                                   |
| [<span data-ttu-id="6516a-112">**GetPixelFormat**</span><span class="sxs-lookup"><span data-stu-id="6516a-112">**GetPixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat)                       | <span data-ttu-id="6516a-113">Obtiene el índice de formato de píxel del formato de píxel actual de un contexto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6516a-113">Obtains the pixel format index of a device context's current pixel format.</span></span>                                                                                            |
| [<span data-ttu-id="6516a-114">**DescribePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="6516a-114">**DescribePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat)             | <span data-ttu-id="6516a-115">Dado un contexto de dispositivo y un índice de formato de píxel, rellena una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) con las propiedades del formato de píxel.</span><span class="sxs-lookup"><span data-stu-id="6516a-115">Given a device context and a pixel format index, fills in a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure with the pixel format's properties.</span></span> |
| [<span data-ttu-id="6516a-116">**GetEnhMetaFilePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="6516a-116">**GetEnhMetaFilePixelFormat**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-getenhmetafilepixelformat) | <span data-ttu-id="6516a-117">Recupera información de formato de píxel para un metarchivo mejorado.</span><span class="sxs-lookup"><span data-stu-id="6516a-117">Retrieves pixel format information for an enhanced metafile.</span></span>                                                                                                          |



 

<span data-ttu-id="6516a-118">La función [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) devuelve un índice de formato de píxel basado en uno que identifica la mejor coincidencia de los formatos de píxel admitidos del contexto del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6516a-118">The [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function returns a one-based pixel format index that identifies the best match from the device context's supported pixel formats.</span></span>

<span data-ttu-id="6516a-119">La función [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) identifica el formato deseado mediante un índice de formato de píxel basado en uno.</span><span class="sxs-lookup"><span data-stu-id="6516a-119">The [**SetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-setpixelformat) function identifies the desired format using a one-based pixel format index.</span></span> <span data-ttu-id="6516a-120">Normalmente, se llama a **ChoosePixelFormat** para buscar un formato de píxel de mejor coincidencia y, a continuación, se llama a **SetPixelFormat** con el resultado de **ChoosePixelFormat**.</span><span class="sxs-lookup"><span data-stu-id="6516a-120">Typically, you call **ChoosePixelFormat** to find a best-match pixel format, and then call **SetPixelFormat** with the result of **ChoosePixelFormat**.</span></span>

<span data-ttu-id="6516a-121">Si llama a **SetPixelFormat** para un contexto de dispositivo que haga referencia a una ventana, **SetPixelFormat** también cambiará el formato de píxel de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6516a-121">If you call **SetPixelFormat** for a device context that references a window, **SetPixelFormat** also changes the pixel format of the window.</span></span> <span data-ttu-id="6516a-122">Establecer el formato de píxel de una ventana más de una vez puede provocar complicaciones significativas para el administrador de ventanas y para las aplicaciones multiproceso, por lo que no se permite.</span><span class="sxs-lookup"><span data-stu-id="6516a-122">Setting the pixel format of a window more than once can lead to significant complications for the Window Manager and for multithread applications, so it is not allowed.</span></span> <span data-ttu-id="6516a-123">Puede establecer el formato de píxel de una ventana solo una vez; después de eso, no se puede cambiar el formato de píxel de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6516a-123">You can set the pixel format of a window only one time; after that, the window's pixel format cannot be changed.</span></span>

<span data-ttu-id="6516a-124">La función [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) devuelve un índice de formato de píxel basado en uno.</span><span class="sxs-lookup"><span data-stu-id="6516a-124">The [**GetPixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-getpixelformat) function returns a one-based pixel format index.</span></span>

<span data-ttu-id="6516a-125">La función [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) toma los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="6516a-125">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function takes the following as parameters:</span></span>

-   <span data-ttu-id="6516a-126">Identificador de un contexto de dispositivo</span><span class="sxs-lookup"><span data-stu-id="6516a-126">A handle to a device context</span></span>
-   <span data-ttu-id="6516a-127">Índice de formato de píxel</span><span class="sxs-lookup"><span data-stu-id="6516a-127">A pixel format index</span></span>
-   <span data-ttu-id="6516a-128">Puntero a una estructura de datos [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)</span><span class="sxs-lookup"><span data-stu-id="6516a-128">A pointer to a [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) data structure</span></span>

<span data-ttu-id="6516a-129">La función [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) devuelve con los miembros de **PIXELFORMATDESCRIPTOR** establecidos correctamente.</span><span class="sxs-lookup"><span data-stu-id="6516a-129">The [**DescribePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-describepixelformat) function returns with the members of **PIXELFORMATDESCRIPTOR** appropriately set.</span></span>

<span data-ttu-id="6516a-130">La función **GetEnhMetaFilePixelFormat** devuelve el tamaño del formato de píxel de un metarchivo y recupera la información del formato de píxel del metarchivo.</span><span class="sxs-lookup"><span data-stu-id="6516a-130">The **GetEnhMetaFilePixelFormat** function returns the size of a metafile's pixel format and retrieves the pixel format information of the metafile.</span></span>

 

 




